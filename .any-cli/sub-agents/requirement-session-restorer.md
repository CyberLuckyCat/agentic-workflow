# SUBAGENTS

自动读取meta.yaml（需求处于哪个阶段）、process.txt（需求当前的进度）、notes.md（需求实现过程中发生了什么），还原需求进度的上下文。

# 职责

1、读取meta.yaml

2、读取process.txt

3、读取notes.md

4、TODO: 结合前三个步骤中的文件内容，结合universal-context-collector返回的内容，还原工作区上下文？（我感觉其实有点冗余，因为如果这三个文件本身就是上下文进度的话，直接读取不就好了？）

# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

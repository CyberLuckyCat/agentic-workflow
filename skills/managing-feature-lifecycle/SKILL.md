# 描述与知识块

Skill 本身就带有描述信息，匹配AGENTS 或 SUBAGENTS的描述后，被进行调用。

# 规范

本md文件，上下文指令必须 < 2k token，内部只能包含对代码、资源文件的链接，不允许深层嵌套。

资源文件已经拆分到res/scripts（代码块）与res/refs（模板与参考资料）中。

skills/skillnamefold 作为一个完整的知识包。


TODO：往该skill的res目录中写入规则时，每条规则都要回答：

1、这条规则被违反的频率有多高？

2、如果违反频率很低，则不需要每次执行时都会加载进入上下文中，浪费上下文空间。


# 职责

通过详细设计阶段，detail-design-quality-reviewer的agent进行匹配调用，并进入到任务规划阶段。

1、对详细设计的结果，进行功能点拆分。

2、进入开发门禁，或可以理解为将当前需求的开发状态由设计方案，变为代码实现？（到底有几个门禁？如何界定门禁？它是否要通过gate-traceability-checker的检查？由谁来调用这个gate-traceability-checker的Skill？）

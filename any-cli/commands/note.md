---
description: "随手记录开发过程中的关键信息，到需求笔记"
allowed-tools: ["Glob", "Read", "Write", "Edit", "Bash"]
---
# 整理知识库索引

使用 `/note`命令后触发，读取用户输入并按照步骤执行。


步骤

1、若用户明确要求，将输入的信息记录到项目、团队的知识库中，则向用户确认要修改的目录。否则，默认将更新内容，放入当前requirement下的notes.md文件中。

2、触发规范维护检测（doc-spec-curator）的subagent。

3、触发项目中的规范检索（doc-spec-retriever）的subagent。

4、根据条件判断，决定是否触发文档批量更新（doc-batch-updater）的subagent。

---
description: "随手记录开发过程中的关键信息，到需求笔记"
allowed-tools: ["Glob", "Read", "Write", "Edit", "Bash"]
---
# 整理知识库索引

使用 `/note`命令后触发。

1、触发规范维护检测（doc-spec-curator）的subagent。

2、触发项目中的规范检索（doc-spec-retriever）的subagent。

3、根据条件判断，决定是否触发文档批量更新（doc-batch-updater）的subagent。

4、TODO: 如果知识是有用的范式、能够上升到全project或team使用的，是否要考虑加入团队知识库中，而非仅更新对应requirement下的notes.md？

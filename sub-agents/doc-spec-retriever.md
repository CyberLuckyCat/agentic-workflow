# SUBAGENTS

同文章中的"engineering-spec-retriever"，改名为doc-spec-retriever感觉更符合用途与归类。

作用：规范检索。

用户输入/note命令或由其他Agent在工作中需要时触发。

也可以设置计划，定时执行。

提取当前requirement目录下的notes.md，记录文档内包含的规范内容与文档修改日期。

若被Agent调用：

1、需要时返回文档修改日期。

2、需要时，根据Agent意图返回相关的文档规范内容。

# 职责

减少主Agent的上下文消耗。

专门使用此Subagent，查阅需求内的notes.md规范文档，并返回给主Agent。

# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

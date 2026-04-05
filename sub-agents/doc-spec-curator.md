# SUBAGENTS

同文章中的"engineering-spec-curator"，改名为doc-spec-curator感觉更符合用途与归类。

作用：规范维护（基于特定的规则判断，来确定是否需要触发维护、如何更新等一系列条件）

可由/note命令主动触发或定期执行。

扫描发现对应requirement下的notes.md文档后（如：作为关联文件在长时间内未被编辑、更新），按照doc-spec-retriever查询到的规则，判断是否需要触发更新。


TODO: 如何随手记录，如何在需求确认验收后提取局部requirement中的notes.md（知识提炼，将需求专属的结构化经验、SOP或检查清单）沉淀到context/中


# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

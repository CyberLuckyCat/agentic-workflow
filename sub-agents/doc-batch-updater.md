# SUBAGENTS

由主Agent根据doc-spec-curator的规则步骤，触发doc-batch-updater。

规则步骤：

1、为requirement中的notes.md新增内容或更新相关规范。

2、TODO: 使用xxxx skill结合context/team下的git规范，自动提PR到main分支（只有main分支是同步沉淀这些内容的，其他跟随feature分支切换不同的requirement）。

PR这部分是需要人类review的，审查知识的更新是否准确、AI读取到之后能否做出正确判断，扫一眼有没有误导性内容后合入。

# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

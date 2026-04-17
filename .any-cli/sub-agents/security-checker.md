# SUBAGENTS

需求的当前阶段：开发实施。

# 职责

输入校验、SQL注入、敏感信息泄露、权限校验

# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

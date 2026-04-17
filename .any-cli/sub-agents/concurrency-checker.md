# SUBAGENTS

需求的当前阶段：开发实施。

# 职责

竞态条件、死锁风险、goroutine泄露、channel使用

# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

complexity

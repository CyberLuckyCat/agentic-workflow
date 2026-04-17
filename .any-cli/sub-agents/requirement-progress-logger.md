# SUBAGENTS

实时记录当前requirement的进度（TODO: 根据阶段来？不同阶段分别记录啥？还是只记录那个8个阶段的需求状态？）到progress.txt中进行存档，确保切换分支之后再回来，依旧能使用/requirement-continue 恢复任务进度。

# 职责

# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

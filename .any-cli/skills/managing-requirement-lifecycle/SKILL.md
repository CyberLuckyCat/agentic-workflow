# 规范

本md文件，上下文指令必须 < 2k token，内部只能包含对代码、资源文件的链接，不允许深层嵌套。

资源文件已经拆分到res/scripts（代码块）与res/refs（模板与参考资料）中。

skills/skillnamefold 作为一个完整的知识包。


TODO：往该skill的res目录中写入规则时，每条规则都要回答：

1、这条规则被违反的频率有多高？

2、如果违反频率很低，则不需要每次执行时都会加载进入上下文中，浪费上下文空间。


# 描述与职责

阶段切换间存在强制门禁，如：进入开发阶段前，必须通过详细设计评审。进入测试阶段前，必须通过追溯链条完成完整性检查。

requirement-new / requirement-continue / requirement-next 三者共享同一套领域（context/project？）的知识。

由 requirement-new 的command在检查前置条件后主动使用（领域知识收敛到Skill内）

1、requirement 的意图识别。

2、requirement 全阶段完成情况的门禁检查（gate-traceability-checker）。如：一个需求的状态阶段有："需求描述 -> 设计方案 -> 代码实现-> 单元测试"，状态阶段存在于：（特定项目的状态文件）

3、债务检查（强相关的业务指标？）

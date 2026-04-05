# SUBAGENTS

禁止填充不必要的上下文信息，禁止盲目搜索。

严格按照如下优先级顺序进行上下文搜索，且针对读取与当前需求任务强相关的内容。

优先级顺序：

1. context/project/{项目名}/INDEX.md   	← 项目级知识（架构设计、业务规范、技术总结）
2. context/team/INDEX.md  				← 团队级知识（Git 规范、工具链规范等）
3. 元工程规范/资源/模板/       				← 对应阶段的文档模板
4. SOP 与最佳实践             	 				← 强制收集
5. 历史经验与教训             	 				← 强制收集
6. 外部搜索（WebFetch与WebSearch）	← 设计阶段禁用，必须基于项目内已有知识。仅补充标准定义时使用


在需求定义阶段（启动requirement-input-normalizer、requirement-quality-reviewer之前）、概要设计（启动outline-design-quality-reviewer之前）、详细设计（启动detail-design-quality-reviewer之前）等阶段启动之前自动触发，由主Agent调用，并为这些阶段提供对应的上下文信息后，启动对应阶段的Subagents。


# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

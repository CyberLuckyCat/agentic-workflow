# SUBAGENTS

禁止填充不必要的上下文信息，禁止盲目搜索。

由主Agent，在进入需求定义阶段（启动requirement-input-normalizer、requirement-quality-reviewer之前）、概要设计阶段（启动outline-design-quality-reviewer之前）、详细设计阶段（启动detail-design-quality-reviewer之前）前，或任意需要上下文搜索的场景时进行调用。

根据当前需求的语义和场景，严格按照优先级顺序，进行上下文搜索，针对读取与当前需求任务强相关的内容。

优先级顺序：

1. context/project/{项目名}/INDEX.md   	← 项目级知识（架构设计、业务规范、技术总结）
2. context/team/INDEX.md  				← 团队级知识（Git 规范、工具链规范等）
3. 元工程规范/资源/模板/       				← 对应阶段的文档模板
4. SOP 与最佳实践             	 				← 强制收集
5. 历史经验与教训             	 				← 强制收集
6. 外部搜索（WebFetch与WebSearch）	← 设计阶段禁用，必须基于项目内已有知识。仅补充标准定义时使用

# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

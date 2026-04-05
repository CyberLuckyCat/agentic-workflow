# SUBAGENTS

代码检查工具，与结构测试。

明确哪些需要限制（模块边界、代码品味、类型命名规范、文件大小限制、特定平台可靠性等），哪些不需要限制（允许解决方案的表达自由）

实现该Agent时，基于"他们的原则是 *"enforce invariants, not micromanage implementations"*——和我在工具设计规范中提出的"封装知识而非流程"一脉相承。更有趣的是一个细节：他们把自定义 lint 的错误信息写成 Agent 的修复指导—— **把约束和修复指引绑定在同一条反馈链路上** 。"的描述，先阅读文章：https://openai.com/zh-Hans-CN/index/harness-engineering/，理解什么是lint/linter与CI后，再阅读 https://lexi-lambda.github.io/blog/2019/11/05/parse-don-t-validate/ 与 https://bits.logic.inc/p/ai-is-forcing-us-to-write-good-code。每阅读一篇文章，先向我给出你分析得出的几点结论，在面板向我确认后，按照你规划实现步骤填充该linter.md的内容。


# 规范

为主Agent隔离工作区上下文，返回到主Agent工作区上下文中的内容，必须 < 2000 token。

Subagent之间禁止嵌套调用，仅由主Agent协调选择调用。

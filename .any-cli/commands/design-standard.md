---
description: "设计标准"
allowed-tools: ["Bash", "Read", "Glob"]
---

# 规范

单条Command必须 < 100行指令。

只做 条件检查 与 委托调用。如：requirement-new 会调用 managing-requirement-lifecycle 跑新需求启动流程。

# 描述

多个Command之间，在同一个语境中共享一套领域知识。

Command不该臃肿与冗余，降低维护复杂度（个人理解是： 此处只做Skill接口调用，具体实现交给Skill去做。确保command不会耦合skill，导致维护复杂度上升）


# 备注

不需要开辟额外Subagent，不需要领域知识或多步工作流的情况下，且高频、固定的入口或动作，可以封装成Command（若非高频且固定，则写在规范里，不需要将其Command工具化）。

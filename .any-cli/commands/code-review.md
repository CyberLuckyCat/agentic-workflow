---
description: "启动7个Checker的代码审查流程"
allowed-tools: ["Bash", "Read", "Glob"]
---
## 描述

用户输入/code-review，或"帮我审查一下代码"时触发。

## 执行步骤

1. 预检：

   - 调用code-review-perpare的Skill（自动识别当前需求、发现待审查的服务仓库、获取增量变更、确认审查范围）
2. **并行审查**：

   - 并行触发7个Subagent：同时工作，
3. **汇总报告**：

   - 调用code-review-report的Skill（合并所有结果，生成统一的审查报告）

# Mission: Issue 2004 Code Review Agent

## Why
掌握 issue #2004 可能涉及的背景知识，读懂其中的框架术语、Go 代码评审概念、安全边界、存储语义和验收指标。目标不是学习如何实现这个 issue，而是具备独立实现前需要的知识底座。

## Success looks like
- 能解释 issue 中 `Skill`、`workspace runtime`、`CodeExecutor`、`PermissionPolicy`、`Filter`、`Telemetry`、`Session / SQL storage` 等词在框架里的含义。
- 能区分自动代码评审 Agent、普通 diff scanner、静态分析工具、LLM 文本点评之间的概念差异。
- 能读懂 unified diff、Go package、hunk、候选行号、`go test`、`go vet`、Staticcheck 等背景知识。
- 能解释安全边界相关术语：沙箱、超时、输出大小限制、环境变量白名单、敏感信息脱敏、artifact 限制、治理拦截。
- 能理解结构化 finding、severity、confidence、source、rule_id、dedup、warnings、needs_human_review 的含义和取舍。
- 能说明 SQLite 或等价持久化存储为什么会出现在该 issue 中，以及 task、sandbox run、permission decision、finding、artifact、report、metrics 分别代表什么信息。

## Constraints
- 默认用中文学习和记录。
- 先学读懂 issue 所需的框架和外部知识，不把 GraphAgent、A2A、AG-UI、长期 memory 等旁支展开。
- 资料必须来自当前 issue、仓库代码或一手官方文档；无法确认的内容不进入 lesson 结论。
- 不提供具体实现步骤、目录设计、代码方案或任务拆解，除非用户明确切换到实现讨论。

## Out of scope
- 从零实现一个独立于 tRPC-Agent-Go 的代码评审 CLI。
- 深入学习全部 tRPC-Agent-Go 组件。
- 教用户如何完成 issue 的具体实现。
- 训练或评测真实大模型能力。

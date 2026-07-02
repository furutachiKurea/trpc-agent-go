# Mission: Issue 2004 Code Review Agent

## Why
掌握 issue #2004 必须依赖的 tRPC-Agent-Go 框架知识与能力：读懂其中的框架术语，并具备用框架 API 实现 Skill、PermissionPolicy、CodeExecutor、Storage、Telemetry 等组件的能力。issue 必须用这个框架来实现，因此目标包含"会用"而不仅是"能解释"。仍然不学习 issue 2004 本身的目录设计、任务拆解或具体实现方案。

## Success looks like
- 能解释 issue 中 `Skill`、`workspace runtime`、`CodeExecutor`、`PermissionPolicy`、`Filter`、`Telemetry`、`Session / SQL storage` 等词在框架里的含义。
- 能写代码调用这些框架 API：定义并注册一个 `PermissionPolicy`、编写 `SKILL.md` 并通过 `LLMAgent` 加载、调用 `CodeExecutor` 执行程序并读取 `RunResult`、配置 Session/SQL storage 和 Telemetry。
- 能区分自动代码评审 Agent、普通 diff scanner、静态分析工具、LLM 文本点评之间的概念差异。
- 能读懂 unified diff、Go package、hunk、候选行号、`go test`、`go vet`、Staticcheck 等背景知识。
- 能解释安全边界相关术语：沙箱、超时、输出大小限制、环境变量白名单、敏感信息脱敏、artifact 限制、治理拦截。
- 能理解结构化 finding、severity、confidence、source、rule_id、dedup、warnings、needs_human_review 的含义和取舍。
- 能说明 SQLite 或等价持久化存储为什么会出现在该 issue 中，以及 task、sandbox run、permission decision、finding、artifact、report、metrics 分别代表什么信息。

## Constraints
- 默认用中文学习和记录。
- 框架能力学习聚焦于 issue 2004 用得到的部分（Skill、PermissionPolicy、CodeExecutor、Session/Storage、Telemetry 及其配套 API），不把 GraphAgent、A2A、AG-UI、长期 memory 等旁支展开。
- 资料必须来自当前 issue、仓库代码或一手官方文档；无法确认的内容不进入 lesson 结论。
- 教框架 API 用法时可以给出通用示例代码；不直接给出 issue 2004 的目录设计、任务拆解或整体实现方案，除非用户明确切换到实现讨论。

## Out of scope
- 从零实现一个独立于 tRPC-Agent-Go 的代码评审 CLI。
- 深入学习 issue 2004 用不到的 tRPC-Agent-Go 组件。
- 直接给出 issue 2004 的具体实现方案、目录结构或任务拆解。
- 训练或评测真实大模型能力。

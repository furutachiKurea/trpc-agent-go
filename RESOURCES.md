# Issue 2004 Code Review Agent Resources

## Knowledge

- [GitHub Issue #2004: 基于 Skills + 沙箱 + 数据库存储构建自动代码评审 Agent](https://github.com/trpc-group/trpc-agent-go/issues/2004)
  任务的权威需求来源。用于理解：验收标准、交付物、必须覆盖的能力边界。
- [tRPC-Agent-Go README](README.md)
  框架定位和顶层能力索引。用于理解：这是 Go-native Agent 框架，不是单一应用。
- [tRPC-Agent-Go Skill 文档](docs/mkdocs/en/skill.md)
  Skill 的当前推荐用法。用于理解：`WithSkills`、`skill_load`、`workspace_exec`、local fallback、container executor。
- [Runner 中文文档](docs/mkdocs/zh/runner.md)
  Runner、Session、Event 流的入口文档。用于理解：一次 run 的会话、事件流和持久化语义。
- [Workspace I/O Example](examples/workspace_io/README.md)
  workspace facade 和 artifact/collect/run pattern 示例。用于理解：workspace 文件、artifact、collect、run 的概念边界。
- [Tool Policy Example](examples/toolpolicy/README.md)
  `PermissionPolicy`、tool metadata、`allow/deny/ask` 的最小示例。用于理解：高风险命令治理。
- [Container Code Execution Example](examples/codeexecution/container/README.md)
  Docker container executor 的配置和安全注意事项。用于理解：沙箱、网络关闭、镜像和资源限制。
- [SQLite Session 文档](docs/mkdocs/zh/session/sqlite.md)
  框架 SQLite session service 的用法和限制。用于理解：SQLite、CGO、WAL、busy timeout 和持久化背景。
- [Git diff-format documentation](https://git-scm.com/docs/diff-format)
  Git diff 格式一手来源。用于理解：`diff --git`、`---/+++`、hunk header、added line 行号映射。
- [Go command: Test packages](https://pkg.go.dev/cmd/go#hdr-Test_packages)
  `go test` 行为一手来源。用于理解：`go test` 只运行高置信 vet 子集，不能等同完整静态分析。
- [Go vet command](https://pkg.go.dev/cmd/vet)
  `go vet` 官方说明。用于理解：vet 检查范围、退出码语义和启用/禁用单项检查。
- [Go context package](https://pkg.go.dev/context)
  context/cancel 生命周期权威来源。用于理解：context 泄漏、取消传播、`CancelFunc` 必须调用。
- [Go database/sql package](https://pkg.go.dev/database/sql)
  数据库连接、事务和 context 语义权威来源。用于理解：`Conn.Close`、`BeginTx`、commit/rollback 生命周期规则。
- [Staticcheck checks](https://staticcheck.dev/docs/checks)
  Staticcheck 规则索引。用于理解：可选增强检查和 rule_id 命名参考。
- [E2B Documentation](https://e2b.dev/docs)
  E2B 沙箱概念来源。用于理解：远程沙箱方案、环境和 API key 前提。

## Wisdom (Communities)

- [trpc-group/trpc-agent-go Issues](https://github.com/trpc-group/trpc-agent-go/issues)
  项目维护者公开讨论区。用于理解：需求澄清和接口语义讨论。
- [trpc-group/trpc-agent-go Pull Requests](https://github.com/trpc-group/trpc-agent-go/pulls)
  查看维护者接受的讨论和代码评审方式。用于理解：项目偏好的表达方式和评审关注点。

## Gaps

- Cube 沙箱在当前本地仓库里的可直接复用入口尚未梳理；背景课先覆盖 issue 明确点名的 container 与 E2B。
- 隐藏样本的判分规则不可见；背景课只解释检出率、误报率、置信度和人工复核这些评价概念。

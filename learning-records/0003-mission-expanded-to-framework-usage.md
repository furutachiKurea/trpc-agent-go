# Mission Expanded: From "Explain" to "Use"

之前的 mission 边界（学习记录 0002）把范围限定在"能解释术语含义"，不涉及框架 API 的实际使用方法。用户指出这个边界有问题：issue #2004 必须用 tRPC-Agent-Go 框架实现，如果不学会怎么调用框架 API（如何注册 PermissionPolicy、如何写 SKILL.md 并加载、如何调用 CodeExecutor、如何配置 Storage/Telemetry），就无法独立实现这个 issue，纯术语解释是不够的。

Mission 已更新（2026-07-02）：

- Success looks like 新增一条：能写代码调用 PermissionPolicy、SKILL.md/LLMAgent 加载、CodeExecutor、Session/SQL storage、Telemetry 等框架 API。
- Constraints 放宽：教框架 API 用法时可以给通用示例代码。
- 仍然保留的边界：不直接给 issue 2004 的目录设计、任务拆解或整体实现方案——这是"学会用框架的通用能力" vs "issue 2004 专属架构方案"之间的区分，后者仍需用户明确切换到实现讨论才展开。

后续 lesson 设计应包含可运行的框架 API 示例代码（如最小 PermissionPolicy 实现、最小 SKILL.md + workspace_exec 用法），而不仅是概念表格。

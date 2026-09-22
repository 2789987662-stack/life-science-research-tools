# Marketplace 打包校验

- Marketplace JSON：通过
- 插件数：3
- 每个插件均包含 `.codex-plugin/plugin.json`：是
- 每个插件均包含 `skills/<name>/SKILL.md`：是
- 每个 Skill 均包含运行时签名：是
- MCP manifest：无（避免因 MCP 声明被标记为 Desktop only）
- Marketplace manifest 位置：`.agents/plugins/marketplace.json`（仓库根目录）

## 结论
结构校验通过，可作为 GitHub marketplace 仓库根目录使用。

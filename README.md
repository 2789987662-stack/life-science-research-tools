# Life Science Research Tools Marketplace

这是为 ChatGPT Work 准备的插件市场仓库，包含三个独立插件：

1. `nature-reviewer`
2. `academic-research-suite`
3. `scientific-agent-skills`

## 为什么这样打包

- 每个插件只装一个明确的 Skill，降低路由歧义。
- 不声明 MCP server，避免因为 MCP 清单被标记为 Desktop only。
- 每个 Skill 都带 `references/runtime-check.md`，用于验证“真的加载了 Skill 本体”，而不是只识别到 @ 标签。
- `.agents/plugins/marketplace.json` 位于仓库根目录，因此从 GitHub 导入时“稀疏路径/Path”应留空。

## GitHub 导入

将本目录完整上传到一个 GitHub 仓库，例如：

`https://github.com/<你的账号>/life-science-research-tools`

然后在“添加插件市场”中填写：

- 来源：仓库 URL（只填仓库 URL，不要填 branch 或子目录 URL）
- Git 引用：`main`，或留空使用默认分支
- 稀疏路径 / Path：留空

导入后，到每个插件详情页确认安装策略。若希望自己可直接使用，将其设为可安装或已安装，具体选项取决于你的工作空间权限。

## 本地目录导入

如果当前客户端支持从本地文件夹添加市场：
- 解压本 ZIP
- 选择本目录 `life-science-research-tools-marketplace`
- 路径仍留空

## 预检

新开一个 Work 对话，逐个测试：

### Nature Reviewer
`@nature-reviewer 请只执行运行时自检，并报告 PACKAGE_SIGNATURE。`

应返回：
`NATURE-REVIEWER-WORK-PORTABLE-1.0`

### Academic Research Suite
`@academic-research-suite 请只执行运行时自检，并报告 PACKAGE_SIGNATURE。`

应返回：
`ACADEMIC-RESEARCH-SUITE-WORK-PORTABLE-1.0`

### Scientific Agent Skills
`@scientific-agent-skills 请只执行运行时自检，并报告 PACKAGE_SIGNATURE。`

应返回：
`SCIENTIFIC-AGENT-SKILLS-LIFESCI-WORK-PORTABLE-1.0`

如果只能识别 @ 标签，但读不出对应签名，就视为插件/Skill 没有完整加载。

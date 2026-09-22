# 迁移说明

## 与旧 research-skills-local 的区别

旧方案的问题是：前端可能保留 `@xxx@research-skills-local` 的引用，但 Work 的实际运行环境不一定挂载对应 Skill 文件。

本市场改成：
- GitHub/本地 marketplace
- 3 个独立插件
- 每个插件包含 1 个自包含 Skill
- 每个 Skill 有独立运行时签名

## 旧插件处理

新插件全部通过预检后，旧 `research-skills-local` 项可以删除或忽略。
如果旧项仍出现在 @ 菜单中，优先从旧 marketplace/source 侧移除，以避免重名和路由歧义。

## 已经手工创建了同名 Skill 怎么办

手工创建的个人 Skill 和 marketplace 插件不是同一个对象。
测试 marketplace 插件时，请明确选择插件来源，避免把个人 Skill 的成功误认为插件成功。

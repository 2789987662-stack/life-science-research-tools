---
name: scientific-agent-skills
description: >
  面向生命科学科研项目的 Scientific Agent Skills Work 便携精选路由器。
  聚焦文献检索与综述、科研信息核验、科学写作、生物信息学、统计/模型评价和可重复性，
  避免加载与当前生命科学竞赛无关的大量技能。
metadata:
  version: "life-science-work-portable-1.0"
  upstream: "kinandigital/scientific-agent-skills"
  upstream_commit: "36fd74c052b019eebeb8e195d566a00a07fc05b0"
  adapter: "curated ChatGPT Work compatibility layer"
---

# Scientific Agent Skills — 生命科学 Work 精选版

## 启动校验
显式调用时首先读取 `references/runtime-check.md`。
若无法读取签名，不得声称本 Skill 已加载。

## 路由
- 文献综述 / 系统检索 → `modules/literature-review.md`
- 查论文 / 核验科研事实 / 找方法来源 → `modules/research-lookup.md`
- 科学写作 / 结果与讨论组织 → `modules/scientific-writing.md`
- FASTA、序列、数据库、注释、生物信息学脚本思路 → `modules/bioinformatics.md`
- 机器学习与统计评价 → `modules/model-evaluation.md`
- 复现、审计、版本与数据泄漏检查 → `modules/reproducibility.md`

## 本项目优先
在 Cas13 / LACE / TIGER 类项目中，优先关注：
- guide / crRNA 与 target RNA 的序列和上下文
- RNA 二级结构、可及性、热力学代理量
- 数据划分与同源序列泄漏
- 模型基线、消融、外部验证
- mismatch / wobble / indel / 结构效应的证据边界
- 预测结果与湿实验读出的层级差异
- 可复现代码、数据版本与冻结集

## Work 兼容原则
上游若要求特定 CLI、API key 或本地脚本，而当前 Work 没有这些工具，
改用当前环境可用的网页检索、文件检索、Python/代码执行或数据库网页完成同等目标；
不得假装运行了不存在的命令。

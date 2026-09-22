---
name: academic-research-suite
description: >
  ARS-Codex 的 ChatGPT Work 便携兼容层。用于深度研究、文献综述、系统综述、
  学术写作、论文审稿、研究到论文的分阶段流程、实验规划与结果验证。
  支持 ars-plan、ars-outline、ars-reviewer、ars-full 等意图别名。
metadata:
  version: "work-portable-1.0"
  upstream: "Imbad0202/academic-research-skills-codex"
  upstream_commit: "3c37ef8ab480ba1e9370309c24b99977ad44091f"
  upstream_version: "3.22.0"
  adapter: "ChatGPT Work portable compatibility layer"
---

# Academic Research Suite — Work 便携版

## 启动校验
显式调用时首先读取 `references/runtime-check.md`。
读取失败时，不得声称 ARS 已加载。

## 路由
根据用户意图读取对应模块：

- 深度研究、文献综述、系统综述、事实核查、研究问题收敛
  → `workflows/deep-research.md`
- 论文规划、提纲、摘要、起草、修改、引文核查
  → `workflows/academic-paper.md`
- 论文审稿、复审、审稿校准
  → `workflows/academic-paper-reviewer.md`
- 从研究到论文的端到端分阶段流程
  → `workflows/academic-pipeline.md`
- 实验设计、统计解释、可重复性验证
  → `workflows/experiment-agent.md`

若任务跨多个阶段，优先使用 `academic-pipeline`；
若用户只有宽泛题目而没有清晰研究问题，先进入 `deep-research` 的苏格拉底式收敛。

## 别名
将下列普通文本或斜杠形式作为模式快捷入口理解：
- ars-plan
- ars-outline
- ars-abstract
- ars-lit-review
- ars-citation-check
- ars-revision-coach
- ars-revision
- ars-reviewer
- ars-rebuttal-audit
- ars-full

若客户端拦截斜杠命令，使用不带斜杠的普通文本别名。

## Work 兼容原则
1. 不假设存在 Codex 专用 hooks、Claude 子智能体、特定 Bash 命令或本地持久状态。
2. 若当前 Work 环境具有文件、浏览器、代码执行、并行任务或应用工具，可用其实现同等目标。
3. 若环境不支持真正的隔离子智能体，不得声称已完成“独立多智能体”验证。
4. 不把计划中的模型配置表述为当前实际模型。
5. 外部检索得到的事实必须可追溯；用户提供文件优先于一般背景知识。
6. 任何涉及事实核查、当前研究或文献状态的任务，优先使用真实来源，而不是凭记忆补齐。
7. 用户拥有最终研究决策权；Skill 提供结构化分析，不替用户作价值判断。

## 项目语言
服从所在项目的语言与术语规则。若项目无特别规定，则默认使用用户当前语言。

# 生物信息学模块

适用于序列、转录本、RNA 结构和数据库任务。

基本纪律：
- 明确参考基因组/转录组版本、accession、序列方向和坐标体系。
- RNA/DNA 字母与互补方向必须核对。
- 记录软件/数据库版本和关键参数。
- RNAfold 等预测代表计算结构模型，不等同于实验结构。
- 多转录本基因需说明使用哪个 isoform。
- near-match / off-target 搜索需记录允许错配、indel、wobble 与过滤条件。
- 任何批量处理先保留原始输入和可追溯中间表。

涉及 Cas13 时，区分 crRNA 的 DR 与 spacer，不把 guide、target、protospacer 方向混用。

# 来源与适配说明

本包是为 ChatGPT Work 稳定调用制作的便携兼容层，不是上游仓库的逐字节镜像。

上游项目：
- Yuan1z0825/nature-skills
- 路径：skills/nature-reviewer
- 固定参考提交：9c9953a06cd33a88cbd258386a295ca4b6a1ef1e
- 上游许可证：Apache-2.0

本兼容层保留上游 nature-reviewer 的核心思想：
三份独立审稿、审稿后综合、证据锚定、Major/Minor 分层、阻断问题校准、
来源约束、不可虚构和角色边界。为提高 Work 兼容性，去除了对特定本地运行时、
测试脚本和外部目录结构的硬依赖，并补充了生命科学审稿门和运行时自检。

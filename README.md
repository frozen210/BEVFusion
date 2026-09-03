# BEVFusion

本仓库是基于 [mit-han-lab/bevfusion](https://github.com/mit-han-lab/bevfusion) 的独立维护版本，用于 LiDAR 与相机融合的 3D 感知研发。上游基线完整保留在 `v0-upstream` tag；项目继续遵循 [Apache License 2.0](LICENSE)。

> 当前尚未修改上游算法实现。所有自有改动均应记录在下方修改记录中，并可通过 `git diff v0-upstream...HEAD` 审查。

## 快速开始

```bash
git clone https://github.com/frozen210/BEVFusion.git
cd BEVFusion
python setup.py develop
```

完整的环境依赖、数据准备、训练、评测和可视化说明请参阅 [上游使用文档](README_UPSTREAM.md#usage)。执行其中的 clone 步骤时，请使用本仓库上方给出的地址。

## 项目目录

| 路径 | 用途 |
| --- | --- |
| `configs/custom/` | 项目自有模型及实验配置，与上游配置隔离 |
| `scripts/` | 环境搭建、数据预处理和训练脚本 |
| `experiments/` | 实验设置、完整指标和配置差异记录 |
| `docs/` | 技术方案、复现报告和环境搭建记录 |
| `README_UPSTREAM.md` | 未修改的上游 README，保留原始使用说明与署名 |

## 基线与修改记录

上游基线为 `mit-han-lab/bevfusion` 的提交 `326653d`（51 commits），在本仓库标记为 `v0-upstream`。

| 日期 | 修改内容 | 对算法/模型的影响 |
| --- | --- | --- |
| 2026-09-03 | 增加权重、训练输出、可视化和部署产物的忽略规则 | 无 |
| 2026-09-03 | 建立项目 README，并将上游原文保存为 `README_UPSTREAM.md` | 无 |
| 2026-09-03 | 建立 `docs/`、`experiments/`、`scripts/` 和 `configs/custom/` 目录规范 | 无 |

后续修改上游代码、配置或行为时，请在本表中显著说明修改内容，并在对应实验记录中保留配置、权重来源和完整评测结果。

## 实验与分支约定

- `main`：稳定、可复现的基线与已验证改动。
- `feat/*`：单个结构或功能改动，一个主题一个分支。
- `exp/*`：仅用于超参数实验，完成归档后可删除。

实验记录应从 [`experiments/TEMPLATE.md`](experiments/TEMPLATE.md) 创建，至少包含 mAP、NDS、五项 TP 指标和十个类别的 AP。

## 许可证与致谢

本项目依据 [Apache License 2.0](LICENSE) 发布。上游版权、许可证文本和源文件中的版权声明均予以保留。原项目介绍、论文引用、模型结果及开源项目致谢请参阅 [README_UPSTREAM.md](README_UPSTREAM.md)。

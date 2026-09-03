# 实验记录

每次实验使用独立子目录，建议命名为 `YYYYMMDD-简短名称/`，并从 [TEMPLATE.md](TEMPLATE.md) 复制记录模板。

实验记录必须包含：

- 对应提交和配置差异；
- 数据版本、预训练权重来源和输出权重路径；
- GPU 型号与数量、单卡 batch size、梯度累积次数和实际总 batch size；
- mAP、NDS、mATE、mASE、mAOE、mAVE 和 mAAE；
- nuScenes 十个类别的逐类 AP；
- 结论、异常和下一步计划。

权重、日志、TensorBoard 文件和数据集不应提交到 Git；这里只保存可复现信息和小型文本结果。

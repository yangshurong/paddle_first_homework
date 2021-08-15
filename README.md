# 这里写自定义项目名称（大标题）

本次任务将基于PaddleSeg展开语义分割任务的学习与实践

# 一、项目背景

练习练习AI

# 二、数据集简介

本项目使用的数据集是:[AI训练营]语义分割数据集合集，包含马分割，眼底血管分割，车道线分割，场景分割以及人像分割。

## 1.数据加载和预处理

!python parse_horse_label.py


## 2.数据集查看
!python horse_create_train_list.py

# 三、模型选择和开发

选择模型，baseline选择bisenet,

## 1.模型训练


!python PaddleSeg/train.py\
--config PaddleSeg/configs/quick_start/bisenet_optic_disc_512x512_1k.yml\
--batch_size 4\
--iters 2000\
--learning_rate 0.01\
--save_interval 200\
--save_dir PaddleSeg/output\
--seed 2021\
--log_iters 20\
--do_eval\
--use_vdl

## 4.模型评估测试


!python PaddleSeg/val.py\
--config PaddleSeg/configs/quick_start/bisenet_optic_disc_512x512_1k.yml\
--model_path PaddleSeg/output/best_model/model.pdparams


## 5.模型预测
!python PaddleSeg/predict.py\
--config PaddleSeg/configs/quick_start/bisenet_optic_disc_512x512_1k.yml\
--model_path PaddleSeg/output/best_model/model.pdparams\
--image_path segDataset/horse/Images\
--save_dir PaddleSeg/output/horse

# 四、效果展示

图在文件底下

# 五、总结与升华


# 个人简介


# Cross_Module_Seg
-跨模态分割——建筑物提取  
-使用数据集ISPRS Potsdam  
-模型文件在`/models`中  使用预训练权重`pretrained_weight/vgg16`  
## 安装环境
运行`pip install -r requirements`  
## 训练
运行`python train.py` 或者使用命令行在`train.bat`中  
主要参数修改：`--data` 原始数据集根目录，我们通过编号索引找寻原始影像数据  
             `--img_sz` 窗口尺寸  
             `--stride` 滑动步长  
             `--arct` 模型选择  
             `--epochs`  `--save_period`模型保存频率，以1个epoch为单位  
             `--out_dir`训练权重文件保存路径
## 测试
运行`python test.py` 或者使用命令行在`test.bat`中  
主要参数修改：`--data` `--arct` 与训练时设置一样  
`--model_file` 加载权重文件  
`--out_dir` 预测图片保存路径
             

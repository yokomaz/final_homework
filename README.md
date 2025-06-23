# 这是复旦大学大数据学院张力老师的研究生课程：神经网络与深度学习 2025年度上半学期期末作业

problem1为任务1：选取身边物体拍摄多角度图片，使用COLMAP 估计相机参数，并使用 NeRF 加速技术（如 Plenoxels、TensoRF 等）进行物体重建和新视图合成；

problem2为任务2：选取同一物体拍摄多角度图片，使用COLMAP 估计相机参数后，采用 3D GaussianSplatting 方法进行物体重建和新视图合成。

训练好的网络权重，数据集在 https://drive.google.com/drive/folders/1n7jWwbzueo9ESeArs1OcIla9X_VbNh7v?dmr=1&ec=wgc-drive-globalnav-goto

# 任务1：

主要包含NeRF与TensoRF的渲染结果，包含不同iteration的video以及渲染图片。

## 训练方法

1. 从google drive连接中下载dataset。
2. 克隆NeRF-Pytorch或者TensoRF仓库，将数据集移动至对应仓库的data目录下
3. 修改config/config.txt文件，对应于数据集路径
4. 使用python train.py --config ./path/to/config实现训练。

## 测试方法

1. 训练以及测试数据集已经通过train.py进行划分，直接进行训练即可看到对应train test结果。

# 任务2使用方法：

主要包含1. 3D Gaussian Splatting的渲染点云以及结果文件。
## 渲染方法

根据3D Gaussian splatting的readme文件，下载安装viewer程序，修改由3D Gaussian Splatting生成的cfg_args文件后，运行.\SIBR gaussianViewer app.exe m ~viewer output查看实时结果

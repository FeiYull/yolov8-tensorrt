# YOLOv8-TensorRT
<div align="center">

  [![Cuda](https://img.shields.io/badge/CUDA-11.3-%2376B900?logo=nvidia)](https://developer.nvidia.com/cuda-toolkit-archive)
  [![](https://img.shields.io/badge/TensorRT-8.4.2.4-%2376B900.svg?style=flat&logo=tensorrt)](https://developer.nvidia.com/nvidia-tensorrt-8x-download)
  [![](https://img.shields.io/badge/ubuntu-18.04-orange.svg?style=flat&logo=ubuntu)](https://releases.ubuntu.com/18.04/)
  [![](https://img.shields.io/badge/windows-10-blue.svg?style=flat&logo=windows)](https://www.microsoft.com/)
  [![](https://img.shields.io/badge/pytorch-1.9.0-blue.svg?style=flat&logo=pytorch)](https://pytorch.org/)
  <br>
  </div>

## 性能速览
🍉我们来看看yolov8n在Nvidia RTX2070m(8G)上的性能表现：更多性能测试，在B站[![](https://img.shields.io/badge/bilibili-blue.svg?logo=bilibili)](https://www.bilibili.com/video/BV1vY4y1d7Dr/?spm_id_from=333.999.0.0&vd_source=a96c9c3f099f4167807291a34fd50fd5)可以观看。

<div align='center'>

| model | video resolution | model input size |GPU Memory-Usage |GPU-Util|
  :-: | :-: | :-: | :-: | :-: |
|yolov8n|1920x1080|8x3x640x640|1093MiB/7982MiB| 14%| 

 <center>	<!--将图片和文字居中-->
<img src=".github/run.jpg"
     alt="无法显示图片时显示的文字"
     style="zoom:40%"/>
<br>		<!--换行-->
<center>🚀cost time per frame	<!--标题--></center>
    <br>		<!--换行-->
</div>

## 介绍
YOLOv8部署（基于TensorRT、CUDA），一个end2end的cuda c实现。如果您还想在TensorRT下部署YOLOv7、YOLOv6、YOLOv5、YOLOv4、YOLOv3等模型，请看我的另一个仓库：TensorRT-Alpha：https://github.com/FeiYull/TensorRT-Alpha
注：opencv仅用于可视化！

## 更新
- 2023.01.08  🚀 全网最快支持yolov8的tensorrt部署

## 安装
兼容平台: Windows and Linux. 以下环境已被测过：<br>
<details>
<summary>Ubuntu18.04</summary>

- cuda11.3
- cudnn8.2.0
- gcc7.5.0
- tensorrt8.4.2.4
- opencv3.x or 4.x（仅用于可视化）
- cmake3.10.2
</details>

<details>
<summary>Windows10</summary>

- cuda11.3 
- cudnn8.2.0
- visual studio 2017 or 2019 or 2022
- tensorrt8.4.2.4
- opencv3.x or 4.x（仅用于可视化）
</details>

## 快速开始
### Ubuntu18.04
设置TensorRT根目录（安装目录）路径:
```bash
git clone https://github.com/FeiYull/yolov8-tensorrt
cd yolov8-tensorrt/cmake
vim common.cmake
# 把common.cmake文件第20行中的TensorRT_ROOT修改成您的TensorRT安装目录, 例如改成如下:
# set(TensorRT_ROOT /root/TensorRT-8.4.2.4)
```
开始编译、运行工程，例如:[yolov8](yolov8/README.md)


## 速览：官方效果 vs TensorRT-Alpha，执行速度
<br>
<div align='center'>			<!--块级封装-->
     <center>	<!--将图片和文字居中-->
    <img src=".github/yolov8n-Offical(left)vsOurs(right).jpg"
         alt="无法显示图片时显示的文字"
         style="zoom:100%"/>
    <br>		<!--换行-->
    <center>yolov8n : Offical( left ) vs Ours( right )	<!--标题--></center>
    <br>		<!--换行-->
    <br>		<!--换行-->
</div>
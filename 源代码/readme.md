# 兽友-动物识别系统

本系统是一款基于mobilenet模型的图像识别系统，能够识别生活中常见的动物并给出简洁的介绍，适用于各个年龄段的人群使用，有助于促进人与自然和谐相处。



## 一、环境配置

(1)首先电脑上需要有anaconda+pycharm这两个软件，anaconda是为了便于我们安装虚拟环境，pycharm便于我们查看代码及修改代码；

(2)进入代码所在文件路径下，在终端中输入

```
conda create -n animals python==3.7.3
```

使用conda创建一个名为"animals"的python版本为3.7.3的虚拟环境；

(3)虚拟环境创建完毕后，使用

```
conda activate animals
```

激活animals虚拟环境；

(4)虚拟环境激活后（命令行前出现(animals)的字样），使用

```
pip install -r requirement.txt
```

安装运行系统需要的库；

(5)至此，环境搭建成功，使用

```
python window.py
```

执行窗口文件，将会看到系统的用户界面，点击上传图片即可自由选择个人电脑上存储的图片进行识别。



## 二、文件介绍

data文件是个人收集的原始动物数据集，该数据集经过了清洗等，根据动物名称不同进行了分类；

images文件是整个系统相关的图片，比如logo、起始页图像等；

models文件是训练完成的模型，我们使用训练结果较好的mobilenet的模型（本来准备用cnn模型但是无论从训练结果还是测试结果来看效果都很差无法应用到系统中，所以选择了mobilenet模型）；

new_data中是手工划分的数据集，其中训练集：验证集：测试集=8：2：0，没有设置测试集是因为数据集的数量不够大，这里使用验证集充当测试集进行最后的测试；

results文件中包含了训练模型过程中的准确率以及损失函数的历史记录以及可视化图；

requirements.txt 是本项目需要的包；

train_mobilenet.py 是训练mobilenet模型的代码；

window.py 是界面文件，主要是利用pyqt5完成的界面，通过上传图片可以对图片种类进行预测；








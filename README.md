# 鬼抽-菩提老祖
【AI创造营】参赛作品
# **鬼畜小视频**

## AiStuido地址：https://aistudio.baidu.com/aistudio/projectdetail/1647685
## BiliBili视频地址：https://www.bilibili.com/video/BV1Zv411b7Pn

## **这里使用的PaddleGan套件的first order model模型，用于人脸动作迁移**
#### **1. 准备好需要迁移的人脸动作视频（视频最好都是头部，头不要瞎动的那种，要不效果不是太好）**
#### **2. 准备要动图片（也是只有头部）**
#### **3. 运行脚本，等待输出~**


# 菩提老祖: 烧焦了诶~

<div align='center'>
  <img src="https://ai-studio-static-online.cdn.bcebos.com/b94857f896704fcbb88bf4081be2fdd96d2d5edec0a9400b91ec7e39e4724cf9" width = "700" height = "400" align=center />
</div>

&nbsp; 

<div align='center'>
  <img src='./t.gif'width='700' />
</div>

&nbsp; 

### 解压PaddleGan包，并安装依赖包和ppgan


```python

#!unzip -oq ./PaddleGAN-master.zip 

pip install -r ./PaddleGAN-master/requirements.txt
python3 -m pip install --upgrade ppgan
```



### 运行脚本，运行前注意driving_video后面为视频地址，source_image为人脸地址，更改完成后运行即可


```python

cd ./PaddleGAN-master

python -u applications/tools/first-order-demo.py  \
     --driving_video ../1.mp4 \
     --source_image ../2.png \
     --relative --adapt_scale 
```



### 最后输出的地址为：`PaddleGAN-master/output`，文件夹内存放的result.mp4及迁移后的视频

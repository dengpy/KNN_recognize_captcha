# KNN_recognize_captcha
大三上学期学了机器学习之后，发现对于orc来说已经有tesseract的存在(也有python版的tesserocr库)，但是利用机器学习算法手动进行一次实践的话更能激励自己。。于是就有了这次的小项目，knn识别验证码图片
<br>
************
ps：发现自己最近真的是井喷式的什么都想干。。。。。。好累/(ㄒoㄒ)/~~痛并快乐着
*************

## 序言：传统机器学习验证码识别（深度学习的我会在 https://github.com/HELL-TO-HEAVEN/MNIST_and_CUSTOM_DATA.git 讲）我打算分为3个阶段：<br>

第一部分、简单验证码的识别（无扭曲、无遮挡、纯数字、排列整齐）<br>
第二部分、稍复杂验证码的识别（扭曲、连接、遮挡、多字符混合）<br>
第三部分、物体分类的验证码类型识别（不用神经网络的话就得用svm了）
  
======================================================================

<br>
## 第一部分：

<br>
### 说明：数据集来源：浙大教务处（下次爬爬西电的官网）
  <br>
  1、验证码数据是从浙大教务处官网爬下来的，多线程，代码也放这里。1000多张，但是因为需要手动标注，所以我只选了100张作为数据，放在data文件夹下，test文件夹放的是测试数据，选了3张；<br>
  2、代码的核心部分就是knn，我单独列出来了：simple_knn.py，写代码过程中的想法与注释都在里面了；<br>
  3、最后结果还不错，三张图片完全正确预测出来<br>
    
### 不足：
  1、验证码过于简单，局限性大；<br>
  2、最后的测试是单张图片进行的，存在偶然性，应该用一个batch进行测试，再得出精度

### 结果：
<br>这是aspx格式的测试图片：
![pic1](https://github.com/HELL-TO-HEAVEN/KNN_recognize_captcha/blob/master/test.png)
<br>
这是结果：
![pic2](https://github.com/HELL-TO-HEAVEN/KNN_recognize_captcha/blob/master/test1.png)

![pic3](https://github.com/HELL-TO-HEAVEN/KNN_recognize_captcha/blob/master/test2.png)

*****************************************************************
## 更新：
<br>
1、测试样本更多了；<br>
2、修改了一下代码；<br>
结果：精度95%上下<br>
结论：样本数据不变的情况下，随着测试数据的增多，精度会下降

![pic4](https://github.com/HELL-TO-HEAVEN/KNN_recognize_captcha/blob/master/knn_captcha.png)


========================================================================================

## 第二部分：

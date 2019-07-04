
前言：在现实生活中很少还有让我心潮澎湃的东西了，AI算一个。不仅是因为高深难懂的理论知识，或是酷炫屌炸天的的黑科技产品。而是AI能够让我们的未来生活变得更加美好~
## Infographic about the terminology of AI
[From](https://www.coursera.org/learn/ai-for-everyone/discussions/weeks/1/threads/Ugmr_DzFEemt8g6E7tChUA)   
<img width="500" src="https://github.com/lukkyy/MachinepLearning/blob/master/pic/AI.jpg">
## To do and not do
<img width="500" src="https://github.com/lukkyy/MachinepLearning/blob/master/pic/do_or_not.jpg">

### 课程
[AI For Everyone](https://www.coursera.org/learn/ai-for-everyone)
[笔记]()

### 概念
* 人工智能 
泛指让机器具有人的智力的技术。 这项技术的目的是使机器像人一样感知、 思考、 做事、 解决问题
* [机器学习]() 
指计算机通过观察环境， 与环境交互， 在吸取信息中学习、 自我更新和进步(从数据中学习)


# MachinepLearning
 基础知识：()

[机器学习笔记-模型评估](https://github.com/lukkyy/MachinepLearning/blob/master/Doc/%E6%A8%A1%E5%9E%8B%E8%AF%84%E4%BC%B0.md)   
[机器学习笔记-特征工程](https://github.com/lukkyy/MachinepLearning/blob/master/Doc/%E7%89%B9%E5%BE%81%E5%B7%A5%E7%A8%8B.md)   
[机器学习笔记-降维](https://github.com/lukkyy/MachinepLearning/blob/master/Doc/%E9%99%8D%E7%BB%B4.md) 

# DeepLearning
[目标函数、优化器、激活函数总结](https://blog.csdn.net/xiaozhuge080/article/details/52688613)
categorical_crossentropy 和 sparse_categorical_crossentropy 的区别在哪？  
如果你的 targets 是 one-hot 编码，用 categorical_crossentropy  
　　one-hot 编码：[0, 0, 1], [1, 0, 0], [0, 1, 0]
如果你的 tagets 是 数字编码 ，用 sparse_categorical_crossentropy  
　　数字编码：2, 0, 1
### loss function  

loss fuction的作用是描述model得到的结果（Y）和真实结果（y）的差异，最简单的表达就是 L=（y-Y)^2(也可y-Y) TiP:Y一般写成y^  
但这个模型不好的地方在于很难收敛：gradient descent not work well(with multiple local optima，gradient descent may not find the global optimum)    
所以针对不同的问题，有很多不同的loss function能更好的得到最优解. 比如binary crossentropy(二分类), sparse categoracial crossentropy('多分类) TiP:crossentropy交叉熵，用来描述两个数据集的相似程度的/  
loss function与cost fuction区别：loss function描述单个样本，cost fuction 描述整个样本集  
the loss function for training example and the overall cost function for the parameters of your algorithm
* [Loss function介绍](https://gombru.github.io/2018/05/23/cross_entropy_loss/)
### Gradient Descent
* [optimizer](http://www.cs.toronto.edu/~tijmen/csc321/slides/lecture_slides_lec6.pdf)

## [Computer-version](https://github.com/lukkyy/Computer-version-toturials)
## [Natural-Language-Processing](https://github.com/lukkyy/Natural-Language-Processing)

## Tool
[TensorFlow](https://github.com/lukkyy/TensorFlow_example)
[Python](https://github.com/lukkyy/Python)

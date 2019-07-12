
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
### Neural network
通常输入不算nn的层数，
神经网络的符号惯例:x表示输入特征， a表示每个神经元的输出， W表示特征的权重，上标表示神经网
络的层数 ，下标表示该层的第几个神经元。
tanh 函数是 sigmoid 的向下平移和伸缩后的结果。效果总是优于 sigmoid 函数.因为函数值域在-1 和+1
的激活函数，其均值是更接近零均值的。在训练一个算法模型时，如果使用 tanh 函数代替sigmoid 函数中心化数据，使得数据的平均值更接近 0 而不是 0.5
但有一个例外：在二分类的问题中，对于输出层，因为y的值是 0 或 1，所以想让yhat的数值介于 0 和 1 之间，而不是在-1 和+1 之间。所以需要使用 sigmoid 激活函数。
sigmoid 函数和 tanh 函数两者共同的缺点是，在z特别大或者特别小的情况下，导数的梯度或者函数的斜率会变得特别小，最后就会接近于 0，导致降低梯度下降的速度。在DNN中会出现梯度消失或者梯度爆炸的情况  
若激活函数是线性函数，那无论隐藏层是多少层，做的只是计算线性函数，所以不如直接去掉全部隐藏层
#### Neural network Dimensions
:假如训练数据有m个样本，每层的神经元有n个，z=wx+b   
则 z: (n,m)  w:(n,(n-1)) b(n,1)
Tip:W的维度是 当前层的 * 前一层 ，若相反的话要转置 ，其他参数都是 当前层 

#### why deep
* 拿图像举例，每层nn相当于特征提取器，前几层提取简单的特征（是否是直线等），后面的层数做特征组合，提取复杂的特征（如人脸轮廓）。
* 另外一个神经网络为何有效来源于电路理论，如果是一层nn，复杂度 0 (2**n)， 若是多层复杂度 0 (log(n))
### [Forward and Backward Propagation推导过程](https://www.coursera.org/learn/neural-networks-deep-learning/lecture/znwiG/forward-and-backward-propagation)
### 常见激活函数的导数
sigmoid：sigmoid=g(z),sigmoid(1 − sigmoid)
Tanh :  1-(Tanh)2
随机初始化:把偏置项b初始化为 0 是合理的,如果权重都初始化为 0，那么由于神经元（hidden units）开始计算同一个函数，而且不管你训练多久，不同的神经元计算的是同样的函数。因此这种情况下超过1个hidden units也没什么意义.  
使用tanh 或者 sigmoid 激活函数，倾向于初始化为很小的随机数。激活函数输出值很大或者很小的话，梯度下降会很慢。  
如果你没有 sigmoid/tanh 激活函数在你整个的神经网络里，就不成问题

###　超参数：需要自己设置
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

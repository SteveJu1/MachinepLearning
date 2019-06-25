# DeepLearning
[目标函数、优化器、激活函数总结](https://blog.csdn.net/xiaozhuge080/article/details/52688613)
categorical_crossentropy 和 sparse_categorical_crossentropy 的区别在哪？

如果你的 targets 是 one-hot 编码，用 categorical_crossentropy
　　one-hot 编码：[0, 0, 1], [1, 0, 0], [0, 1, 0]
如果你的 tagets 是 数字编码 ，用 sparse_categorical_crossentropy
　　数字编码：2, 0, 1

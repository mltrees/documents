# 深度学习

* 常工作的一个难点是很难知道要提取哪些特征，解决办法是使用机器学习来发掘表示本身，而不仅仅把表示映射到输出。这种方法我们称之为表示学习(representation learning)。
* 深度学习(deep learning) 通过其他较简单的表示来表达复杂表示，解决了表示学习中的核心问题。
* 深度学习让计算机通过构建较简单的概念构建复杂的概念，例如除了输入层和输出层，还有隐藏层，每个层之间都是简单的函数。
* 总体来说，深度学习将大千世界表示为层次嵌套的层次概念体系，由简单概念联系定义为复杂概念。例如对于不同颜色、不同形状的物体，通过设置颜色分层，形状分层
# tips
* 深度学习的前身是简单线性模型，给定$x_1, x_2,......x_n$，以及权重$w_1,w_2,…,w_n$，通过计算$f(x) = x_1*w_1 + x_2*w_2 + ... + x_n * w_n$得到$y$

* 线性模型和梯度下降以及随机梯度下降算法在20世纪60年代及产生，现在仍然占据主流位置。

* MLP(Multi-Layer Perception)也叫人工神经网络(Artificial Neural Network)除了输入输出，中间还有多个隐层

**softmax:** 与sigmoid类似，用于输出多个结果
$$
softmax(z)_i = \frac{exp(z_i)}{\sum_{j}{exp(z_j)}}
$$
softmax最常用作分类器的输出，来表示$n$个不同类上的概率分布
$$
\log softmax(z)_i=z_i - \log\sum_jexp(z_j)
$$
$softmax$总值为1，则一个单元值的增加必然对应着其它单元值的减小

# 附
* 深度学习简单例子[例如计算机难以理解原始感观输入数据的含义，如表示为像素值集合的图像。将一组像素映射到对象标识的函数非常复杂。如果直接处理，学习或评估此映射似乎是不可能的。深度学习将所需的复杂映射分解为一系列嵌套的简单映射(每个由模型的不同层描述)来解决这一难题。输入展示在可见层(visible layer)，这样命名的原因是因为它包含我们能观察到的变量。然后是一系列从图像中提取越来越多抽象特征的隐藏层(hidden layer)。因为它们的值不在数据中给出，所以将这些层称为“隐藏层”;模型必须确定哪些概念有利于解释观察数据中的关系。这里的图像是每个隐藏单元表示的特征的可视化。给定像素，第1层可以轻易地通过比较相邻像素的亮度来识别边缘。有了第1隐藏层描述的边缘，第2隐藏层可以容易地搜索可识别为角和扩展轮廓的边集合。给定第2隐藏层中关于角和轮廓的图像描述，第3隐藏层可以找到轮廓和角的特定集合来检测特定对象的整个部分。最后，根据图像描述中包含的对象部分，可以识别图像中存在的对象(经Zeiler and Fergus(2014)许可引用此图)]
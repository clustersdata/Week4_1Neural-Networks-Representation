# Week4_1Neural-Networks-Representation
Week4_1Neural Networks Representation
# Week4_1Neural-Networks-Representation
Week4_1Neural Networks Representation
# Week4_1Neural-Networks-Representation
Week4_1Neural Networks Representation
第 1 题
Which of the following statements are true? Check all that apply.

The activation values of the hidden units in a neural network, with the sigmoid activation function applied at every layer, are always in the range (0, 1).
Any logical function over binary-valued (0 or 1) inputs x1x1 and x2x2 can be (approximately) represented using some neural network.
A two layer (one input layer, one output layer; no hidden layer) neural network can represent the XOR function.
Suppose you have a multi-class classification problem with three classes, trained with a 3 layer network. Let a(3)1=(hΘ(x))1 be the activation of the first output unit, and similarly a(3)2=(hΘ(x))2a2(3)=(hΘ(x))2 and a(3)3=(hΘ(x))3a3(3)=(hΘ(x))3. Then for any input x, it must be the case that a(3)1+a(3)2+a(3)3=1a1(3)+a2(3)+a3(3)=1.
*     答案: 1 2 * 
* 选项1: sigmoid激励层的取值范围都是(0-1). 正确 ** 
* 选项2: logical function有四种操作:AND OR XOR NOT. 其中两层的Network可以表示出AND OR NOT这三类,三层Network可以表示出XOR. 正确 ** 
* 选项3: 要实现xor操作须要有一个hidden layer. 不正确 ** 
* 选项4: 计算三个分类中每一个分类的期望,最理想的情况才会出现类似1 0 0 0这种. 不正确 **

第 2 题
Consider the following neural network which takes two binary-valued inputs x1,x2∈{0,1}x1,x2∈{0,1} and outputs hΘ(x)hΘ(x). Which of the following logical functions does it (approximately) compute? 


OR
AND
NAND (meaning “NOT AND”)
XOR (exclusive OR) 
*     答案: 1 * 
* hθ=g(−20+30x1+30x2)hθ=g(−20+30x1+30x2) *
x1x1	x2x2	hθhθ
0	0	0
1	0	1
0	1	1
1	1	1
* 只要有一个为1,就为True, 这不就是OR嘛 *

第 3 题
Consider the neural network given below. Which of the following equations correctly computes the activation a(3)1a1(3)? Note: g(z)g(z) is the sigmoid activation function. 
 
* a(3)1=g(Θ(2)1,0a(2)0+Θ(2)1,1a(2)1+Θ(2)1,2a(2)2)a1(3)=g(Θ1,0(2)a0(2)+Θ1,1(2)a1(2)+Θ1,2(2)a2(2)) 
* a(3)1=g(Θ(1)1,0a(1)0+Θ(1)1,1a(1)1+Θ(1)1,2a(1)2)a1(3)=g(Θ1,0(1)a0(1)+Θ1,1(1)a1(1)+Θ1,2(1)a2(1)) 
* a(3)1=g(Θ(1)1,0a(2)0+Θ(1)1,1a(2)1+Θ(1)1,2a(2)2)a1(3)=g(Θ1,0(1)a0(2)+Θ1,1(1)a1(2)+Θ1,2(1)a2(2)) 
* The activation a(3)1a1(3) is not present in this network.

*     答案: 1 * 
* a(3)1a1(3) 是第3层的第1个激活单元=第2层的ΘΘ 乘以 第2层的a * 
* 第2层的ΘΘ就是Θ2Θ2 * 
* 第2层的aa就是a2a2 *

第 4 题
You have the following neural network: 
 
You’d like to compute the activations of the hidden layer a(2)∈R3a(2)∈R3. 
One way to do so is the following Octave code: 
 
You want to have a vectorized implementation of this (i.e., one that does not use for loops). Which of the following implementations correctly compute a(2)a(2)? Check all that apply.

z = Theta1 * x; a2 = sigmoid (z);
a2 = sigmoid (x * Theta1);
a2 = sigmoid (Theta2 * x);
z = sigmoid(x); a2 = sigmoid (Theta1 * z);
*     答案: 1 * 
* 选项2: sigmoid是最后一步, 同时是先 Theta1*x, 再sigmoid(z) **

第 5 题
You are using the neural network pictured below and have learned the parameters Θ(1)=[1111.72.43.2]Θ(1)=[112.411.73.2] (used to compute a(2)) and Θ(2)=[10.3−1.2]Θ(2)=[10.3−1.2] (used to compute a(3)a(3) as a function of a(2)a(2)). 
Suppose you swap the parameters for the first hidden layer between its two units so Θ(1)=[111.713.22.4]Θ(1)=[11.73.2112.4] and also swap the output layer so Θ(2)=[1−1.20.3]Θ(2)=[1−1.20.3]. How will this change the value of the output hΘ(x)hΘ(x)? 


It will stay the same.
It will increase.
It will decrease
Insufficient information to tell: it may increase or decrease.
*     答案: 1 * 
**     当交换Θ(1)Θ(1)中的两行时,实际上就是交换了a(2)2a2(2) 与 a(2)3a3(2), 
原先是 a(2)1∗0.3a1(2)∗0.3+a(2)2∗(−1.2)a2(2)∗(−1.2) 现在变为$a_2^{(2)}(-1.2)+a_1^{(2)}*0.3$$ 没什么区别 *

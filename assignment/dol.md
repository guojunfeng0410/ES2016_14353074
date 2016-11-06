#Lab2: DOL实例分析&编程
####任务1.修改example2,让3个square模块变成2个, tips:修改xml的iterator
修改解释：已经知道该实验有三个基本模块:generator、square、consumer。其中generator依次产生1至19的数，square对数进行平方处理，consumer输出结果，而example2.xml则是使用这三个模块产生逻辑运算。让3个square模块变成2个，观察examle2.xml代码。

修改example2.xml中代码:
>variable value="3" name="N"

为
>variable value="2" name="N"

使得square的迭代次数从三变为二。

重新编译运行
>ant –f runexample.xml –Dnumber=2

得到结果:

![alt text](https://github.com/guojunfeng0410/picture/blob/master/lab2_example2_picture1.JPG?raw=true "result")

观察example2.dot
![alt text](https://github.com/guojunfeng0410/picture/blob/master/lab2_example2_picture2.JPG?raw=true "result")

####任务2.修改example1，使其输出3次方数，tips:修改square.c
修改解释：已经知道该实验有三个基本模块:generator、square、consumer。其中generator依次产生1至19的数，square对数进行平方处理，consumer输出结果，而example1.xml则是使用这三个模块产生逻辑运算。修改example1.xml，使其输出3次方数.
修改
>i=i*i

为
>i=i*i *i

重新编译运行
>ant –f runexample.xml –Dnumber=1

得到结果:

![alt text](https://github.com/guojunfeng0410/picture/blob/master/lab2_example1_picture1.JPG?raw=true "result")

观察example1.dot
![alt text](https://github.com/guojunfeng0410/picture/blob/master/lab2_example1_picture2.JPG?raw=true "result")

#实验感想
本次试验是DOL实例分析&编程，在这次实验中可以看到一个具体的dol程序包含各个进程以及一个系统架构定义这些模块的连接方式，我们学习这些模块的运行方式并且修改它们的代码，从而加深了对它们的了解。

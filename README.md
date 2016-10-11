#DOL配置
---
####Description
>  Distributed operation layer (DOL) is a software development framework to program parallel applications. The DOL allows to specify applications based on the Kahn process network model of computation and features a simulation engine based on SystemC. Moreover, the DOL provides an XML-based specification format to describe the implementation of a parallel application on a multi-processor systems, including binding and mapping.
  
![](https://raw.githubusercontent.com/guojunfeng0410/picture/master/6.JPG)
####How to install

#####Install necessary enviroment
 
 > $ sudo apt-get update

 >$  sudo apt-get install ant 

 > $ sudo apt-get install openjdk-7-jdk

 > $ sudo apt-get install unzip
 
#####Download file 
> $ sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip

#####Unzip file
1.Create folder of dol
>$  mkdir dol
  
2.Unzip dolethz.zip into dol 
> $ unzip dol_ethz.zip -d dol

 3.Unzip system.c
 >$ tar -zxvf systemc-2.3.1.tgz
 
#####Compile system.c
1.Enter folder systemc-2.3.1 
> $ cd systemc-2.3.1

2.Creat a temporary folder objdir
> $ mkdir objdir

3.Enter folder objdir
>$ cd objdir

4.Execute configure(used to set parameter for compile)
>$ ../configure CXX=g++ --disable-async-updates

![](https://raw.githubusercontent.com/guojunfeng0410/picture/master/1.jpg)

5.Compile
>$ sudo make install

6.Check file in folder systemc-2.3.1 after compiled
>$ cd   ..

> $ ls

![](https://raw.githubusercontent.com/guojunfeng0410/picture/master/2.jpg)

7.Remember present working directory for subsequent step
>pwd  

##### Dol
1.Enter folder of dol
>$ cd .../dol

2.Change build_zip.xml.Find following words and then substitute the previous result of command pwd for YYY 
>property name="systemc.inc" value="YYY/include"
property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"

3.Compile 
>$ ant-f build_zip.xml.all

4.try to run first example
>$ cd build/bin/main
>ant-f runexample.xml -Dnumber=1

![](https://raw.githubusercontent.com/guojunfeng0410/picture/master/5.jpg)


---
####Experimental experience 
在实验中遇到困难，失败的时候不要灰心，慢慢找资料，多尝试，最后会成功的。

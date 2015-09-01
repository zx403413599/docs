:title: any problems of linux
:author: Lennart Regebro
:description: The Hovercraft! tutorial.




----

编程外的思考
====

* 有没有更好的安装方式呢？我的这种安装方式是否有问题？有的话请告诉我。（很多依赖包我采用pip和easy_install都无法安装，感觉是pip配置文件配置源的问题）
* 一定要看官方的文档，Google和百度出来的结果往往是碎片化的，不全面。这样可以少走很多弯路，减少不必要的工作量。
* 遇到的问题要先思考，想想是什么问题再Google和百度。
* 解决问题要形成文档，方便自己也方便别人。

----

linux安装anaconda
===================

1. 先去官网安装 anaconda3

2. bash 路径/文件名.sh  进行安装

3. 将anaconda3/bin 加入永久环境变量 

    * export PATH=$PATH:/home/wangjianlong/anaconda3/bin
	
	* vi /etc/profile 最后面加入 export PATH=$PATH:/home/wangjianlong/anaconda3/bin
	
	* source /etc/profile
	
	* 开启另外一个终端 输入python 看是否成功
	
4. 若机器已经安装过python 则去除软连接 rm /usr/bin/python

5. 建立软连接 sudo ln -s /your anaconda3 file/bin/python3 /usr/bin/python

6. 端输入 python 看是否已经连接成功

7. 使用pip install package_name(如requests） 下载第三方库 若下载不了 
将anaconda/bin/pip 复制到 /usr/bin  替换该文件夹下的pip 需要授予/usr/bin 777权限 也要授予/usr/bin/pip 777权限'

8. 替换完成后 使用pip install requests 测试是否可以下载 完成。

----

:data-scale: 3 

:data-rotate-z: -90

:data-x: r3000

:data-y: r3000

共享文件夹
===========

1. 安装功能增强包

2. 设置共享文件夹 自动挂载

3. cd 要共享的文件夹目录下 

4. sudo mount -t vboxsf windows_file linux_file

----

安装Virtualenv with Virtualenvwrapper
=====================================

links- Virtualenvwrapper

.. _links: http://virtualenvwrapper.readthedocs.org/en/latest/ 

text_link- Virtualenv with Virtualenvwrapper

.. _text_link: http://roundhere.net/journal/virtualenv-ubuntu-12-10/

workon 虚拟空间名字

deativate 退出虚拟空间名字

----

wins py2与Py3共存下虚拟环境
=============================

# install
pip install virtualenvwrapper-win
# mk virtualenv dir
mkvirtualenv --python=F:\softs\python2\python.exe p2  （安装在zx403413599 env文件目录下）
# use
workon p2
# pip
pip install tornado


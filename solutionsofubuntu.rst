:title: any problems of linux
:author: Lennart Regebro
:description: The Hovercraft! tutorial.

----

linux��װanaconda
===================

1. ��ȥ������װ anaconda3

2. bash ·��/�ļ���.sh  ���а�װ

3. ��anaconda3/bin �������û������� 

    * export PATH=$PATH:/home/wangjianlong/anaconda3/bin
	
	* vi /etc/profile �������� export PATH=$PATH:/home/wangjianlong/anaconda3/bin
	
	* source /etc/profile
	
	* ��������һ���ն� ����python ���Ƿ�ɹ�
	
4. �������Ѿ���װ��python ��ȥ�������� rm /usr/bin/python

5. ���������� sudo ln -s /your anaconda3 file/bin/python3 /usr/bin/python

6. ������ python ���Ƿ��Ѿ����ӳɹ�

7. ʹ��pip install package_name(��requests�� ���ص������� �����ز��� 
��anaconda/bin/pip ���Ƶ� /usr/bin  �滻���ļ����µ�pip ��Ҫ����/usr/bin 777Ȩ�� ҲҪ����/usr/bin/pip 777Ȩ��'

8. �滻��ɺ� ʹ��pip install requests �����Ƿ�������� ��ɡ�

----

:data-scale: 3 

:data-rotate-z: -90

:data-x: r3000

:data-y: r3000

�����ļ���
===========

1. ��װ������ǿ��

2. ���ù����ļ��� �Զ�����

3. cd Ҫ������ļ���Ŀ¼�� 

4. sudo mount -t vboxsf windows_file linux_file

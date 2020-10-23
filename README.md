# WeChatDat

#### 介绍
微信dat文件批量解析



#### 使用说明

1.  基于python3.7
2.  安装binascii，datetime
3.  python Wechat.py

###
dat文件和源图片文件就是用某个数按字节异或了一下，异或回来就可以了，
A ^ B = C
B ^ C = A
A ^ C = B
假设png文件头是A，dat文件是C，用A和C文件头的字节异或就可以得出B，因
为图片的格式以png，jpg，gif为主，通过这三种文件格式的头两个字节和待
转换文件的头两个字节一一异或的结果相等就找到B了，同时也知道了文件的
格式

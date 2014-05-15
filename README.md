脚本集合
===
自己写的或者收集的一些实用的linux下的脚本    
待更新...    
===
####dump\_via\_ssh
用来抓包的，手机上需要装tcpdump和openssh，android就得root，iphone得越狱，然后保证可以访问到手机，然后用下面的命令：    

    dump_via_ssh -i interface_name ip_addr    
    
-i 后面是interface，大概就是网卡名称，不知道的话可以用ip命令看一下    
    
    ip addr
    
大概会得到类似的信息    

    1: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP qlen 100
    link/ether xx:xx:xx:xx:xx:xx brd ff:ff:ff:ff:ff:ff
    inet 172.16.1.160/24 brd 172.16.1.255 scope global wlan0
    inet6 fe80::da50:e6ff:fe2b:c947/64 scope link 
       valid_lft forever preferred_lft forever

那个wlan0就是    
ip_addr就是手机的ip地址    
运行后第一次应该会问是否链接，输入yes就行，就是ssh第一次连接的时候都会问的那个，然后输入密码，现在用的是root用户，以后再加上用户密码的参数吧，不过感觉手机上一般也就用root用户    
没什么问题的话wireshark就会起来了    
===   
####load\_modules\_for\_genymotion   
加载运行genymotion模拟器需要的模块   


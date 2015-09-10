# thibkphp-memcached

ThinkPHP Seesion的Memcached驱动支持阿里云OCS及集群

1.检测环境是否安装memcached扩展 注意是memcached 不是 memcache
php -m

如果出现memcached就可以了 
当然你也可以用phpinfo(); 查看
如果没有的那就是安装了 具体方法我就不说了 大家可以百度下
别忘了在php.ini里面
memcached.use_sasl = 1
分号去掉，没有的话就复制此行
别忘了安装完成后重启下php


2.下载扩展文件
复制到/ThinkPHP/Library/Think/Session/Driver 目录下

3.编写配置文件

    'MEMCACHE_HOST'=>'1.ocs.aliyuncs.com', //连接地址
    'MEMCACHE_PORT'=>'11211',    //端口
    'MEMCACHE_USERNAME'=>'username',   //用户名
    'MEMCACHE_PASSWORD'=>'password',   //密码
    'SESSION_TYPE'=>'Memcached',       //名称

以上配置中（地址，端口，用户名，密码）如果你是多个服务器你可以用英文的,号隔开
好了 以上配置就完成了，尽情享受吧。

title: Shadowsocks配置
date: 2015-07-28 15:12:32
tags: [工具,翻墙]
---

### 安装服务端: 
sudo pip install shadowsocks

==========================


### 服务端配置: 
<pre><code>
vim /etc/shadowsocks.json

{
    "server":"xx.xx.xx.xx",
    "server_port":8388,
    "password":"xxxxxxxxxx",
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}


启动:ssserver -c /etc/shadowsocks.json
后台启动:ssserver -c /etc/shadowsocks.json -d start
关闭:ssserver -c /etc/shadowsocks.json -d stop
开机启动把命令写入/etc/rc.local文件里
</code></pre>

==========================


### 客户端win:
<a href="https://github.com/shadowsocks/shadowsocks-windows">点击这里下载客户端</a>
然后打开按里面的界面配置就好了

==========================


### 客户端linux：
安装: sudo pip install shadowsocks
<pre><code>
vim /etc/shadowsocks.json

{
    "server":"xx.xx.xx.xx",
    "server_port":8388,
    "password":"xxxxxxxxxxxx",
    "local_address": "127.0.0.1",
    "local_port":1080,
    "timeout":300,
    "method":"aes-256-cfb",
    "fast_open": false
}

启动:sslocal -c /etc/shadowsocks.json
后台启动:sslocal -c /etc/shadowsocks.json -d start
关闭:sslocal -c /etc/shadowsocks.json -d stop
开机启动把命令写入/etc/rc.local文件里
</code></pre>

==========================

### SwitchySharp配置(只有linux需要,win直接全局代理就好了)
只填SOCKS 代理那行，127.0.0.1:1080
并且选择SOCKS v5

==========================

### linux下命令行使用shadowsocks(proxychains)
安装: apt-get install proxychains
只把[ProxyList]下面的socks4那行删掉改成

<pre><code>
[ProxyList]
socks5  127.0.0.1 1080
</code></pre>

不要按官方的说明改，反正我按官方的改不行
附:<a href="https://github.com/shadowsocks/shadowsocks/wiki/Using-Shadowsocks-with-Command-Line-Tools">官方说明</a>

=========================

测试下是否可用: 

<pre><code>
proxychains curl http://www.twitter.com
</code></pre>
    



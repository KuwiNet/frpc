## Frpc客户端管理脚本
Frp 是一个高性能的反向代理应用，可以帮助您轻松地进行内网穿透，对外网提供服务，支持 tcp, http, https 等协议类型，并且 web 服务支持根据域名进行路由转发。

* 详情：fatedier (https://github.com/fatedier/frp)</br>
* 脚本原作者：clangcn (https://github.com/clangcn/onekey-install-shell)</br>
* 本脚本完全使用MvsCode(https://github.com/MvsCode/frps-onekey )的frps.init代码修改而成，供frpc使用。

### 操作方法
#### 一、安装Frpc客户端
~~~bash
wget -N https://raw.githubusercontent.com/KuwiNet/frpc/master/frpc_install.sh
chmod 755 frpc_install.sh
./frpc_install.sh
~~~
#### 二、下载frpc.init移动到/etc/init.d/frpc并赋权
~~~bash
wget -N https://raw.githubusercontent.com/KuwiNet/frpc/master/frpc.init
mv frpc.init /etc/init.d/frpc
chmod 755 /etc/init.d/frpc
~~~
#### 三、安装快捷命令
##### Debian/Ubuntu
~~~bash
update-rc.d -f frpc defaults
ln -s /etc/init.d/frpc /usr/bin/frpc
~~~
##### CentOS/Redhat
~~~bash
chkconfig --add frpc
~~~
#### 四、启动Frpc、查看状态
~~~bash
frpc start
~~~
~~~bash
frpc status
~~~

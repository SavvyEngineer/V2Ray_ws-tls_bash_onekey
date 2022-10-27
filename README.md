## V2Ray based on Nginx 的 vmess+ws+tls 一论 install script

> Thanks to JetBrains for the license

> Thanks for non-commercial open source development authorization by JetBrains
### About VMess MD5 authentication information filtering mechanism
> 自 2022 年 1 月 1 日起，电影端将电影电影电影电影MD5电影的上海的下载。 Any client using MD5 authentication information will not be able to connect to the server that disables VMess MD5 authentication information.

Affected users, we strongly recommend that you reinstall it, and set alterid to 0 (the current default value has been changed to 0), and no longer use the VMess MD5 authentication mechanism.
If you don't want to reinstall, you can enable MD5 authentication mechanism by using https://github.com/KukiSa/VMess-fAEAD-disable

### Telegram group
* Telegram: https://t.me/wulabing_v2ray
* Telegram update public channel: https://t.me/wulabing_channel

### Preparation work
* Prepare a domain name and add a record.
* [V2ray official description](https://www.v2ray.com/), understand TLS WebSocket and V2ray related information
* Install wget

### Installation/update method
Vmess+websocket+TLS+Nginx+Website
```
wget -N --no-check-certificate -q -O install.sh "https://raw.githubusercontent.com/wulabing/V2Ray_ws-tls_bash_onekey/master/install.sh" && chmod +x install.sh && bash install .sh
```

VLESS+websocket+TLS+Nginx+Website
```
wget -N --no-check-certificate -q -O install.sh "https://raw.githubusercontent.com/wulabing/V2Ray_ws-tls_bash_onekey/dev/install.sh" && chmod +x install.sh && bash install .sh
```

### Attention
* If you don't understand the specific meaning of the script, except the domain name, please use the default value provided by the script
* 使用本设计可以你可以Linux电影可以电影，可以本电视的电影，在线设计电视
* Currently supporting Debian 9+ / Ubuntu 18.04+ / Centos7+, some Centos templates may have difficult to handle compilation problems, it is recommended that when you encounter compilation problems, please replace them with other template systems
* 群主 only provides extremely limited support, if there is a problem you can ask 群友
* Every week at 3 points, Nginx will restart automatically in conjunction with the signing of the certificate. During this time, the node will not be able to connect normally.

### Update log
> Update content Please view CHANGELOG.md

### 鸣谢
* ~~本第一季的可以天生电影（Use Host） 第二： https://github.com/dylanbai8/V2Ray_ws-tls_Website_onekey Please select according to your needs~~ The author can be stopped maintaining
* 本设计中 MTProxy-go TLS version project reference https://github.com/whunt1/onekeymakemtg Thank you whunt1
* 本设计中輔速4合1官方原地地地址 https://www.94ish.me/1635.html Thank you
* 本设计中輔速4合1最作管理版 Project Reference https://github.com/ylx2016/Linux-NetSpeed ​​Thank you ylx2016

### Certificate
> If you already have the certificate file of your domain name, you can rename the crt and key file to v2ray.crt v2ray.key and place it in /data directory (the directory does not exist), please note the certificate file permissions及结果时间期，电影结果时间期过期后请请自行所输

The script supports automatic generation of let's encrypted certificate, valid for 3 months, theory, automatic generation of certificate, supports automatic renewal

### View client configuration
`cat ~/v2ray_info.txt`

### V2ray Introduction

* V2Ray is an excellent open source network agent tool, it can help you enjoy the Internet experience, and it currently supports the use of Windows, Mac, Android, IOS, Linux and other operating systems on all platforms.
* This script is a complete script configuration, and after all the processes have been run normally, it can be used directly according to the output of the client
* Please note: We still strongly recommend that you fully understand the entire program's working flow and principles

### It is recommended to set up a single server only
* The default script to install the latest version of V2ray core
* V2ray core current latest version is 4.22.1 (at the same time, please pay attention to the client core's synchronization update, need to guarantee the client's kernel version >=服务端 kernel version)
* It is recommended to use the default 443 port as the connection port
* Fake contents can be replaced by yourself.

### Attention
* It is recommended to use this script in a pure environment, if you are new, please do not use Centos system.
* Please do not use this program in the production environment before trying to make this script really usable.
* This program relies on Nginx to realize relevant functions, please use [LNMP](https://lnmp.org) or other similar Nginx scripts. Users who have installed Nginx scripts should be especially careful. ，若方式，电影电影电影 may deal with this problem).
* Some functions of V2Ray depend on the system time, please ensure that you use the system of V2RAY program UTC time error within three minutes, the time zone is irrelevant.
* 本 bash depends on [V2ray official installation script](https://install.direct/go.sh) 及 [acme.sh](https://github.com/Neilpang/acme.sh) 工作。
* Centos system user please run the related program in the firewall in advance (Default: 80, 443)


### Start mode

Start V2ray: `systemctl start v2ray`

Stop V2ray: `systemctl stop v2ray`

Start Nginx: `systemctl start nginx'

Stop Nginx: `systemctl stop nginx'

### Related directory

Web directory: `/home/wwwroot/3DCEList`

V2ray服务端设计：`/etc/v2ray/config.json`

V2ray client configuration: `~/v2ray_info.inf`

Nginx Directory: `/etc/nginx`

Certificate document: `/data/v2ray.key 和 /data/v2ray.crt`

### donation

You can use 我的放瓦工 AFF 费利VPS

https://bandwagonhost.com/aff.php?aff=63939

You can use the proxy provided by my justmysocks AFF 贪头恡瓦工

https://justmysocks.net/members/aff.php?aff=17621

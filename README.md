# 概述
该cms集成一般网站基础的部件，可以作为建站的通用基础摩卡。包括：
* 登录，注册，找回密码
* 第三方登录（微博，QQ，微信等）
* 用户信息修改
* 后台管理
* 权限分配

# 安装说明
>* git
```shell
git clone https://github.com/echoOly/ttcms.git
```
>* 克隆下来后，使用composer初始化~
```shell
composer install
```
>* 文设置件目录权限
```
chmod -R  777 data storage install config
```
>* Download
https://github.com/echoOly/ttcms/releases
下载的zip档案是进过composer初始化后的包，可以直接解压使用，无需使用composer初始化，如果需要升级，请执行
```shell
composer update
```

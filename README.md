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
下载的zip档案是进过composer初始化后的包，导入数据库/data/database/*, 可以直接解压使用，无需使用composer初始化，如果需要升级，请执行
```shell
composer update
```
部门配置

# 数据库说明
表名|描述|调用方式
----|------|-----
online_stats|在线用户统计|通用
online_logs|在线记录|通用
online|在线用户|通用
system_config|后台各页面设置项配置|model('Xconfig')
x_log|日志信息 |LogRecord - model('Logs')
schedule|计划任务|和通常的计划任务不同，App框架初始化唤醒，现在有用户在线统计使用。慎用！
system_data|系统性的配置|model('Xdata')
navi|导航 头部底部|model('Navi')
invite_code|邀请码|model('Invite')
sensitive_word|过滤词|通用
sensitive_category|过滤词分类|通用
credit_type|积分类型|通用
credit_setting|积分规则|通用
credit_record|积分记录|通用
credit_user|用户积分信息|model('Credit')
area|地区|树形地区 model('CategoryTree')->setTable('area')
permission_node|节点权限|通用
permission_group|应用组内权限|通用
usr_profile|用户资料，入学年份，学历等，可以定制|通用
user_profile_setting|用户资料分类，可以多个层级|通用
usr_category|用户标签，多级|通用
user_category_link|用户-用户标签关联|通用
user_verified_category|用户认证类型|通用
user_verified|用户认证|通用
denounce|举报信息|model('denounce')
addon|插件信息|model('addon')
feedback|用户反馈|通用
application_slide|轮播图|通用
tag|标签|model('Tag')
app_tag|应用|用户 - 标签关系表|model('Tag')

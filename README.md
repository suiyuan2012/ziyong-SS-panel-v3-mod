1.安装宝塔面面板，PHP版本选择7.1，其他默认，使用Nginx环境。

2.新建站点，记住域名。

3.新建数据库，记住数据库用户和密码，（宝塔面板默认数据库名=用户名）。



配置PHP( 宝塔用户 )

宝塔用户可能会在超过某一数量节点的时候出现 Undefined offset :0 in 你的网站路径 这个错误， 这个问题会导致后端无法进行连接，可以按照以下方法解决

在宝塔面板中找到php，点击设置

在禁用函数一栏找到 system proc_open proc_get_status 去除它

在性能调整中，把 PHP 运行模式设置为 静态

在配置修改中 按 Ctrl+F 搜索 display_errors = 改为 Off 后保存

4.运行下面的脚本：

      wget https://raw.githubusercontent.com/suiyuan2012/ziyong/master/install.sh; bash install.sh


三分钟左右安装完，安装之后没有默认管理员，切换到/www/wwwroot/网站里面去，记住，到根目录即可。然后执行下面一行添加管理员（输入用户名，密码，然后输入Y确认即可）：

php xcat createAdmin //创建管理员

下面这些建议也执行一次：

php xcat syncusers //同步用户

php xcat initQQWry //下载IP解析库

php xcat resetTraffic //重置流量

php xcat initdownload //下载ssr程式

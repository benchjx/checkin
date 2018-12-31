# checkin--------------广州、深圳、上海、北京等地三网。

https://www.hostloc.com/thread-505027-1-1.html

本帖最后由 bot 于 2018-12-20 22:32 编辑


之前看到loc有个网友分享的用良心云还是哪个云的方法，才想起来也可以用travis-ci

https://github.com/fakedon/checkin

1.fork我的项目，下一步
   或者上传你自己的签到脚本到github，需要有.travis.yml文件，并在文件内设置运行签到的命令
2.注册https://travis-ci.org/，可通过github一键注册
3.访问https://travis-ci.org/account/repositories，Repositories里找到你的项目，x点成√
4.点settings，Environment Variables下Name填hostloc_username和hostloc_password，Value 填 你的帐号 和 密码
5.Cron Jobs 设置成 daily

完成。
脚本没有问题的话就能每天正常签到了




2018.12.20 更新loc签到脚本，支持多账号签到，环境变量（Environment Variables）格式改为hostloc_username_0, hostloc_password_0, hostloc_username_1, hostloc_password_1...

PS。用户名/密码是填在travis-ci的环境变量里，并不会暴露密码，github中并没有密码信息
因为签到任务依托于travis-ci，任务调用并不是定时执行，可以在一天中的任何时候，这个取决于网站的任务调配，有时两次执行间隔差不多有48个小时

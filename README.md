2018年8月/
太理教务助手第一版，实现了太原理工大学教务处常用功能的第三方查询（成绩、校历、排名等）。提供Web和微信小程序两个版本
-----------------------------------------------------
2018年9月/
实现免VPN、课表查询功能，将后台设计成API的形式，实现前后端分离。微信小程序暂未更新
-----------------------------------------------------
2018年10月25日/
新增免验证码功能，新增教务处通知解析
-----------------------------------------------------
2018年10月30日/
使用Django完成重构，后台从Java环境迁移到Python环境，提供稳定的免VPN环境。
-----------------------------------------------------

关于免VPN： 
1、基于Ubuntu，在Docker内运行校园网VPN程序，固定容器的IP地址（Docker Hub搜索仓库auchandirect/forticlient） 2、定义IP路由容器到教务处IP（202.207.247.44 via 172.20.0.2 |202.207.247.60 via 172.20.0.2） 3、VPN的登录态会失效，可以编写脚本，利用Crontab来定时任务，定时重启VPN容器（0 0 * * * /usr/bin/python3 /opt/task/vpn.py &）
-----------------------------------------------------
关于免验证码： 
图像识别，可以自己手写，可以基于百度云或者腾讯云的第三方图像识别API
-----------------------------------------------------
微信小程序还在完善中，暂未更新...
-----------------------------------------------------

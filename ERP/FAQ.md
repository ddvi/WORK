![]()
#### 1-服务器内网ip变更，erp服务器需要如何处理
1）修改为固定ip地址
右击右下角网络图标，打开网络和共享中心
![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvz4mm17oj308m04f3yy.jpg)
进入NIC1进行配置调整
![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvz777z4tj30ip0apacb.jpg)
确认网络通常后进入下一步
2）确定SystemControl，scktsvr两个服务都处于启动状态,查看右下角是否有这两个图标
![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvzb4hqwyj30dq07o0th.jpg)
如果没有，点击桌面上如下两个快捷方式进行启动
![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvzdqchlkj308i07idh1.jpg)
3）修改客户端IP地址
    打开易飞erp快捷方式所在文件目录，
   ![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvzfnxokmj30bc0fd77w.jpg)   
    打开上一层目录，最下面找到YiFeiConfig，双击修改为服务器当前ip地址
   ![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvzggk1z5j30t10krtk9.jpg)
   ![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvzgy00s8j30mz04ygnv.jpg)

   完成后依次点击
    test connect db
                test systemcontrols
                test connect  需要输入密码 为服务器密码
                都成功后点击ok
   ![](http://ww1.sinaimg.cn/large/005Lei8Jly1gdvzjb2og7j30lg0e7435.jpg)
   
4. 修改h3c公网映射配置
打开H3C管理界面，
192.168.1.1
输入密码并登陆
注：必须使用ie浏览器否则某些配置如端口映射可能无法调整
依次点击高级设置=》地址转换=》虚拟服务器
双击操作下的编辑图标
211 81 8088 8089 1433 212 213
端口对应的内网服务其ip均需要调整为当前服务器内网IP

5.修改每台电脑erp配置
打开易飞erp快捷方式所在文件目录，打开上一层目录，最下面找到YiFeiConfig，双击修改为服务器当前ip地址

ERP就可以正常使用了

END
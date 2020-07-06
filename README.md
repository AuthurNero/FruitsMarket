# FruitsMarket
## 水果超市特性:

###  一、客户端

客户端可多开， 支持账号注册，自动将本地操作日志发送到服务端。

​	1.客户端连接服务器失败会尝试重连三次，一直失败就退出。

​	2.客户端实时同步信息，每一步操作同步一次信息。

#### 顾客:	

​	1.查看水果 。

​	2.选购水果加购物车，加购完库存会减少， 数据同步。

​	3.购物车结算，按满减优惠价格计算，退出客户端后购物车依然保存。

#### 管理员:	

​	1.可对水果数据进行增删改查，实时同步。

​	2.可对用户进行增删改查，实时同步。

​	3.添加水果时，如果出现同种水果，自动叠加。

​	4.删除水果或者账号时，二次确认。

#### 用户注册:	

​	1.会员注册，账号实时同步。

​	2.管理员注册，需要从服务端获取秘钥，正确后创建管理员。

​	3.创建账号时密码二次确认再创建。

​	4.账号和密码只允许6-15位的英文或者数字。

### 二、服务端

​	1.实时打印配置拉取和更新日志，显示时间和操作IP。

​	2.实时日志打印并保存到服务器log.txt文件。

​	3.当被请求管理员秘钥时，打印秘钥。

​	4.四个端口作用：发送数据端口、接收数据端口、发送秘钥端口、接收日志端口。

​	5.四线程同时进行，同时监听。



#### 已知BUG：

​	1.打印列表不对齐问题

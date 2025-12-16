# E-commerce_log_offline_analysis_system
![image](images/1751104939283.jpg)
### 技术框架

| 产品       | 版本号    |
| ---------- | --------- |
| 服务器系统 | CentOS7.9 |
| Java JDk   | jdk-8     |
| Zookeeper  | 3.5.7     |
| Nginx      | 1.20.1    |
| Hadoop     | 3.1.3     |
| Hive       | 3.1.2     |
| HBase      | 2.0.5     |
| Sqoop      | 1.4.6     |
| MySQL      | 5.7.28    |

###  测试服务器规划

| node1 | hadoop, hbase, mysql, nginx, flume    |
| ----- | ------------------------------------- |
| node2 | hadoop, hbase, zookeeper              |
| node3 | hadoop, hbase, zookeeper, hive, sqoop |
| node4 | hadoop, hbase,zookeeper               |

### 数据参数说明

| 参数名称 | 类型   | 描述                                                         |
| -------- | ------ | ------------------------------------------------------------ |
| en       | string | 事件名称, eg: e_pv                                           |
| ver      | string | 版本号, eg: 0.0.1                                            |
| pl       | string | 平台, eg: website，ios,android                               |
| sdk      | string | Sdk类型, eg: js、java                                        |
| b_rst    | string | 浏览器分辨率，eg: 1920*1080                                  |
| b_iev    | string | 浏览器信息（userAgent），火狐控制台输入：window.navigator.userAgent，示例："Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:76.0) Gecko/20100101 Firefox/76.0" |
| u_ud     | string | 用户/访客唯一标识符                                          |
| l        | string | 客户端语言                                                   |
| u_mid    | string | 会员id，和业务系统一致                                       |
| u_sd     | string | 会话id                                                       |
| c_time   | string | 客户端时间                                                   |
| p_url    | string | 当前页面的url                                                |
| p_ref    | string | 上一个页面的url                                              |
| tt       | string | 当前页面的标题                                               |
| ca       | string | Event事件的Category名称                                      |
| ac       | string | Event事件的action名称                                        |
| kv_*     | string | Event事件的自定义属性                                        |
| du       | string | Event事件的持续时间                                          |
| oid      | string | 订单id                                                       |
| on       | string | 订单名称                                                     |
| cua      | string | 支付金额                                                     |
| cut      | string | 支付货币类型                                                 |
| pt       | string | 支付方式                                                     |

### 例子：Launch事件

| **方法名称** | **onLaunch**                                                 |
| ------------ | ------------------------------------------------------------ |
| 发送的数据   | u_sd=8E9559B3-DA35-44E1-AC98-85EB37D1F263&c_time=1449137597974&ver=1&en=e_l&pl=website&sdk=js&b_rst=1920*1080&u_ud=12BF4079-223E-4A57-AC60-C1A04D8F7A2F&b_iev=Mozilla%2F5.0%20(Windows%20NT%206.1%3B%20WOW64)%20AppleWebKit%2F537.1%20(KHTML%2C%20like%20Gecko)%20Chrome%2F21.0.1180.77%20Safari%2F537.1&l=zh-CN |
| 参数说明     | u_sd=8E9559B3-DA35-44E1-AC98-85EB37D1F263 会话id<br />c_time=1449137597974 客户端时间<br />ver=1 版本<br />en= e_l  事件的名称 e_l<br />pl=website 平台<br />sdk=js sdk类型<br />b_rst=1920*1080 客户端屏幕的分辨率<br />u_ud=12BF4079-223E-4A57-AC60-C1A04D8F7A2F 访客的标识<br />b_iev=Mozilla%2F5.0%20(Windows%20NT%206.1%3B%20WOW64)%20AppleWebKit%2F537.1%20(KHTML%2C%20like%20Gecko)%20Chrome%2F21.0.1180.77%20Safari%2F537.1 浏览器信息<br />l=zh-CN 客户端的语言 |



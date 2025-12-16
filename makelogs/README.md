# E-commerce_log_offline_analysis_system
### 项目搭建

1.新建JavaWeb项目New Project

2.选择maven webapp项目

![image](..\images\ee253f4a-f5e6-4ebe-a516-122c6f6e60ca.png)

3.填写项目有关信息

4.配置maven

5.点击Finish，加载项目

6.在pom.xml文件中添加flume依赖

<dependency> 

​	<groupId>org.apache.flume</groupId>

​	<artifactId>flume-ng-auth</artifactId>

​	<version>1.9.0</version>

</dependency>

7.为项目Modules配置Web

![image](..\images\e2260035-5f3c-40a0-85d3-84be24692279.png)

发现当前项目的Modules下已经存在Web配置了，则可以跳转到下一步

![image](..\images\95bd8468-4a89-4d41-a530-79b5ab395c18.png)

8.配置artifact

![image](..\images\ab9e21f5-c328-4da6-9031-1523a6baaa24.png)

### 配置Tomcat

1.IDEA项目Encoding设置

![image](..\images\439adc6f-81f5-44e2-8bf5-4f4811b0d761.png)

2.安装解压Tomcat到一个位置

3.配置Tomcat

![image](..\images\Snipaste_2025-12-16_11-16-15.png)

点击local后：

![image](..\images\Snipaste_2025-12-16_11-18-01.png)

安装上图标识的步骤依次点击。文件路径选择你按照的Tomcat所在位置

4.进入如下界面后配置artifacts

![image](..\images\Snipaste_2025-12-16_11-21-53.png)

![image](..\images\Snipaste_2025-12-16_11-22-51.png)

![image](..\images\Snipaste_2025-12-16_11-24-49.png)

![image](..\images\Snipaste_2025-12-16_11-25-37.png)

5.点击Server选项检查，配置可以使用

![image](..\images\Snipaste_2025-12-16_11-26-57.png)

点击apply，然后点击OK

6.启动项目，测试http://localhost:8080/

![image](..\images\Snipaste_2025-12-16_11-28-44.png)

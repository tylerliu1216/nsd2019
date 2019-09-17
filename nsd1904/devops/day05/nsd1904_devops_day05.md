# nsd1904_devops_day05

CI：持续集成，jenkins是最为流行的CI工具

CD：持续交付

软件开发部署流程

```mermaid
graph LR
dev(程序员)--推送-->git(gitlab)
jen(jenkins)--拉取-->git
app(应用服务器)--下载-->jen
```

## jenkins应用

安装：jenkins是java编写的程序。jenkins在安装过程中，需要访问互联网。

```shell
[root@node6 ~]# rpm -ihv jenkins-2.177-1.1.noarch.rpm 
[root@node6 ~]# systemctl start jenkins
[root@node6 ~]# systemctl enable jenkins
```

初始化：

访问http://192.168.4.6:8080 -> 在安装插件页面，选择“选择插件来安装” -> 点击“无”，不安装插件 -> 在“创建第一个管理员帐户”页面，点击右下角“使用admin账户继续” -> 进入到管理页面后，点击右上角的“admin” -> 左侧configure，该页面内修改密码

配置插件：使用国内镜像站点

首页 -> Manage Jenkins -> Manage Plugins -> Advanced -> Update Site: https://mirrors.tuna.tsinghua.edu.cn/jenkins/updates/update-center.json -> submit 

安装插件：Available -> Localization: Chinese (Simplified) / Git Parameter -> Install without restart -> Restart Jenkins when installation is complete and no jobs are running





















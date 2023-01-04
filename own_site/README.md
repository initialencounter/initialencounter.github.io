
# 在手机上搭建个人网站
应群友要求，出一期在Android手机上搭建个人网站教程
我们这个网站是以hopweb的PHP做后端，cpolar内网穿透。
搭建成功以后，可以在外网访问

## 需要用到的工具

### 网站后台--hopweb
[hopweb](https://atreep.netlify.app/hopweb/)

### 内网穿透工具--极点云cpolar
[cpolar](https://www.cpolar.com/)

### 运行cpolar的容器ZeroTermux
[ZeroTermux](https://github.com/hanxinhao000/ZeroTermux)


## 搭建流程

### 1. hopweb环境配置
1.1 给hopweb后台运行的权限

1.2 修改端口
打开hopweb>>右上角设置面板>>PHP环境配置>>将PHP服务端口修改为5700

1.3 新建web项目
打开hopweb>>创建项目>>确定>>打开新建的项目

### 2. ZeroTermux环境配置
2.1 授予ZeroTermux后台运行的权限

2.2 更新termux
```shell
pkg upgrade
```

2.3 安装wget
```shell
pkg install wget
```

2.4 下载cpolar
```shell
wget https://static.cpolar.com/downloads/releases/3.3.12/cpolar-stable-linux-arm.zip
```

2.5 解压cpolar
```shell
unzip cpolar-stable-linux-arm.zip
```

### 3. 部署

3.1 注册cpolar
进入cpolar官网[cpolar](https://www.cpolar.com/)>>免费使用>>创建账号

3.2 配置cpolar
复制命令粘贴到termux>>回车

3.3 启动服务
```shell
./cpolar 5700
```

3.4 查看地址
浏览器输入http://localhost:4040

## 退出

4.1 停止服务

打开termux>>输入Ctrl+C

4.2 退出termux

```shell
exit
```

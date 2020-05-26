#### docker 的好处
1. 安装软件时省去环境变量的配置
2. 可拉取自己镜像，在不同机器上跑

#### win10 下安装Docker
* 过程
1. 下载 [DockerToolbox.exe](https://get.daocloud.io/toolbox/)(我下载的版本为 DockerToolbox-19.03.1.exe)       
2. 执行上述 exe 文件后，在 Docker Toolbox 目录下(ds)用 Git Bash 执行 start.sh（之所以没用 Quick Start 是因为我出现了闪退问题）
```
start sh
```
3. 我们会得到一个IP地址，以后会用到
4. 使用[加速器](https://www.jianshu.com/p/2aa5b05717c6)

#### 概念
* 镜像(image)
* 容器(container)通过镜像运行起来的实例
> 通过镜像运行起来的进程
* 仓库(reposity)
> 专门存放镜像的地方


#### command
* docker version:查看 docker 版本
* docker-machine ip:查看 ip 地址
* docker pull tomcat:拉取 tomcat 镜像
* docker image ls:查看已拉取到的镜像
* docker ps:查看进程
* docker run xxx:开启容器
* docker rm xxx:删除容器

#### Docker daemon
```
docker run hello-world
```
1. 接受 Docker client 讯息"本地没有 hello-world 镜像"
2. 从 Docker Hub 中拉取 hello-world 镜像
3. 创造容器，以运行相关进程
4. 将结果输出至 Docker client


#### Docker 安装 mysql
1. 拉取 mysql 镜像
```
 docker run --name mysql1 -e MYSQL_ROOT_PASSWORD=123456 -p 3306:3306 -d mysql:8.0.28
```
2. 进入容器的 linux 环境(这一步不能用 git bash，必须用 cmd)
```
docker exec -it mysql1 bash
```
3. 登录
```
mysql -u root -p
```
接下来会提醒你输入密码，输入 123456 后就进入 mysql 了

#### 在本机登录 mysql
1. 开启被关闭的 container:直接在 cmd 中执行
```
docker start mysql1
```
2. 进入 mysql 命令行环境
```
docker exec -it mysql1 bash
```
3. 登录
```
mysql -u root -p
```


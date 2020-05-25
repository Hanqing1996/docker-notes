## win10 下安装Docker
* 过程
1. 下载 [DockerToolbox.exe](https://get.daocloud.io/toolbox/)(我下载的版本为 DockerToolbox-19.03.1.exe)       
2. 执行上述 exe 文件后，在 Docker Toolbox 目录下用 Git Bash 执行 start.sh（之所以没用 Quick Start 是因为我出现了闪退问题）
```
start sh
```
3. 我们会得到一个IP地址

#### 
* 镜像(image)
> 
* 容器(container)通过镜像运行起来的实例
> 通过镜像运行起来的进程
* 仓库(reposity)
> 专门存放镜像的地方


#### command
* docker version:查看 docker 版本
* 

#### Docker daemon(-D 指的就是 daemon)
```
docker run hello-world
```
1. 接受 Docker client 讯息"本地没有 hello-world 镜像"
2. 从 Docker Hub 中拉取 hello-world 镜像
3. 创造容器，以运行相关进程
4. 将结果输出至 Docker client

# caffe 环境配置
## 1. 安装好UBUNTU系统 （我使用UBUNTU20）
## 2. 下载安装驱动
- NVIDIA 驱动地址 [nvidia driver](https://www.nvidia.cn/geforce/drivers/)

## 3. 安装docker
- [docker 安装](https://docs.docker.com/engine/install/ubuntu/)
- 安装完后输入 docker -version 查看是否成功
- 安装toolkit
- 输入
 
```
curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | \
  sudo apt-key add -
distribution=$(. /etc/os-release;echo $ID$VERSION_ID)
curl -s -L https://nvidia.github.io/nvidia-docker/$distribution/nvidia-docker.list | \
  sudo tee /etc/apt/sources.list.d/nvidia-docker.list
sudo apt-get update
```

然后安装

`sudo apt-get install -y nvidia-container-toolkit`

重启docker 

`systemctl restart docker`

## 下载镜像
`docker pull nvcr.io/nvidia/caffe:20.03-py3`

## 创建容器
`sudo docker run --gpus all -it 容器ID /bin/bash`






# Window 
- WSL1不支持
- Docker桌面版会强制安装到C盘
- 可以直接在WSL2里像在Linux里安装一样
- 尽量把文件放在WSL发行版文件系统里，一可以提高性能，二减少一些兼容性问题的出现(毕竟WSL与Window的文件系统还是不一样的)

# WSL2 安装Docker
参考https://zhuanlan.zhihu.com/p/148511634
## Install
```
curl -fsSL https://get.docker.com -o get-docker.sh
//sleep20s
sudo sh get-docker.sh
sudo service docker start
```
## Check 
```
service docker status
ps aux|grep docker
```
## Pull Test
```
docker pull busybox
docker images
```
> 注意：不同于完全linux虚拟机方式，WLS2下通过apt install docker-ce命令安装的docker无法启动，因为WSL2方式的ubuntu里面没有systemd。上述官方get-docker.sh安装的docker，dockerd进程是用ubuntu传统的init方式而非systemd启动的。

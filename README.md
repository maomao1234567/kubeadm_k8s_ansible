# kubeadm_k8s_ansible
使用Ansible自动化运维工具，使用Kubeadm部署k8s集群。
## 准备多个虚拟机
我在实验过程中部署了PXE网络自动化安装CENTOS7的功能，可以通过网络自动安装虚拟机。主要是安装并配置了DHCP、TFTP、HTTP服务。 分别用来分配IP， 提供安装引导文件、内核文件，以及安装应答文件、必要的软件包。
## 初始化虚拟机安装k8s的系统环境
这个过程主要是对虚拟机做一些安装k8s集群前的系统初始化的操作，比如将关闭selinux, 防火墙服务，配置虚拟网卡配置将其改为静态IP, 关闭NetworkManager服务，并且重启网络服务。修改HOSTNAME, 修改yum源的配置信息，安装docker，以及kubelet。

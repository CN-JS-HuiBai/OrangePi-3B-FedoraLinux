##FedoraLinux38 For OrangePi 3B镜像存储仓库##
这里是用于存储FedoraLinux 38（Linux-6.6-MainLine内核） OrangePi 3B的镜像仓库，
该镜像目前已经可以提供UWE5622网卡的支持(蓝牙似乎没有正常运行)，但镜像默认不启用该部分模块，您可以通过以下命令启用：
  modprobe lib80211
  modprobe cfg80211
  modprobe sprdwl_ng
目前已知的问题有：
  1、dnf -y update之后会安装FedoraLinux官方6.5.x的内核，该内核无法启动，原因尚且不明，请在执行完该命令之后，手动将默认内核切换为6.6.0内核
  2、设置模块自动加载，在更新内核版本后，可能会出现无法正确加载WIFI驱动的问题，原因尚且不明，在排查结束后会修复改漏洞
该镜像默认使用的root账户的密码为orangepi
该镜像额外的管理员账户用户名为orangepi密码为orangepi

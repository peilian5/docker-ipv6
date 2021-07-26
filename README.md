# docker-ipv6




docker启用ipv6方法




docker engine 的版本大于等于20.10.2，因为这个版本才开始支持ip6tables。



正式开始：

编辑 /etc/docker/daemon.json ，加上以下内容。（如果没有这个文件直接创建。）

{
  "ipv6": true,
  "fixed-cidr-v6": "fd00::/80",
  "experimental": true,
  "ip6tables": true
}



重启docker ：

sudo systemctl restart docker

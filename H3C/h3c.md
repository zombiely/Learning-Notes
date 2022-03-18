```shell
（1）键入以下命令，创建VLAN2并进入其视图。
<H3C> system-view
[H3C] vlan 2
（2）键入以下命令，指定VLAN 2的描述字符串为home。
[H3C-vlan2] description home
（3）键入以下命令，向VLAN2中加入端口Ethernet2/0/1和Ethernet2/0/2。
[H3C-vlan2] port Ethernet 2/0/1 Ethernet 2/0/2
（4）键入以下命令，创建VLAN 3并进入其视图。
[H3C-vlan2] vlan 3
（5）键入以下命令，向VLAN3中加入端口Ethernet2/0/3和Ethernet2/0/4。
[H3C-vlan3] port Ethernet 2/0/3 Ethernet 2/0/4
示例2：
-----------------------------------
H3C交换机基于端口VLAN的配置示例
https://blog.51cto.com/winda/30568


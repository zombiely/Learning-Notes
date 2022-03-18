* **PPTP需开放端口：**
UDP:1723

* **L2TP需开放端口：**
UDP:500
UDP:4500
UDP:1701  
*注意：端口映射时应该将协议设置为UDP，否则无法生效*

GRE（Generic Routing Encapsulation）通用路由封装：是对某些网络层协议（如IP和IPX）的报文进行封装，使这些被封装的报文能够在另一网络层协议（如IP）中传输。GRE可以作为第三层隧道协议，在协议层之间采用隧道（Tunnel）技术。Tunnel是一个虚拟的点对点的连接，可以看成仅支持点对点连接的虚拟接口，这个接口提供了一条通路，使封装的数据报能够在这个通路上传输，并在一个Tunnel的两端分别对数据报进行封装及解封装。  
我们使用两台AR28进行互联，并在之间创建GRE最简单的隧道。互联拓扑图如下：  
AR28-31<++++++++++>AR28-31

```bash
【AR28-1】
# 
sysname AR28-1 
# 
interface Ethernet2/0 
ip address 202.101.1.2 255.255.255.0 /公网IP/ 
# 
interface Ethernet2/1 
ip address 192.168.1.1 255.255.255.0 //内部私网IP 
# 
interface Tunnel0 //创建GRE隧道 tunnel 0 
ip address 192.168.0.1 255.255.255.252 // tunnel IP和对方tunnel IP在同一网段 
source 202.101.1.2 //GRE隧道源地址 
destination 202.101.2.2 //GRE隧道目的地址 
# 
ip route-static 0.0.0.0 0.0.0.0 202.101.1.1 preference 60 
//到公网的默认路由 
ip route-static 192.168.2.0 255.255.255.0 Tunnel 0 preference 60 
//通过tunnel访问对方私网的路由 
# 
【AR28-2】 
# 
sysname AR28-2 
# 
interface Ethernet2/0 
ip address 202.101.2.2 255.255.255.0 //内部私网IP 
# 
interface Tunnel0 //创建tunnel 0 
ip address 192.168.0.2 255.255.255.252 //tunnel IP和对方tunnel IP在同一网段 
source 202.101.2.2 /源地址 
destination 202.101.1.2 //目的地址 
# 
ip route-static 0.0.0.0 0.0.0.0 202.101.2.1 preference 60 
//到公网的默认路由 
ip route-static 192.168.1.0 255.255.255.0 Tunnel 0 preference 60 
//通过tunnel访问对方私网的路由

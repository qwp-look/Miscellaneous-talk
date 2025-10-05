# 公网中转端配置指南

我们选择使用阿里云的公网服务器，主要是因为其价格便宜（68元/年）。

- **服务器信息**：
  - 系统：Windows 2022 数据中心版
  - 配置：2vCPU，内存2GiB，ESSD云盘40GiB，公网宽带200Mbps
  - [阿里云官网](https://www.aliyun.com/)

## 配置步骤

### 1. 使用 nps 替代 frp

原方案使用 [frp](https://github.com/fatedier/frp)，但由于配置问题未成功，改用 [nps](https://github.com/ehang-io/nps)。

### 2. 登录 nps 控制台

1. 登录公网服务器，访问 `http://<你的公网IP>:8080`。
2. 默认用户名和密码：`admin` / `123`。
3. 登录后进入客户端页面，点击“新建客户端”，保持默认设置。

   ![nps 客户端页面](nps.PNG)

4. 点击加号查看“客户端启动命令”：

   ```bash
   ./npc.exe -server=xx.xx.xx.xx:8024 -vkey=xxxxx -type=tcp
   ```

### 3. 配置 npc

1. 在运行 MC-server 的服务器上安装 npc。
2. 下载 [nps release](https://github.com/ehang-io/nps/releases)。
3. 解压后找到 `npc.conf` 文件并进行配置。
```test
   示例配置：
[common]
server_addr=xx.xx.xx.xx:8024
conn_type=tcp
vkey=xxxxxxxxxxxxxxxxxxxxx
auto_reconnection=true
crypt=true
compress=true
disconnect_timeout=60

[moonlight1]
mode=tcp
target_addr=127.0.0.1:47984
server_port=47984

[moonlight2]
mode=tcp
target_addr=127.0.0.1:47987
server_port=47987

[moonlight3]
mode=tcp
target_addr=127.0.0.1:47984
server_port=47984

[moonlight4]
mode=tcp
target_addr=127.0.0.1:48010
server_port=48010

[moonlight5]
mode=udp
target_addr=127.0.0.1:47998
server_port=47998

[moonlight6]
mode=udp
target_addr=127.0.0.1:47999
server_port=47999

[moonlight7]
mode=tcp
target_addr=127.0.0.1:47989
server_port=47989

[moonlight8]
mode=udp
target_addr=127.0.0.1:48000
server_port=48000

[minecraft]
mode=tcp
target_addr=127.0.0.1:25565
server_port=25565

```
4. 在 nps 网页控制端的客户端页面，点击“隧道”，根据 `npc.conf` 添加隧道。

   示例：

   ![隧道配置示例]({DA4FEC78-964D-4DE7-8B27-E8C0D7ED3E4C}.png)

### 4. 启动 npc

1. 打开解压后的文件夹。
2. 在地址栏输入 `powershell.exe`。
3. 在弹出的窗口中输入启动命令：

   ```bash
   ./npc.exe -server=xx.xx.xx.xx:8024 -vkey=xxxxx -type=tcp
   ```

至此，网络传输配置完成。
# 控制端配置指南

## 1. 安装 Moonlight

1. 在控制端安装 [Moonlight](https://github.com/moonlight-stream/moonlight-qt)。
2. 手动添加中转服务器的公网 IP。
3. 在 MC-server 端打开 Sunshine，输入 PIN 码即可连接，之后无需再次验证。

## 2. 文件管理工具选择

我们选择使用 [Alist](https://github.com/AlistGo/alist)。

### 安装步骤

1. 在 MC-server 端安装 Alist。
2. 解压下载的文件，得到可执行文件：

   ```bash
   unzip alist-xxxx.zip
   ```

3. 运行程序：

   ```bash
   .\alist.exe server
   ```

4. 获得管理员信息：

   - **低于 v3.25.0 版本**：

     ```bash
     .\alist.exe admin
     ```

   - **高于 v3.25.0 版本**：

     - 随机生成一个密码：

       ```bash
       .\alist.exe admin random
       ```

     - 手动设置一个密码（`NEW_PASSWORD` 是你需要设置的密码）：

       ```bash
       .\alist.exe admin set NEW_PASSWORD
       ```

5. 登录你的 Alist，进行管理。
6. 添加存储，完成配置。

   示例：

   ![Alist 配置示例]({F538AA1C-718C-4B7F-B99A-7C0E84712922}.png)

至此，文件管理工具配置完成。
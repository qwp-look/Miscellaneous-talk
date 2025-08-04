# MC 服务器运行端配置指南

## 1. 运行软件选择

我们选择使用 [MCSManager](https://github.com/MCSManager/MCSManager)，它可以方便地运行 MC 服务器。

### 安装步骤

1. 安装 [Git](https://git-scm.com/)。

2. 克隆 MCSManager 仓库并安装依赖：

   ```bash
   git clone https://github.com/MCSManager/MCSManager.git
   ./install-dependents.bat
   ./npm-dev-windows.bat
   ```

3. 创建账号并创建实例。

## 2. 游戏核心选择

我们选择使用 [Arclight](https://github.com/IzzelAliz/Arclight)。

### 安装步骤

1. 参考以下文档完成安装：
   - [Arclight 安装文档](https://wiki.izzel.io/s/arclight-docs/doc/installation-0ian14HIpu)
   - [MCSManager Java 版设置文档](https://docs.mcsmanager.com/setup_java_edition.html)

2. 点击运行即可。

> **注意**：过程中可能会有少量报错，只要不影响运行即可忽略。

## 3. 配置管理软件

我们选择使用 [Sunshine](https://github.com/LizardByte/Sunshine)。

### 系统要求

#### 最低要求

| 组件      | 要求                                                                 |
|-----------|----------------------------------------------------------------------|
| GPU       | AMD: VCE 1.0 或更高，详见 [obs-amd 硬件支持](https://github.com/obsproject/obs-amd-encoder/wiki/Hardware-Support) |
|           | Intel: Linux: VAAPI 兼容，详见 [VAAPI 硬件支持](https://www.intel.com/content/www/us/en/developer/articles/technical/linuxmedia-vaapi.html)<br>Windows: Skylake 或更新版本，支持 QuickSync 编码 |
|           | Nvidia: NVENC 启用的显卡，详见 [NVENC 支持矩阵](https://developer.nvidia.com/video-encode-and-decode-gpu-support-matrix-new) |
| CPU       | AMD: Ryzen 3 或更高<br>Intel: Core i3 或更高                          |
| 内存      | 4GB 或更多                                                           |
| 操作系统  | Windows: 10+ (Windows Server 不支持虚拟手柄)<br>macOS: 13+<br>Linux/Debian: 12+ (bookworm)<br>Linux/Fedora: 40+<br>Linux/Ubuntu: 22.04+ (jammy) |
| 网络      | 主机: 5GHz, 802.11ac<br>客户端: 5GHz, 802.11ac                        |

#### 4K 建议

| 组件      | 要求                                                                 |
|-----------|----------------------------------------------------------------------|
| GPU       | AMD: Video Coding Engine 3.1 或更高                                  |
|           | Intel: Linux: HD Graphics 510 或更高<br>Windows: Skylake 或更新版本，支持 QuickSync 编码 |
|           | Nvidia: GeForce GTX 1080 或更高                                      |
| CPU       | AMD: Ryzen 5 或更高<br>Intel: Core i5 或更高                          |
| 网络      | 主机: CAT5e 以太网或更好<br>客户端: CAT5e 以太网或更好               |

#### HDR 建议

| 组件      | 要求                                                                 |
|-----------|----------------------------------------------------------------------|
| GPU       | AMD: Video Coding Engine 3.4 或更高                                  |
|           | Intel: HD Graphics 730 或更高                                        |
|           | Nvidia: Pascal 架构 GPU (GTX 10 系列) 或更高                         |
| CPU       | AMD: Ryzen 5 或更高<br>Intel: Core i5 或更高                          |
| 网络      | 主机: CAT5e 以太网或更好<br>客户端: CAT5e 以太网或更好               |

### 安装步骤

1. 下载 [Sunshine release](https://github.com/LizardByte/Sunshine/releases)。

2. 安装并创建账号即可。
# MPET - Multi-Protocol Exploitation Toolkit
![](https://socialify.git.ci/onewinner/MPET/image?custom_language=Go&description=1&font=Inter&forks=1&issues=1&language=1&logo=&name=1&owner=1&pulls=1&stargazers=1&theme=Auto)
<div align="center">


<div align="center">
    <h3>MPET (Multi-Protocol Exploitation Toolkit)——多协议漏洞利用与攻击模拟平台</h3>
</div>

[功能特性](#-功能特性) • [快速开始](#-快速开始) • [使用指南](#-使用指南) • [支持协议](#-支持的协议) • [截图展示](#-截图展示)

</div>

---

## 📖 项目简介

MPET (Multi-Protocol Exploitation Toolkit) 是一款专业的多协议安全测试工具，基于 Wails 框架构建的现代化桌面应用。它提供了对 25+ 种主流服务协议的连接测试、未授权访问检测、弱口令检测和漏洞利用能力，是安全研究人员和渗透测试工程师的得力助手。

### 🎯 核心优势

- **🚀 高效批量**: 支持 CSV、Fscan、Lightx 等多种格式批量导入，支持拖拽上传
- **🔍 智能检测**: 自动识别导入结果的未授权访问和弱口令漏洞
- **📊 可视化报告**: 一键导出 Markdown 格式漏洞报告，支持自动生成漏洞截图
- **🎨 现代界面**: Vue 3 + Ant Design Vue 打造的精美 UI
- **🔐 代理支持**: 内置 SOCKS5 代理，支持认证
- **💾 数据管理**: SQLite 数据库存储，支持漏洞信息自定义
- **🌐 跨平台**: 一次构建，Windows/Linux/macOS 全平台运行

## ✨ 功能特性

### 核心功能

- ✅ **多协议支持**: 覆盖 25+ 种主流服务协议（数据库、文件传输、消息队列、容器编排等）
- ✅ **智能导入**: 支持 CSV、Fscan 1.8.4、Fscan 2.1.1、Lightx 结果文件自动识别和导入
- ✅ **批量操作**: 批量导入、批量连接、批量删除、批量导出
- ✅ **未授权检测**: 自动检测 Redis、MongoDB、Docker、Kubernetes 等服务的未授权访问
- ✅ **弱口令检测**: 自动识别扫描工具结果中的弱口令，支持自定义凭据测试
- ✅ **命令执行**: SSH、Docker、Kubernetes 容器命令执行
- ✅ **文件浏览**: FTP、SFTP、SMB 文件浏览和下载
- ✅ **远程桌面**: VNC、RDP 屏幕截图获取
- ✅ **实时监控**: 实时显示连接状态和详细日志
- ✅ **漏洞报告**: 自动生成 Markdown 格式漏洞报告，包含截图和修复建议
- ✅ **漏洞管理**: 内置漏洞信息库，支持自定义编辑

### 高级特性

- 🔧 **代理穿透**: 全局 SOCKS5 代理配置，支持代理认证
- 🎨 **主题切换**: 亮色/暗色主题自由切换
- 📋 **多格式导入**: 支持 CSV、Fscan、Lightx 等多种格式自动识别
- 🎯 **拖拽上传**: 直接拖拽文件到窗口即可导入，无需点击按钮
- 🔍 **智能解析**: 自动识别未授权访问和弱口令，无需手动标注
- 🔄 **自动刷新**: 实时更新连接状态
- 🎯 **智能筛选**: 按类型、IP、用户名、状态、消息内容筛选
- 📊 **分页展示**: 支持自定义每页显示数量
- 🖼️ **截图导出**: 自动截取连接详情用于报告生成

## 🔌 支持的协议

### 数据库服务 (9种)

| 协议 | 默认端口 | 检测能力 | 特殊功能 |
|------|---------|---------|---------|
| **Redis** | 6379 | 未授权访问、弱口令 | 命令执行、数据读取 |
| **MySQL** | 3306 | 弱口令 | 数据库查询 |
| **PostgreSQL** | 5432 | 弱口令 | 数据库查询 |
| **SQL Server** | 1433 | 弱口令 | 数据库查询 |
| **Oracle** | 1521 | 弱口令 | 多服务名尝试 |
| **MongoDB** | 27017 | 未授权访问、弱口令 | 数据库操作 |
| **Memcached** | 11211 | 未授权访问 | 缓存读取 |
| **Elasticsearch** | 9200 | 未授权访问 | API 调用、数据查询 |
| **Etcd** | 2379 | 未授权访问 | 配置读取 |

### 文件传输服务 (4种)

| 协议 | 默认端口 | 检测能力 | 特殊功能 |
|------|---------|---------|---------|
| **FTP** | 21 | 未授权访问、弱口令 | 文件浏览、下载 |
| **SFTP** | 22 | 弱口令 | 文件浏览、下载 |
| **SMB** | 445 | 未授权访问、弱口令 | 共享浏览、文件下载 |
| **SSH** | 22 | 弱口令 | 命令执行、文件操作 |

### 远程管理服务 (3种)

| 协议 | 默认端口 | 检测能力 | 特殊功能 |
|------|---------|---------|---------|
| **RDP** | 3389 | 弱口令 | 屏幕截图 |
| **VNC** | 5900 | 未授权访问、弱口令 | 屏幕截图 |
| **WMI** | 135 | 弱口令 | Windows 管理 |

### 消息队列服务 (3种)

| 协议 | 默认端口 | 检测能力 | 特殊功能 |
|------|---------|---------|---------|
| **RabbitMQ** | 5672 | 弱口令 | 消息队列操作 |
| **MQTT** | 1883 | 未授权访问、弱口令 | 消息订阅发布 |
| **Kafka** | 9092 | 未授权访问 | 消息队列操作 |

### 容器与编排服务 (2种)

| 协议 | 默认端口 | 检测能力 | 特殊功能 |
|------|---------|---------|---------|
| **Docker** | 2375 | 未授权访问 | 容器管理、命令执行 |
| **Kubernetes** | 8080/10250 | 未授权访问 | Pod 管理、命令执行 |

### 其他服务 (4种)

| 协议 | 默认端口 | 检测能力 | 特殊功能 |
|------|---------|---------|---------|
| **Zookeeper** | 2181 | 未授权访问 | 配置读取 |
| **ADB** | 5555 | 未授权访问 | Android 设备管理 |
| **JDWP** | 8000 | 未授权访问 | Java 调试 |
| **RMI** | 1099 | 未授权访问 | Java 远程调用 |

## 🏗️ 技术架构

### 后端技术栈

- **语言**: Go 1.22+
- **框架**: Wails v2.11
- **数据库**: SQLite (modernc.org/sqlite - 纯 Go 实现)
- **协议库**: 
  - Redis: go-redis/redis
  - MySQL: go-sql-driver/mysql
  - PostgreSQL: lib/pq
  - MongoDB: mongo-driver
  - SSH: golang.org/x/crypto/ssh
  - Docker: docker/docker/client
  - Kubernetes: k8s.io/client-go
  - 等 25+ 种专用客户端库

### 前端技术栈

- **框架**: Vue 3.4 (Composition API)
- **语言**: TypeScript 5.2
- **UI 库**: Ant Design Vue 4.0
- **构建工具**: Vite 4.5
- **状态管理**: Pinia 2.1
- **图标**: Ant Design Icons
- **截图**: html2canvas

### 项目结构

```
MPET/
├── backend/                          # 后端 Go 代码
│   ├── app.go                       # Wails 应用主类
│   ├── config/                      # 配置管理
│   │   └── config.go               # 配置加载和保存
│   ├── handlers/                    # 请求处理器
│   │   ├── command.go              # 命令执行处理
│   │   ├── connection.go           # 连接管理处理
│   │   ├── file.go                 # 文件操作处理
│   │   ├── import.go               # 导入处理
│   │   ├── proxy.go                # 代理配置处理
│   │   └── report.go               # 报告生成处理
│   ├── models/                      # 数据模型
│   │   ├── connection.go           # 连接模型
│   │   └── vulnerability.go        # 漏洞信息模型
│   ├── parsers/                     # 结果解析器
│   │   ├── csv.go                  # CSV 解析器
│   │   ├── fscan.go                # Fscan 1.8.4 解析器
│   │   ├── fscan21.go              # Fscan 2.1.1 解析器
│   │   └── lightx.go               # Lightx 解析器
│   └── services/                    # 业务逻辑
│       ├── connector.go            # 连接服务核心
│       ├── database.go             # 数据库操作
│       ├── logger.go               # 日志服务
│       ├── report.go               # 报告生成服务
│       ├── vulnerability.go        # 漏洞信息服务
│       └── connectors/             # 协议实现
│           ├── service.go          # 连接器注册
│           ├── redis.go            # Redis 连接器
│           ├── mysql.go            # MySQL 连接器
│           ├── docker.go           # Docker 连接器
│           ├── kubernetes.go       # Kubernetes 连接器
│           └── ... (25+ 协议实现)
├── frontend/                         # 前端 Vue 代码
│   ├── src/
│   │   ├── assets/                 # 静态资源
│   │   │   └── icons/              # 服务图标
│   │   ├── components/             # 组件
│   │   │   ├── TitleBar.vue        # 自定义标题栏
│   │   │   ├── FTPFileBrowser.vue  # FTP 文件浏览器
│   │   │   ├── DockerShellModal.vue # Docker Shell 弹窗
│   │   │   └── VulnerabilityModal.vue # 漏洞信息管理
│   │   ├── composables/            # 组合式函数
│   │   │   ├── useConnections.ts   # 连接管理
│   │   │   ├── useCommand.ts       # 命令执行
│   │   │   ├── useImport.ts        # 导入功能
│   │   │   ├── useProxy.ts         # 代理配置
│   │   │   ├── useReport.ts        # 报告导出
│   │   │   └── ...
│   │   ├── stores/                 # 状态管理
│   │   │   └── theme.ts            # 主题管理
│   │   ├── utils/                  # 工具函数
│   │   │   ├── constants.ts        # 常量定义
│   │   │   ├── formatters.ts       # 格式化工具
│   │   │   └── parsers.ts          # 解析工具
│   │   ├── views/                  # 页面
│   │   │   └── Home.vue            # 主页面 (1500+ 行)
│   │   ├── App.vue                 # 根组件
│   │   └── main.ts                 # 入口文件
│   └── wailsjs/                    # Wails 自动生成
├── data/                            # 数据目录
│   └── connections.db              # SQLite 数据库
├── reports/                         # 报告输出目录
├── config.json                      # 配置文件
├── example.csv                      # CSV 示例文件
├── app.go                          # Wails 应用入口
├── main.go                         # 主程序
├── wails.json                      # Wails 配置
└── go.mod                          # Go 依赖
```

## 🚀 快速开始

### 环境要求

- **Go**: 1.22 或更高版本
- **Node.js**: 18.0 或更高版本
- **pnpm**: 8.0 或更高版本
- **Wails CLI**: v2.11 或更高版本

### 安装 Wails CLI

```bash
# macOS/Linux
go install github.com/wailsapp/wails/v2/cmd/wails@latest

# Windows
go install github.com/wailsapp/wails/v2/cmd/wails@latest
```

### 克隆项目

```bash
git clone https://github.com/onewinner/MPET.git
cd MPET
```

### 安装依赖

```bash
# 安装 Go 依赖
go mod download

# 安装前端依赖
cd frontend
pnpm install
cd ..
```

### 开发模式

```bash
# 启动开发服务器（支持热重载）
wails dev
```

### 构建应用

```bash
# Windows (64位)
wails build -platform windows/amd64

# Linux (64位)
wails build -platform linux/amd64

# macOS (通用二进制)
wails build -platform darwin/universal

# macOS (ARM64 - Apple Silicon)
wails build -platform darwin/arm64

# macOS (AMD64 - Intel)
wails build -platform darwin/amd64
```

构建完成后，可执行文件位于 `build/bin/` 目录。

## 📖 使用指南

### 1. 添加连接目标

#### 方式一：手动添加

1. 点击顶部工具栏的 **"添加"** 按钮
2. 在弹出的对话框中：
   - 选择服务类型（自动填充默认端口）
   - 填写 IP 地址
   - 填写端口（可选，使用默认端口）
   - 填写用户名（可选，留空尝试未授权访问）
   - 填写密码（可选）
3. 点击 **"测试连接"** 按钮验证配置
4. 点击 **"确定"** 保存并自动开始连接测试

#### 方式二：扫描工具结果导入

MPET 支持自动识别和导入主流扫描工具的结果文件，无需手动转换格式。

**支持的工具**：

1. **Fscan 1.8.4**
   - 格式：`[+] Redis:192.168.1.100:6379 unauthorized`
   - 格式：`[+] MySQL:192.168.1.101:3306 root:password123`
   - 自动识别未授权访问和弱口令

2. **Fscan 2.1.1**
   ```
   # ===== 漏洞信息 =====
   127.0.0.1:9200 elasticsearch admin/123456
   192.168.1.100:6379 redis 未授权
   ```
   - 自动解析漏洞信息部分
   - 支持 `/` 分隔的用户名密码格式

3. **Lightx**
   ```
   [2025-12-14 21:00:31] [Plugin:MySQL:SUCCESS] MySQL:127.0.0.1:3306 root/root
   [2025-12-14 21:00:32] [Plugin:Redis:SUCCESS] Redis:192.168.1.100:6379 未授权访问
   ```
   - 自动识别 Plugin 标记
   - 支持时间戳和状态标记

**导入步骤**：

1. 点击顶部工具栏的 **"导入"** 按钮
2. 选择扫描工具的结果文件（.txt 或 .csv）
3. 系统自动识别文件格式并解析
4. 自动导入并开始批量测试

**智能识别特性**：

- ✅ 自动识别未授权访问（无用户名密码）
- ✅ 自动提取弱口令（用户名/密码）
- ✅ 自动去重（相同目标只导入一次）
- ✅ 自动标准化服务类型名称
- ✅ 支持多种分隔符格式（`:`, `/`, 空格）

#### 方式三：CSV 批量导入

1. 点击顶部工具栏的 **"导入"** 按钮
2. 选择 CSV 文件（参考 `example.csv`）
3. 系统自动导入并开始批量测试

**CSV 格式示例**：

```csv
Type,IP,Port,User,Pass
Redis,192.168.1.100,6379,,
MySQL,192.168.1.101,3306,root,password123
SSH,192.168.1.102,22,admin,admin123
FTP,192.168.1.103,21,anonymous,
MongoDB,192.168.1.104,27017,,
Docker,192.168.1.105,2375,,
```

**CSV 格式说明**：

- **Type**: 服务类型（Redis、MySQL、SSH 等）
- **IP**: 目标 IP 地址
- **Port**: 目标端口
- **User**: 用户名（可选，留空表示未授权访问）
- **Pass**: 密码（可选）

#### 方式四：剪贴板导入

1. 复制符合 CSV 格式或扫描工具输出格式的文本到剪贴板
2. 点击顶部工具栏的 **"剪贴板导入"** 按钮
3. 系统自动解析并导入

#### 方式五：拖拽上传 🎯

**最便捷的导入方式**：直接将文件拖拽到应用窗口即可！

1. 将 CSV 或 TXT 文件拖拽到 MPET 窗口
2. 出现蓝色拖拽提示遮罩
3. 释放文件，系统自动识别格式并导入

**支持的文件格式**：
- ✅ `.csv` - CSV 格式文件
- ✅ `.txt` - Fscan/Lightx 结果文件

**智能识别**：
- 自动识别 Fscan 1.8.4、Fscan 2.1.1、Lightx 格式
- 自动区分未授权访问和弱口令
- 自动去重和标准化

### 2. 连接测试

- **单个测试**: 点击连接列表中的 **"重连"** 按钮
- **批量测试**: 
  1. 勾选多个连接（或点击表头全选）
  2. 点击顶部工具栏的 **"批量连接"** 按钮
  3. 系统并发执行连接测试

### 3. 查看详情

1. 点击连接列表中的 **"详情"** 按钮展开详细信息
2. 详情面板包含：
   - **连接信息**: 服务类型、IP、端口、用户名、状态、消息等
   - **连接日志**: 实时显示连接过程的详细日志
   - **执行结果**: 显示命令执行结果或文件列表
   - **命令执行**: 支持 SSH、Docker、Kubernetes 等服务的命令执行

### 4. 特殊功能

#### FTP/SFTP/SMB 文件浏览

- 连接成功后，详情面板会显示文件浏览器
- 支持目录导航、文件下载

#### Docker 容器管理

- 连接成功后，点击 **"容器 Shell"** 按钮
- 选择容器并执行命令

#### Kubernetes Pod 管理

- 连接成功后，在命令执行区域选择 Pod
- 执行命令或查看日志

#### VNC/RDP 屏幕截图

- 连接成功后，点击 **"获取屏幕截图"** 按钮
- 截图会显示在执行结果区域

### 5. 导出漏洞报告

1. 勾选需要导出的连接
2. 点击顶部工具栏的 **"导出报告"** 按钮
3. 系统自动：
   - 展开所有选中的连接详情
   - 截取连接卡片截图
   - 从数据库读取漏洞信息模板
   - 根据用户名密码判断是弱口令还是未授权访问
   - 生成 Markdown 格式报告
   - 保存到 `reports/report_YYYYMMDD_HHMMSS/` 目录

**报告包含**：
- 漏洞基本信息（名称、等级、目标地址）
- 漏洞说明（自动填充用户名密码）
- 漏洞截图（连接详情截图）
- 修复建议（从数据库读取）

### 6. 漏洞信息管理

1. 点击顶部工具栏的 **"漏洞信息"** 按钮
2. 在弹出的对话框中：
   - 查看所有漏洞信息模板
   - 添加新的漏洞信息
   - 编辑现有漏洞信息
   - 删除不需要的漏洞信息

**漏洞信息包含**：
- 服务类型（如 Redis、MySQL）
- 漏洞类型（弱口令或未授权访问）
- 漏洞名称
- 风险等级（高危、中危、低危）
- 漏洞描述（支持 `{username}` 和 `{password}` 占位符）
- 修复建议

### 7. 代理配置

1. 点击顶部工具栏的 **"代理"** 按钮
2. 在弹出的对话框中：
   - 启用/禁用代理
   - 选择代理类型（SOCKS5）
   - 填写代理主机和端口
   - 填写代理用户名和密码（可选）
3. 点击 **"确定"** 保存配置
4. 所有后续连接将通过代理进行

### 8. 筛选和搜索

使用顶部筛选栏快速定位目标：

- **服务类型**: 多选筛选
- **IP 地址**: 模糊搜索
- **用户名**: 模糊搜索
- **状态**: 成功/失败/待连接
- **消息内容**: 模糊搜索

### 9. 系统日志

1. 点击右上角的 **"日志"** 按钮
2. 查看系统运行日志
3. 点击 **"清空显示"** 清除日志显示（不影响实际日志）

## ⚙️ 配置文件

### config.json

应用启动时自动生成，位于可执行文件同目录：

```json
{
  "password": "admin123",
  "proxy": {
    "enabled": false,
    "type": "socks5",
    "host": "127.0.0.1",
    "port": "1080",
    "user": "",
    "pass": ""
  }
}
```

### connections.db

SQLite 数据库文件，包含两张表：

**connections 表**：
- 存储所有连接信息
- 包含连接日志和执行结果

**vulnerabilities 表**：
- 存储漏洞信息模板
- 支持自定义编辑

- 

## 📊 截图展示

### 主界面

![image-20260116174700348](./assets/image-20260116174700348.png)

### 连接详情

![image-20260116174732762](./assets/image-20260116174732762.png)

### 文件浏览器

![image-20260116174805546](./assets/image-20260116174805546.png)

### Docker Shell

![image-20260116174901647](./assets/image-20260116174901647.png)

![image-20260116175040245](./assets/image-20260116175040245.png)

### 漏洞报告

![image-20260116175149459](./assets/image-20260116175149459.png)



## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！

### 开发流程

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

### 代码规范

- Go 代码遵循 `gofmt` 格式
- TypeScript 代码遵循 ESLint 规则
- 提交信息遵循 Conventional Commits

## 📝 更新日志

### v1.0.0 (2026-01-16)

**新功能**：
- ✅ 支持 25+ 种服务协议
- ✅ 智能导入：支持 Fscan 1.8.4、Fscan 2.1.1、Lightx 结果文件自动识别
- ✅ 拖拽上传：直接拖拽文件到窗口即可导入
- ✅ 批量导入和批量操作
- ✅ 未授权访问和弱口令自动识别
- ✅ Docker 和 Kubernetes 容器管理
- ✅ FTP/SFTP/SMB 文件浏览
- ✅ VNC/RDP 屏幕截图
- ✅ Markdown 格式漏洞报告导出
- ✅ 漏洞信息数据库管理
- ✅ SOCKS5 代理支持
- ✅ 亮色/暗色主题切换

**智能解析**：
- ✅ 自动识别 Fscan 1.8.4 格式（`[+] Service:IP:Port credential`）
- ✅ 自动识别 Fscan 2.1.1 格式（漏洞信息部分）
- ✅ 自动识别 Lightx 格式（Plugin 标记）
- ✅ 自动区分未授权访问和弱口令
- ✅ 自动去重和标准化服务类型

**技术栈**：
- Wails v2.11
- Go 1.22
- Vue 3.4
- TypeScript 5.2
- Ant Design Vue 4.0

## ⚠️ 免责声明

**本工具仅供安全研究和合法授权测试使用。**

- ✅ **合法用途**：
  - 授权的安全测试和渗透测试
  - 学习和研究网络安全技术
  - 企业内部安全审计
  - 安全培训和教学

- ❌ **禁止用途**：
  - 非法入侵和未授权访问
  - 窃取他人数据和隐私
  - 破坏计算机系统
  - 任何违反法律法规的行为

**使用者需自行承担使用本工具所产生的任何法律责任。作者不对任何滥用行为负责。**

## 👥 作者信息

**公众号**: 浅梦安全  
**开发者**: onewin  

## 参考致谢

感谢**知攻善防实验室**：**ChinaRan404的开源项目**[ChinaRan0/Attack_login: 适用于红队攻防演练获得目标账户批量登录，报告编写](https://github.com/ChinaRan0/Attack_login)

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源协议。

---

<div align="center">

**MPET - Multi-Protocol Exploitation Toolkit**  
**多协议漏洞利用与攻击模拟平台**

专业 · 高效 · 安全

Made with ❤️ by onewin

</div>

## Star History Chart

[![Star History Chart](https://api.star-history.com/svg?repos=onewinner/MPET&type=Date)](https://www.star-history.com/#onewinner/MPET&Date)

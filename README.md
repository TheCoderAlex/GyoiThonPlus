# GyoiThonPlus

## 项目简介
GyoiThonPlus 是对原工具 GyoiThon 的增强版本，旨在解决原工具中存在的一些 bug，并添加了用户友好的前后端界面，使得工具的使用更加便捷和直观。通过本项目，用户可以更轻松地进行配置管理、环境检查等操作。

## 项目结构
```
GyoiThonPlus/
├── app/                   # 后端代码
│   ├── api/               # API 接口
│   ├── templates/         # 前端模板
│   ├── utils/             # 工具函数
│   └── __init__.py        # 初始化文件
├── front/                 # 前端代码
│   ├── src/               # 源代码
│   │   ├── components/    # 组件
│   │   ├── mock/          # 模拟数据
│   │   ├── pages/         # 页面
│   │   ├── store/         # 状态管理
│   │   └── utils/         # 工具函数
│   ├── docs/              # 文档
│   ├── jsconfig.json      # JavaScript 配置
│   ├── package.json       # 前端依赖配置
│   └── tsconfig.node.json # TypeScript 配置
├── bin/                   # 二进制文件
│   └── GyoiThon/          # GyoiThon 相关文件
│       └── config.ini     # 配置文件
├── config.py              # 项目配置
├── requirements.txt       # Python 依赖
├── package.json           # 项目依赖
├── package-lock.json      # 项目依赖锁定
├── start_celery.sh        # 启动 Celery 的脚本
└── example/
    ├── docker-compose.yml # Docker Compose 配置文件
    └── README.md          # 示例项目说明
```

## 功能特性
1. **用户友好界面**：提供了前后端界面，方便用户进行操作和配置管理。
2. **配置管理**：支持对配置文件进行读取和更新，用户可以在界面上直接修改配置项。
3. **环境检查**：提供了对 Python 包、Node.js 版本和网络连接的检查功能，确保环境的正确性。
4. **模拟登录**：支持模拟登录功能，方便开发和测试。

## 环境准备
- **Python 环境**：确保已经安装 Python，项目使用的 Python 包依赖在 `requirements.txt` 中列出。
- **Node.js 和 Yarn**：需要安装 Node.js（版本 `^16.14.0`）和 Yarn（版本 `^1.21.1`）。
- **Git**：版本 `^2.15.0`，用于拉取代码。
- **Redis 环境**：项目使用 Redis 作为 Celery 的消息代理和结果后端，需要安装并启动 Redis 服务。
- **Docker 和 Docker Compose**：用于一键搭建项目环境。

## 安装步骤
### 后端依赖安装
```bash
pip install -r requirements.txt
```

### 前端依赖安装
```bash
cd front
npm install
```

## 使用 Docker Compose 搭建靶场
### 启动环境
在项目根目录下，使用以下命令启动项目测试用的靶场：
```bash
cd example
docker-compose up -d
```
此命令会根据 `example/docker-compose.yml` 文件中的配置，启动 Drupal 7.57 靶场及相关数据库服务。Drupal 服务将映射到本地的 8000 端口。

### 关闭环境
如果需要关闭并移除所有由 Docker Compose 启动的容器，可以使用以下命令：
```bash
cd example
docker-compose down
```

## 运行项目
### 启动 Celery
由于项目使用 Celery 进行任务处理，需要在单独的会话中启动 Celery worker。可以使用以下命令：
```bash
./start_celery.sh
```
此脚本会设置必要的环境变量并启动 Celery worker。

### 后端启动
```bash
# 进入项目根目录
python run.py
```

### 前端启动
```bash
# 进入 front 目录
cd front
npm run dev
```

## API 接口
### 配置管理
- `GET /api/config`：获取配置文件信息。
- `POST /api/update`：更新配置文件信息。

### 环境检查
- `GET /api/check_python_packages`：检查 Python 包是否满足要求。
- `GET /api/check_node_version`：检查 Node.js 版本是否满足要求。
- `GET /api/check_network_connectivity`：检查网络连接是否正常。

## 贡献指南
如果你对本项目感兴趣，可以按照以下步骤进行贡献：
1. Fork 本项目。
2. 创建新的分支：`git checkout -b feature/your-feature`。
3. 提交你的更改：`git commit -m 'Add some feature'`。
4. 推送至远程分支：`git push origin feature/your-feature`。
5. 提交 Pull Request。

## 许可证
本项目采用 [MIT 许可证](LICENSE)。

## 联系方式
如果你有任何问题或建议，可以通过以下方式联系我们：
- 邮箱：[alextang@seu.edu.cn]
- GitHub Issues：[https://github.com/GyoiThonPlus/issues](https://github.com/GyoiThonPlus/issues)

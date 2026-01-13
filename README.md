# My NocoDB Deployment

基于 Docker 部署的 **NocoDB** (Airtable 开源替代品)，运行于 Ubuntu 22.04 云服务器。

## 🚀 架构说明
本项目采用生产级双容器架构：
- **App**: NocoDB (Node.js) - 运行在 8080 端口
- **Database**: PostgreSQL 14 (Alpine) - 独立数据存储
- 你需要手工修改.env.sample 成为.env 并编辑你想要的内容
## 🛠 快速管理命令

### 启动服务
```bash
docker compose up -d
```
###STOP
docker compose down
###查看日志
```Bash

docker compose logs -f nocodb-app
```
###更新版本
Bash

docker compose pull && docker compose up -d
###文件结构
docker-compose.yml: 容器编排配置文件

.env: 环境变量及数据库密码 (已加入 .gitignore，不上传)

noco_db_data/: PostgreSQL 数据库持久化目录

noco_app_data/: NocoDB 静态资源及附件存储




# My NocoDB Deployment

基于 Docker 部署的 **NocoDB** (Airtable 开源替代品)，运行于 Ubuntu 22.04 云服务器。

## 🚀 架构说明
本项目采用生产级双容器架构：
- **App**: NocoDB (Node.js) - 运行在 8080 端口
- **Database**: PostgreSQL 14 (Alpine) - 独立数据存储

## 🛠 快速管理命令

### 启动服务
```bash
docker compose up -d
```
###STOP
docker compose down
```

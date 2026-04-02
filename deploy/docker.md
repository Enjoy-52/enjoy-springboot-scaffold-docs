# Docker 部署

## 推荐方式
- 使用 `docker-compose` 统一编排依赖（Nacos/DB/Redis/Seata 等）
- 应用镜像按服务拆分构建与发布

## 关键点
- 环境变量区分环境
- 配置中心地址可通过环境变量注入


# Nacos 配置

## 推荐结构
- `application.yml`：公共配置
- `{app}.yml`：应用级配置
- `datasource.yml` / `redis.yml`：按域拆分

## 注意事项
- 生产环境开启权限与审计
- 重要配置变更走发布流程


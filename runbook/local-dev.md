# 本地运行（建议）

## 配置策略
多数服务采用「本地 `application.yml` 兜底 + Nacos 配置中心为主」：
- 常见形式：`spring.config.import: optional:nacos:...`
- 常见默认 profile：`cloud-dev-mac`（以各服务 `application.yml` 为准）

## 常见依赖
- **Nacos**：服务注册与配置中心
- **MySQL**：业务库（不同服务可能使用不同 schema）
- **Redis**：缓存/会话/分布式能力（部分 starter 会默认启用）
- **XXL Job Admin**：若启用作业调度（控制台 + 执行器）
- **Seata**：按需启用分布式事务（以配置为准）

## 推荐启动顺序（最小可用链路）
1. `enjoy-base-nacos`
2. MySQL、Redis
3. `enjoy-base-uam`（共享依赖点）
4. `enjoy-base-auth`
5. `enjoy-base-gateway`
6. 其它业务服务（`app-biz`、`bpm-biz`、`pay`、`mp`、`report`、`dash-design` 等）
7. 运维/工具/调度（`monitor`、`code-generator`、`xxl-job`、`elastic-job`、`quartz`）

## 排障提示
- 页面/接口 404：先确认网关路由与目标服务 `spring.application.name` 是否一致
- 配置不生效：检查 `spring.profiles.active` 与 Nacos 中 DataId/Group/Namespace 是否匹配
- 连接失败：优先核对 Nacos/MySQL/Redis 地址端口（很多服务支持环境变量覆盖）


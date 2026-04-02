# Starter 组件总览（`enjoy-starter`）

`enjoy-starter` 是公司自研 Spring Boot 组件集合，统一以 `enjoy-starter-*` 形式提供能力，并通过 `enjoy-starter-bom` 统一依赖版本。

## 自动装配形式
- **Spring Boot 3 推荐方式**：`META-INF/spring/org.springframework.boot.autoconfigure.AutoConfiguration.imports`
- **显式启用方式**：通过 `@Enable...` 注解 + `@Import(...)`（常用于网关、动态数据源、Job、Swagger 等）
- **环境增强**：少数模块使用 `META-INF/spring.factories` 注册 `EnvironmentPostProcessor`（如日志模块）

## 组件分类（建议）
- **基础**：`starter-core`、`starter-log`
- **数据**：`starter-data`、`starter-datasource`、`starter-sequence`
- **服务治理**：`starter-feign`、`starter-sentinel`、`starter-gray`
- **安全与合规**：`starter-security`、`starter-xss`、`starter-encrypt`、`starter-audit`、`starter-sensitive`
- **网关与通信**：`starter-gateway`、`starter-sse`、`starter-websocket`
- **业务扩展**：`starter-uam`、`starter-app`、`starter-bpm-*`、`starter-job`、`starter-oss`、`starter-swagger`、`starter-seata`

下一步阅读建议：
- 先看「Starter → 微服务引用矩阵」
- 再按组件分类逐个深入


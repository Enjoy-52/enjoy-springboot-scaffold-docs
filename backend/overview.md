# 后端总览（`src/backend`）

后端代码位于 `enjoy/src/backend`，整体为 **Maven 多模块**，核心分三块：

- **`enjoy-starter-parent`**：父 POM，统一 Maven 插件、发布与基础依赖策略。
- **`enjoy-starter`**：自研 `enjoy-starter-*` 组件集合（含 `enjoy-starter-bom` 统一版本）。
- **`enjoy-framework`**：业务与平台微服务聚合工程（各可运行 Spring Boot 服务都在这里）。

## 关键聚合关系
- `enjoy-framework` 的 parent 为 `com.millennia:enjoy-starter-parent`
- `enjoy-framework` 通过 `dependencyManagement` import `com.millennia:enjoy-starter-bom`

## 微服务聚合（`enjoy-framework`）
`enjoy-framework` 通过 profile 聚合模块（常见：`mode-cloud` / `mode-boot`），并在其下按领域拆分：
- **Base（基础底座）**：网关、认证、权限/用户、Nacos 等
- **Presentation（业务展示）**：App/BPM/支付/公众号/报表/大屏等
- **Scheduler（调度）**：XXL/ElasticJob/Quartz
- **Ops/Devtools（运维/工具）**：监控、代码生成器

## 建议阅读顺序
1. 先看「Starter 组件」：理解通用能力如何被复用
2. 再看「微服务清单」：每个服务做什么、依赖哪些 starter
3. 最后看「本地运行」：依赖与启动顺序


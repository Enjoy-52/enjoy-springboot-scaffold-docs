# 微服务清单（`enjoy-framework`）

> 以下服务均位于 `enjoy/src/backend/enjoy-framework`，并具备独立启动入口（`@SpringBootApplication` 或在 POM 指定 mainClass）。

## Base（基础底座）
- **`enjoy-base-nacos`**：Nacos Server/Console 打包运行（POM mainClass 指向 Nacos 启动类）
- **`enjoy-base-gateway`**：网关（`EnjoyGatewayApplication`），统一入口与路由
- **`enjoy-base-auth`**：认证中心（`EnjoyAuthApplication`），OAuth2/鉴权
- **`enjoy-base-uam`**：用户/权限/文件等中心（`EnjoyUamApplication`），多服务共享依赖点

## Presentation（业务展示）
- **`enjoy-app-biz`**：App 业务（`EnjoyAppApplication`）
- **`enjoy-bpm-biz`**：流程/工作流（`EnjoyBpmApplication`，Flowable）
- **`enjoy-pay`**：支付平台（`EnjoyPayPlatformApplication`）
- **`enjoy-mp`**：公众号平台（`EnjoyMpPlatformApplication`）
- **`enjoy-report`**：报表服务（`EnjoyReportApplication`）
- **`enjoy-dash-design`**：大屏设计（`EnjoyDashDesignApplication`）

## Scheduler（调度）
- **`enjoy-xxl-job`**：XXL Job 控制台（`EnjoyJobAdminApplication`）
- **`enjoy-elastic-job`**：作业执行侧（`EnjoyElasticJobApplication`）
- **`enjoy-quartz`**：Quartz 调度服务（`EnjoyQuartzApplication`）

## Ops/Devtools（运维/工具）
- **`enjoy-monitor`**：监控（`EnjoyMonitorApplication`，Boot Admin Server）
- **`enjoy-code-generator`**：代码生成器（`EnjoyCodeGeneratorApplication`）


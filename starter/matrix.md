# Starter → 微服务引用矩阵

> 口径：以各微服务 `pom.xml` 中对 `com.millennia:enjoy-starter-*` 的 **直接依赖**为准。

| Starter | 被引用的微服务（artifactId） |
|---|---|
| `enjoy-starter-core` | `enjoy-app-biz`、`enjoy-monitor`、`enjoy-mp`、`enjoy-code-generator` |
| `enjoy-starter-data` | `enjoy-base-auth`、`enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-mp`、`enjoy-pay`、`enjoy-quartz`、`enjoy-elastic-job`、`enjoy-code-generator` |
| `enjoy-starter-datasource` | `enjoy-pay`、`enjoy-code-generator` |
| `enjoy-starter-feign` | `enjoy-base-auth`、`enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-mp`、`enjoy-report` |
| `enjoy-starter-gateway` | `enjoy-base-gateway`、`enjoy-base-uam` |
| `enjoy-starter-gray` | `enjoy-base-auth`、`enjoy-base-uam`、`enjoy-app-biz`、`enjoy-mp`、`enjoy-pay`、`enjoy-quartz`、`enjoy-elastic-job`、`enjoy-code-generator` |
| `enjoy-starter-idempotent` | `enjoy-code-generator` |
| `enjoy-starter-job` | `enjoy-elastic-job` |
| `enjoy-starter-log` | `enjoy-base-auth`、`enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-mp`、`enjoy-pay`、`enjoy-quartz`、`enjoy-code-generator` |
| `enjoy-starter-oss` | `enjoy-base-uam` |
| `enjoy-starter-security` | `enjoy-base-auth`、`enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-mp`、`enjoy-pay`、`enjoy-quartz`、`enjoy-elastic-job`、`enjoy-code-generator` |
| `enjoy-starter-sensitive` | `enjoy-mp`、`enjoy-pay` |
| `enjoy-starter-sentinel` | `enjoy-base-gateway`、`enjoy-base-auth`、`enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-mp`、`enjoy-pay`、`enjoy-quartz`、`enjoy-elastic-job` |
| `enjoy-starter-sequence` | `enjoy-bpm-biz`、`enjoy-pay` |
| `enjoy-starter-swagger` | `enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-pay`、`enjoy-quartz`、`enjoy-code-generator` |
| `enjoy-starter-uam` | `enjoy-base-uam`、`enjoy-pay`、`enjoy-report`、`enjoy-dash-design`、`enjoy-code-generator` |
| `enjoy-starter-xss` | `enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-mp`、`enjoy-pay`、`enjoy-code-generator` |
| `enjoy-starter-audit` | `enjoy-base-uam` |
| `enjoy-starter-encrypt` | `enjoy-base-uam`、`enjoy-app-biz`、`enjoy-bpm-biz`、`enjoy-mp`、`enjoy-pay`、`enjoy-quartz`、`enjoy-code-generator` |

## 备注
- `enjoy-xxl-job` 更偏向「控制台/管理端」，主要使用 xxl-job 官方依赖，不一定直接依赖 `enjoy-starter-job`。
- 其它 starter（如 `seata` / `sse` / `websocket` / `excel` / `bpm-*`）可能在未展开的模块或特定场景中启用；建议结合实际服务 `pom.xml` 与 Nacos 配置核对。


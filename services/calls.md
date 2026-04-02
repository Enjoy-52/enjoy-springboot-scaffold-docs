# 服务调用关系（线索）

> 这里的调用关系来自代码中的 `@FeignClient(...)` 线索与 starter 依赖推断，适合作为“全局视图”。最终以实际接口与网关路由/Nacos 配置为准。

## 关键依赖点
- **`enjoy-base-uam`（`enjoy-uam-biz`）**：多数服务会依赖它提供的用户/权限/文件等能力

## Feign 调用线索（部分）
- **Auth → UAM**
  - `RemoteUserService`：`@FeignClient(value="enjoy-uam-biz")`
- **Report → UAM**
  - `RemoteFileService`：`@FeignClient(value="enjoy-uam-biz")`（文件能力）
- **其它服务 → UAM**
  - 多处出现 `RemoteFileService` / `RemoteUserService` 目标为 `enjoy-uam-biz`
- **外部服务调用 App**
  - `RemoteAppUserService`：目标 `enjoy-app-biz`
- **外部服务调用 BPM**
  - `RemoteBpmApiService`：目标 `enjoy-bpm-biz`

## 入口流量
通常从 **`enjoy-base-gateway`** 进入，按路由规则转发至各后端服务。


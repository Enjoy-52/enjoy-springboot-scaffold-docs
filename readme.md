<!--
 * @Author: CodeCaptain
 * @Date: 2026-04-02 17:22:35
 * @LastEditors: CodeCaptain
 * @LastEditTime: 2026-04-02 17:26:45
 * @Description: 
 * @FilePath: /enjoy-springboot-scaffold-docs/readme.md
-->
# SpringCloud 微服务脚手架

> 基于 SpringCloud Alibaba 构建的企业级微服务脚手架，开箱即用。

<div class="tip">
  内置：Gateway + Nacos + Sentinel + OpenFeign + Seata + MyBatis-Plus + Knife4j
</div>

## 项目结构
```bash
scaffold/
├── gateway # 网关
├── system-api # 系统模块 API
├── system-service # 系统模块实现
├── common # 公共工具
└── pom.xml # 父依赖
```
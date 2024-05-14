# 开发概要文档

## 开发周期

本项目开发周期预计为：**1个半月**（要求，每人开发需要按时完成分配的任务，以及对任务内未提及或隐藏部分完善出来）

## 开发前的准备事项

- **环境搭建**：确保具备必要的软件安装和环境配置，包括但不限于 `Node.js`, `Vue CLI`, `JDK-17`, `Kotlin`, `PostgreSQL`, `Redis` 以及 `Docker` 环境设置。
- **需求理解**：开发者需求解析分析，确保每位开发人员都能完全理解项目需求和业务逻辑。
- **设计评审**：进行系统设计评审，确保架构设计能够满足项目需求，同时保持良好的扩展性和维护性。
- **代码规范**：制定统一的代码编写规范和提交规范，确保代码质量和团队协作的高效性。
- **安全考虑**：加强对数据安全和隐私保护的重视，确保所有模块都采取合适的安全措施。
- **项目管理**：使用敏捷开发方法进行项目管理，定期进行迭代计划和回顾会议，保证项目按时进展。

## 项目开发

我们协作开发采用 git 进行，使用 github 平台进行项目管理与敏捷开发管理。

- 后端项目：https://github.com/fantastic-editor/FantasticEditorApi
- 前端项目：https://github.com/fantastic-editor/FantasticEditorWeb

## 人员配置

- 曾昶雯【项目负责人|前端开发】
- 张睿相【后端开发|前端开发】
- 戴闯【后端工程|后端设计】

## 环境搭建

后端开发者前期需要准备 `JDK-17`, `Kotlin-1.9.22`, `Maven`, `PostgreSQL`, `Redis` 相应开发环境，统一使用 Jetbrains Intellij IDEA Ultimate 2023.3.X / Jetbrains Intellij IDEA Ultimate 2024.1.X，`Docker` 环境选择配置，建议使用 `Docker` 部署 `PostgreSQL`、`Redis` 等服务。

前端开发者前期需要准备 `Node.js`, `Vue CLI` 相应开发环境，统一使用 Jetbrains WebStorm 2023.3.X / Jetbrains WebStorm 2023.4.X ，无需额外配置 `Docker` 环境。

使用 Jetbrains Intellij IDEA Ultimate 为了保证开发者的开发规范请务必安装如下插件：

1. Alibaba Java Coding Guidelines
2. CheckStyle-IDEA
3. Git Commit Template Check

使用 Jetbrains WebStorm 为了保证开发者开发规范请务必安装如下插件：

1. Git Commit Template Check

## 框架配置

### 后端

1. 使用主体框架 `SpringBoot-Kotlin 3.2.5 Maven`
   1. SDK配置
   2. 架构打包
2. 数据库采用 `PostgreSQL alpine3.19` 具体数据库设计逻辑见后
3. 缓存数据库采用 `Redis 7.2` 具体数据库样式逻辑见后

### 前端

- 使用框架 `Vue3`
- 使用设计框架，主要为 `AntDesign` ，辅助设计为 `Tailwindcss`
- 原型图设计工具 `Pixso`

## 接口规范

- 接口采用 Apifox 进行接口测试，已将各位开发者拉入团队项目内（可在 锋楪技术团队 -> FantasticEditor 中查阅到）
- Api 采用 `RESTful` 风格进行开发，具体额外开发规范请参考接口开发规范，对所有的业务请求中，若返回内容不正确，均会返回对应的HTTP状态码与请求内容。
- 具体其他接口内容参考规范后进行配置
- 使用 IDEA 插件 [Apifox Helper](https://plugins.jetbrains.com/plugin/20549-apifox-helper) 辅助进行接口文档编写与描述完善
- 对于所有接口，各位开发者需要完成对故障尽可能返回信息，对错误内容进行预案。避免出现未知错误导致程序无法按需进行。
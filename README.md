<h1 align="center">🧬 RabGenDB · 前端</h1>

<p align="center"><em>—— 狂犬病毒基因组数据库的 Vue 前端</em></p>
<p align="center"><em>—— 2024.12.24</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/Framework-Vue%202.6-42B883?style=flat-square" />
  <img src="https://img.shields.io/badge/UI-Element%20UI-409EFF?style=flat-square" />
  <img src="https://img.shields.io/badge/Router-vue--router%203-3EAF7C?style=flat-square" />
  <img src="https://img.shields.io/badge/HTTP-axios-5A29E4?style=flat-square" />
  <img src="https://img.shields.io/badge/Type-Practice%20Project-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Status-Complete-brightgreen?style=flat-square" />
</p>

---

## 项目简介

**RabGenDB**（Rabies Genome Database）是一个狂犬病毒基因组数据库练手项目，支持序列元数据的**提交 → 审核 → 检索**全流程。本仓库为其**前端**，按**三级角色**渲染不同界面，通过 axios 调用后端（配套仓库 `004_SpringbootWeb_RabGenDB_Backend`）接口。

## 技术栈

| 组件           | 说明                    |
| :------------- | :---------------------- |
| Vue 2.6        | 前端框架                |
| Vue CLI 5      | 构建脚手架              |
| Element UI 2.15| 组件库                  |
| vue-router 3   | 路由（history 模式）    |
| axios          | 与后端通信              |

## 角色与页面

| 角色 (role)      | 页面                                                      |
| :--------------- | :-------------------------------------------------------- |
| 普通用户 (2)     | 首页 · 狂犬概览 · 序列检索 · 序列提交 · 通知 · 个人信息   |
| 管理员 (1)       | 首页 · 序列检索 · **序列审核** · 个人信息                 |
| 超级管理员 (0)   | 首页 · **用户管理** · **权限管理** · 个人信息             |

## 目录结构

```
src/
├── main.js                 # 入口
├── App.vue
├── router/index.js         # 路由表（登录 + 三级角色页面）
├── components/
│   ├── LoginComponent.vue
│   ├── user/               # 普通用户页面
│   ├── admin/              # 管理员页面
│   └── superAdmin/         # 超级管理员页面
└── assets/images/          # 狂犬病毒基因组 / 结构 / 分布图等
```

## 运行

```bash
npm install        # 安装依赖
npm run serve      # 本地开发（默认 http://localhost:8080）
npm run build      # 生产构建
```

> 需先启动后端仓库 `004_SpringbootWeb_RabGenDB_Backend`（运行在 `http://localhost:9090`）。

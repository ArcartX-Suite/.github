<div align="center">
<img src="https://github.com/user-attachments/assets/959da519-d523-48ce-bb09-b5cad5bbc4af" alt="ArcartX-Suite" width="100%" />
<br /><br />
    
[![Docs](https://img.shields.io/badge/ArcartX--Suite_Wiki-文档-6366f1?style=for-the-badge&logo=readthedocs&logoColor=white)](https://arcartx-suite.github.io/ArcartXSuite-Wiki/)
[![Cloud](https://img.shields.io/badge/AXS_Cloud-云端平台-0ea5e9?style=for-the-badge&logo=cloudflare&logoColor=white)](https://cloud.021209.xyz)
[![ArcartX Wiki](https://img.shields.io/badge/ArcartX_Wiki-官方文档-f97316?style=for-the-badge&logo=bookstack&logoColor=white)](https://wiki.arcartx.com/docs)
[![Forum](https://img.shields.io/badge/ArcartX-论坛-8b5cf6?style=for-the-badge&logo=discourse&logoColor=white)](https://arcartx.com)
[![SDK](https://img.shields.io/github/v/release/ArcartX-Suite/ArcartXSuite-Core?label=axs-api&style=for-the-badge)](https://github.com/ArcartX-Suite/ArcartXSuite-Core/releases)

</div>

<br />

## 关于本组织

本 GitHub Organization 是 **ArcartX-Suite 开源生态** 的公开入口，主要托管：

- **开源 SDK** — 模块开发 API（`axs-api`）与宿主参考实现
- **Wiki 文档** — 服主指南、开发者教程与 API 参考
- **免费模块** — 部分免费模块的源码与发布（陆续开源）

完整版 ArcartX-Suite（含更多商业模块与云端分发）不在此组织内维护。服主使用、模块授权与安装说明见 [ArcartX-Suite Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/)；ArcartX 客户端与服务端基础请查阅 [ArcartX 官方 Wiki](https://wiki.arcartx.com/docs)。

> **说明：** ArcartX-Suite 为基于 ArcartX 客户端模组生态构建的**第三方**框架，**不属于 ArcartX 官方插件**。
> 
> **警告：** 本系列所有作品均以扩展 **ArcartX** 生态为理念，不允许在本组织进行任何破坏 **ArcartX** 权益的行为。
>
> **邀请：** 我们欢迎一切愿意为 **ArcartX** 开拓生态的有志之士，请联系QQ群 1098634325

---

## 相关站点

| 站点 | 说明 | 链接 |
|------|------|------|
| **AXS Cloud** | ArcartX-Suite 云端平台：服主注册、免费模块授权、模块装备与同步 | [cloud.021209.xyz](https://cloud.021209.xyz) |
| **ArcartX-Suite Wiki** | 本组织维护的插件文档：模块配置、开发者指南、API 参考 | [arcartx-suite.github.io/ArcartXSuite-Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/) |
| **ArcartX Wiki** | ArcartX 官方文档：客户端模组、服务端插件、UI/HUD 等 | [wiki.arcartx.com/docs](https://wiki.arcartx.com/docs) |
| **ArcartX 论坛** | ArcartX 社区论坛：服主交流、问题反馈、资源分享 | [arcartx.com](https://arcartx.com) |

云端授权与免费模块装备流程见 [Wiki · 云端模块](https://arcartx-suite.github.io/ArcartXSuite-Wiki/guide/cloud-modules)。

---

## 仓库一览

| 仓库 | 说明 | 链接 |
|------|------|------|
| **ArcartXSuite-Core** | 模块开发 SDK：`axs-api` 源码、桥接 API、发布脚本与 CI | [仓库](https://github.com/ArcartX-Suite/ArcartXSuite-Core) · [Releases](https://github.com/ArcartX-Suite/ArcartXSuite-Core/releases) |
| **ArcartXSuite-Wiki** | VitePress 文档站源码（服主 / 开发者 / API） | [文档站](https://arcartx-suite.github.io/ArcartXSuite-Wiki/) · [源码](https://github.com/ArcartX-Suite/ArcartXSuite-Wiki) |
| **免费模块** | 独立仓库，按模块开源（见下表） | 随模块逐步添加 |

---

## 免费模块

ArcartX-Suite 共有 **12 个免费模块**。其中部分模块的源码将发布在本组织下；无论是否已开源，配置与用法均以 Wiki 为准。

| 模块 | 说明 | 文档 |
|------|------|------|
| **RGB** | 渐变文本，PAPI 扫光效果 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/rgb) |
| **Pickup** | 拾取 HUD 提示 + 扫描器模式 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/pickup) |
| **Announcer** | 公告 / 字幕轮播，可点击执行命令 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/announcer) |
| **LoginView** | ArcartX UI 登录/注册，支持 AuthMe | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/loginview) |
| **OnlineRewards** | 在线奖励 / 签到 / 补签卡 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/onlinerewards) |
| **CombatEffect** | 战斗特效、连击、伤害飘字 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/combateffect) |
| **EventPacket** | 事件引擎，触发器 × 动作组合 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/eventpacket) |
| **Prop** | 快捷道具栏，客户端按键绑定 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/prop) |
| **Essentials** | 传送 / Warp / 一键砍树 / UI 菜单 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/essentials) |
| **Regions** | 区域保护，40+ 标志 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/regions) |
| **Menu** | 配置驱动 ArcartX 菜单 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/menu) |
| **AfkReward** | 区域 / 原地挂机奖励 | [Wiki](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/afkreward) |

完整模块索引（含非开源的商业模块文档入口）：[Wiki · 模块总览](https://arcartx-suite.github.io/ArcartXSuite-Wiki/modules/)。

---

## 模块开发者 · 快速开始

1. 从 [ArcartXSuite-Core Releases](https://github.com/ArcartX-Suite/ArcartXSuite-Core/releases) 下载 `axs-api-<version>.jar`，或克隆仓库后执行 `./gradlew :axs-api:jar`
2. 实现 `AbstractAXSModule`，编写 `module.yml`
3. 将模块 Jar 放入服务器的 `plugins/ArcartXSuite/modules/`，在宿主 `config.yml` 启用

```kotlin
dependencies {
    compileOnly(files("libs/axs-api-1.2.0-beta.jar"))
    compileOnly("org.spigotmc:spigot-api:1.20.1-R0.1-SNAPSHOT")
}
```

- [开发者指南](https://arcartx-suite.github.io/ArcartXSuite-Wiki/guide/developer/)
- [Capability 详解](https://arcartx-suite.github.io/ArcartXSuite-Wiki/guide/developer/capability-guide)
- [模块 Ed25519 签名](https://arcartx-suite.github.io/ArcartXSuite-Wiki/guide/developer/module-signature)
- [MODULAR-README.md](https://github.com/ArcartX-Suite/ArcartXSuite-Core/blob/main/MODULAR-README.md)

模块代码中 **只能** `import xuanmo.arcartxsuite.api.*`，**禁止**引用宿主 `bridge.*` 或 `module` 实现类。

---

## ArcartXSuite-Core 包含什么

| 目录 | 说明 |
|------|------|
| `axs-api/` | 模块公共 API（`AXSModule`、`ModuleContext`、Bridge API 等） |
| `axs-placeholder/` | PlaceholderAPI 扩展接口 |
| `proxy/` | Bungee / Velocity 代理端公共库 |
| `scripts/` | `publish-release.*`、`sign-module.py` 等工具 |
| 宿主参考实现 | 模块加载、桥接、跨服、配置诊断等基础设施源码 |

宿主参考实现涵盖属性 / 物品 / 经济桥接、CrossServer SDK、Keybind、Ed25519 模块签名等能力，供第三方模块与贡献者阅读，**不代表完整商业版插件的全部实现**。

---

## 环境要求

| 组件 | 要求 |
|------|------|
| Java | 17+（推荐 21） |
| Minecraft | 1.20.1+（Paper / Spigot 等） |
| 客户端 | ArcartX 模组（必装） |
| 开发依赖 | `axs-api` JAR（`compileOnly`） |

服主安装 ArcartX-Suite 宿主、在 [云端平台](https://cloud.021209.xyz) 注册并装备模块等流程，见 [Wiki · 快速开始](https://arcartx-suite.github.io/ArcartXSuite-Wiki/guide/)。安装 ArcartX 本体请先阅读 [ArcartX 官方 Wiki](https://wiki.arcartx.com/docs)。

---

## 参与贡献

| 类型 | 去向 |
|------|------|
| 文档修正 / 补全 | [ArcartXSuite-Wiki Issues](https://github.com/ArcartX-Suite/ArcartXSuite-Wiki/issues) |
| SDK / API / 工具链 | [ArcartXSuite-Core Issues](https://github.com/ArcartX-Suite/ArcartXSuite-Core/issues) |
| 免费模块源码 | 对应模块仓库的 Issues |
| 插件使用 / 云端授权 | [AXS Cloud](https://cloud.021209.xyz) · [Wiki · 云端模块](https://arcartx-suite.github.io/ArcartXSuite-Wiki/guide/cloud-modules) |
| ArcartX 客户端 / UI | [ArcartX Wiki](https://wiki.arcartx.com/docs) · [ArcartX 论坛](https://arcartx.com) |

欢迎 Pull Request。文档与小修复可直接提交；API 变更或大功能请先开 Issue 讨论。

---

## 链接速查

| | |
|---|---|
| ☁️ AXS Cloud 云端平台 | https://cloud.021209.xyz |
| 📖 ArcartX-Suite Wiki | https://arcartx-suite.github.io/ArcartXSuite-Wiki/ |
| 🔗 ArcartX 官方 Wiki | https://wiki.arcartx.com/docs |
| 💬 ArcartX 论坛 | https://arcartx.com |
| 💻 开源 SDK（axs-api） | https://github.com/ArcartX-Suite/ArcartXSuite-Core |
| 📝 ArcartX-Suite 文档源码 | https://github.com/ArcartX-Suite/ArcartXSuite-Wiki |

---

<div align="center">

<sub>
本页面存放于 <code>.github/profile/README.md</code> ·
ArcartX 与 ArcartX-Suite 均为各自项目的品牌名称
</sub>

</div>

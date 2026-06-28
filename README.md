<div align="center">

<!-- Banner：建议 1200×400 左右，上传到本仓库 assets/ 或任意 public 仓库 -->
<img width="3676" height="348" alt="ArcartX-Suite" src="https://github.com/user-attachments/assets/f95a5b48-22df-4020-b471-dc6df28fdbc2" />

<br /><br />

<!-- ===== Badges（按需启用，替换 YOUR_ORG / 链接） ===== -->

[![Docs](https://img.shields.io/badge/文档-Wiki-6366f1?style=for-the-badge&logo=readthedocs&logoColor=white)](https://YOUR_ORG.github.io/ArcartXSuite-Wiki/)
[![Cloud](https://img.shields.io/badge/云端平台-AXS_Cloud-0ea5e9?style=for-the-badge&logo=cloudflare&logoColor=white)](https://cloud.example.com)
[![Community](https://img.shields.io/badge/社区-ArcartX-f97316?style=for-the-badge&logo=discord&logoColor=white)](https://arcartx.com)
[![Release](https://img.shields.io/github/v/release/YOUR_ORG/ArcartXSuite?label=最新版本&style=for-the-badge)](https://github.com/YOUR_ORG/ArcartXSuite/releases)
[![License](https://img.shields.io/github/license/YOUR_ORG/ArcartXSuite?style=for-the-badge)](https://github.com/YOUR_ORG/ArcartXSuite/blob/main/LICENSE)

</div>

<br />

## ArcartX-Suite · 服务器玩法的交响组曲

> **Suite — 组曲，亦是套装。**
>
> 26+ 个模块如同 26+ 个乐章——每一个独立运作、各具音色、按需启用，
> 共享 ArcartX 的统一调性与 UI 主题，组合成一部属于你自己的 **服务器组曲**。
>
> 「 从登录到击杀，每一帧都是一个音符 」

**ArcartX-Suite（AXS）** 是专为 **ArcartX** 客户端生态构建的全场景 Minecraft 服务器核心套件。
采用「宿主 + 独立模块 Jar」架构：宿主提供桥接、模块加载、跨服与配置诊断，**所有业务逻辑在 `modules/*.jar` 中运行**。

> **说明：** ArcartX-Suite 为基于 ArcartX 生态的第三方框架，**不属于 ArcartX 官方插件**。

---

## 生态一览

| 项目 | 说明 | 链接 |
|------|------|------|
| **ArcartXSuite** | 服务端宿主插件（26+ 内置/可购模块） | [仓库](https://github.com/YOUR_ORG/ArcartXSuite) · [Releases](https://github.com/YOUR_ORG/ArcartXSuite/releases) |
| **ArcartXSuite-Core** | 模块开发 SDK（`axs-api` 源码与 CI 发布） | [仓库](https://github.com/YOUR_ORG/ArcartXSuite-Core) · [axs-api](https://github.com/YOUR_ORG/ArcartXSuite-Core/releases) |
| **ArcartXSuite-Wiki** | 服主文档、开发者指南、API 参考 | [文档站](https://YOUR_ORG.github.io/ArcartXSuite-Wiki/) · [源码](https://github.com/YOUR_ORG/ArcartXSuite-Wiki) |
| **AXS Cloud** | 服主账号、服务器绑定、模块授权与分发 | [云端平台](https://cloud.example.com) · [源码](https://github.com/YOUR_ORG/ArcartXSuite-CloudPlatform) |

---

## 模块亮点

<table>
<tr>
<td width="50%">

### 免费模块（节选）

- **LoginView** — ArcartX UI 登录/注册
- **CombatEffect** — 战斗特效与飘字
- **Regions** — 区域保护（40+ 标志）
- **Menu** — 配置驱动 ArcartX 菜单
- **Essentials** — 传送 / Warp / 一键砍树

</td>
<td width="50%">

### 付费模块（节选）

- **Tab** — 自定义 Tab 列表面板
- **Title** — 称号系统（属性联动）
- **Market** — 全球市场 / 拍卖行
- **Mail / Warehouse** — 邮件与仓库
- **QQBot** — QQ 群服互联（OneBot 11）

</td>
</tr>
</table>

完整模块列表见 [Wiki · 模块一览](https://YOUR_ORG.github.io/ArcartXSuite-Wiki/guide/modules)。

---

## 快速开始

### 服主

1. 安装 **Paper 1.20.1+**、**ArcartX 服务端插件** 与玩家端 **ArcartX 模组**
2. 下载 [ArcartXSuite 最新 Release](https://github.com/YOUR_ORG/ArcartXSuite/releases) 放入 `plugins/`
3. 在 `plugins/ArcartXSuite/config.yml` 中按需启用模块
4. 阅读 [服主指南](https://YOUR_ORG.github.io/ArcartXSuite-Wiki/guide/)

### 模块开发者

1. 从 [ArcartXSuite-Core Releases](https://github.com/YOUR_ORG/ArcartXSuite-Core/releases) 获取 `axs-api-<version>.jar`
2. 实现 `AbstractAXSModule`，编写 `module.yml`
3. 将产物放入 `plugins/ArcartXSuite/modules/`
4. 详见 [开发者指南](https://YOUR_ORG.github.io/ArcartXSuite-Wiki/guide/developer/)

```kotlin
// build.gradle.kts — 仅 compileOnly，禁止依赖宿主实现类
dependencies {
    compileOnly(files("libs/axs-api-x.x.x.jar"))
    compileOnly("org.spigotmc:spigot-api:1.20.1-R0.1-SNAPSHOT")
}
```

---

## 环境要求

| 组件 | 版本 |
|------|------|
| Java | 17+ |
| Minecraft | 1.20.1+（Paper / Spigot） |
| 客户端 | ArcartX 模组 |
| 可选 | Redis（跨服）、Vault / PlayerPoints（经济桥接） |

---

## 核心设计

```text
plugins/
  ArcartXSuite.jar              ← 宿主（桥接 + 模块加载）
  ArcartXSuite/
    config.yml                  ← modules.<id>.enabled
    modules/
      MyModule.jar              ← 第三方或云端模块
    data/<module>/              ← 模块运行时数据
    ui/                         ← 从 Jar 导出的 ArcartX UI
```

- **模块化** — 独立 Jar，热加载，配置一键开关
- **Capability** — 跨模块调用推荐方式，避免直接依赖实现类
- **ArcartX UI 原生** — 统一客户端 UI / HUD 体验
- **ConfigDiagnosticEngine** — 配置结构体检与迁移提示

---

## 参与与反馈

- **Bug / 功能建议** — 在对应仓库提交 [Issue](https://github.com/YOUR_ORG/ArcartXSuite/issues)
- **Pull Request** — 欢迎文档修正与小改进；大功能请先开 Issue 讨论
- **第三方模块** — 使用 [axs-api](https://github.com/YOUR_ORG/ArcartXSuite-Core) 开发，可参考 Wiki [Capability 详解](https://YOUR_ORG.github.io/ArcartXSuite-Wiki/guide/developer/capability-guide)

---

## 相关链接

| | |
|---|---|
| 📖 文档 | https://YOUR_ORG.github.io/ArcartXSuite-Wiki/ |
| ☁️ 云端 | https://cloud.example.com |
| 🏰 ArcartX 社区 | https://arcartx.com |
| 💬 Discord / QQ | *(替换为你的社群链接)* |

---

<div align="center">

<sub>
ArcartX-Suite 与 ArcartX 均为各自项目的商标或品牌名称 · 本组织页面由
<a href="https://github.com/YOUR_ORG/.github">.github/profile</a> 维护
</sub>

<br /><br />

<!-- 可选：GitHub 统计卡片（替换 YOUR_ORG） -->
<!-- ![Stats](https://github-readme-stats.vercel.app/api?username=YOUR_ORG&show_icons=true&theme=default) -->

</div>

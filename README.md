<div align="center">

<img src="https://github.com/user-attachments/assets/959da519-d523-48ce-bb09-b5cad5bbc4af" alt="ArcartX-Suite" width="100%" />

<br /><br />

[![Docs](https://img.shields.io/badge/文档-Wiki-6366f1?style=for-the-badge&logo=readthedocs&logoColor=white)](https://xuanmomo233.github.io/ArcartXSuite-Wiki/)
[![Cloud](https://img.shields.io/badge/云端平台-cloud.021209.xyz-0ea5e9?style=for-the-badge&logo=cloudflare&logoColor=white)](https://cloud.021209.xyz)
[![ArcartX](https://img.shields.io/badge/ArcartX-官方文档-f97316?style=for-the-badge&logo=bookstack&logoColor=white)](https://wiki.arcartx.com/docs)
[![SDK](https://img.shields.io/github/v/release/xuanmomo233/ArcartXSuite-Core?label=axs-api&style=for-the-badge)](https://github.com/xuanmomo233/ArcartXSuite-Core/releases)
[![Community](https://img.shields.io/badge/社区-arcartx.com-8b5cf6?style=for-the-badge&logo=internetarchive&logoColor=white)](https://arcartx.com)

</div>

<br />

## ArcartX-Suite · 服务器玩法的交响组曲

> **Suite — 组曲，亦是套装。**
>
> 26 个模块如同 26 个乐章——每一个独立运作、各具音色、按需启用，
> 共享 ArcartX 的统一调性与 UI 主题，组合成一部属于你自己的 **服务器组曲**。
>
> 「 从登录到击杀，每一帧都是一个音符 」——不只是插件，是服务器玩法的交响组曲。

**ArcartX-Suite（AXS）** 是专为 **ArcartX** 生态构建的下一代全场景 Minecraft 服务器核心套件与玩法基础设施。
一个插件覆盖 **26 个功能领域**，涵盖经济交易、全球市场、抽奖开箱、钓鱼小游戏、称号系统、战令系统、仓库银行等核心玩法，统一 ArcartX UI 体验，模块间深度联动。

采用「宿主 + 独立模块 Jar」架构：宿主统一管理属性/物品/经济桥接、模块加载、跨服传输与配置诊断，**所有业务逻辑在 `modules/*.jar` 中运行**。

> **说明：** ArcartX-Suite 为基于 ArcartX 客户端模组生态构建的**第三方**宿主框架，**不属于 ArcartX 官方插件**。

---

## 生态仓库

| 项目 | 说明 | 链接 |
|------|------|------|
| **ArcartXSuite** | 服务端宿主插件（26 个内置/云端模块） | [仓库](https://github.com/xuanmomo233/ArcartXSuite) |
| **ArcartXSuite-Core** | 模块开发 SDK（`axs-api` 源码 + CI 发布） | [仓库](https://github.com/xuanmomo233/ArcartXSuite-Core) · [Releases](https://github.com/xuanmomo233/ArcartXSuite-Core/releases) |
| **ArcartXSuite-Wiki** | 服主文档、开发者指南、API 参考 | [文档站](https://xuanmomo233.github.io/ArcartXSuite-Wiki/) · [源码](https://github.com/xuanmomo233/ArcartXSuite-Wiki) |
| **ArcartxSuite-CloudPlatform** | AXS Cloud 云端授权与模块分发平台 | [cloud.021209.xyz](https://cloud.021209.xyz) · [源码](https://github.com/xuanmomo233/ArcartxSuite-CloudPlatform) |

---

## 1.2.0-beta 新特性

- **核心本体云端下发** — bootstrap 瘦壳 + 云端下载加密核心 `.axb`，自动更新无需手动替换 jar
- **云端授权平台** — 服主通过 [cloud.021209.xyz](https://cloud.021209.xyz) 注册、购买/领取授权、装备模块到服务器
- **Ed25519 签名验证** — 服务器与云端通信使用 Ed25519 密钥对，支持模块签名防篡改
- **模块 Jar 独立部署** — 全部 26 个模块支持独立 jar，外部 jar 接管时宿主自动跳过内置加载
- **免费模块自动授权** — 注册云端账号后免费模块 license 自动创建，首次绑定服务器自动装备
- **异地绑定安全告警** — 新机器指纹绑定触发安全事件，管理员可审阅

---

## 26 个模块一览

### 免费模块（12 个）

| 模块 | 说明 |
|------|------|
| **RGB** | 渐变文本渲染，PAPI 输出扫光效果 |
| **Pickup** | 物品拾取 HUD 弹出提示 + 扫描器模式 |
| **Announcer** | 公告 / 字幕轮播系统，可点击执行命令 |
| **LoginView** | ArcartX UI 登录/注册面板，支持 AuthMe 桥接 |
| **OnlineRewards** | 在线奖励 / 每日签到 / 连续签到 / 补签卡 |
| **CombatEffect** | 战斗特效（击杀/连击/伤害飘字），四插件属性来源自动检测 |
| **EventPacket** | 事件引擎，9 种触发器 × 11 种动作自由组合 |
| **Prop** | 快捷道具栏，客户端按键绑定临时属性加成 |
| **Essentials** | 基础工具（传送/家/Warp/一键砍树/背包整理/UI 菜单） |
| **Regions** | 区域保护（40+ 标志/优先级继承/世界规则） |
| **Menu** | 配置驱动 ArcartX 菜单系统，ESC 替换、命令/物品绑定 |
| **AfkReward** | 区域挂机 + 原地挂机双模式、周期命令奖励、排行榜 |

### 付费模块（11 个）

| 模块 | 说明 |
|------|------|
| **Title** | 分组称号系统，有效期/品质/套装属性/头顶显示/聊天 Tab 前缀 |
| **Conversation** | NPC 对话引擎，Chemdah + Adyeshach 联动，ArcartX UI 渲染 |
| **Mail** | 邮件系统，玩家写信/预设派发/CDK 兑换/物品附件/跨服广播 |
| **Warehouse** | 仓库银行，个人/共享仓库、多货币银行、定期存款、二级密码 |
| **QuestGPS** | 任务导航，Chemdah 任务追踪、路径寻路 + 3D 模型标记 |
| **Map** | 大地图 / 锚点传送 / 玩家路径点 / 小地图 HUD |
| **BattlePass** | 战令系统，三层通行证 + 日/周/赛季任务池 + ArcartX UI 面板 |
| **Market** | 全球市场，系统商店 + 玩家拍卖行 + 回收商店，多货币跨服同步 |
| **Lottery** | 抽奖系统，CS 开箱滚动动画 + 原神祈愿卡池，保底机制 |
| **Fishing** | 钓鱼系统，星露谷风格小游戏、多水域生态、钓鱼图鉴 |
| **QQBot** | QQ 群服互联，OneBot 11 双向消息同步、QQ-游戏账号绑定 |

### 福利模块（3 个）

| 模块 | 领取条件 | 授权份额 |
|------|----------|----------|
| **Chat** | 任意消费 | 5 |
| **Tab** | 累计消费满 ¥100 | 5 |
| **EntityTracker** | 累计消费满 ¥200 | 5 |

完整配置与依赖见 [Wiki · 模块总览](https://xuanmomo233.github.io/ArcartXSuite-Wiki/modules/)。

---

## AXS Cloud · 云端指挥台

**AXS Cloud** 是为 ArcartX-Suite 组曲服务的云端管理平台——管理服务器注册、模块授权与分发、QQ Bot 配置，让每一首乐章在正确的服务器上奏响。

| 能力 | 说明 |
|------|------|
| 服主账号 | QQ + 密码注册/登录，一账号管理多服 |
| 服务器绑定 | Ed25519 公钥 + 机器指纹 → 获取 `serverCode` |
| 模块授权 | 购买/领取授权，「装备模块」勾选到指定服务器 |
| 加密分发 | 下载 `.axb` 模块包，指纹绑定 AES 解密密钥 |
| 核心下发 | `/v1/core/*`、`/v1/app-jar/*` 宿主 jar 与 bootstrap 分发 |
| 心跳监控 | 在线状态、TPS、玩家数等实时上报 |
| QQ Bot 运维 | OneBot 11 WebSocket，群服互联配置管理 |

**技术栈：** Hono + Drizzle ORM + PostgreSQL · React + Vite + Tailwind CSS · OneBot 11

服主流程：[注册云端账号](https://cloud.021209.xyz) → 配置 `plugins/ArcartX-Suite/config.yml` 的 `cloud` 节 → 装备模块 → 执行 `/axs sync`。详见 [Wiki · 云端模块](https://xuanmomo233.github.io/ArcartXSuite-Wiki/guide/cloud-modules)。

---

## 快速开始

### 服主

1. 安装 **Paper 1.20.1+**（或 Spigot / Mohist）、**ArcartX 服务端插件** 与玩家端 **ArcartX 模组**（[官方文档](https://wiki.arcartx.com/docs)）
2. 将 **ArcartX-Suite** jar 放入 `plugins/`，启动一次生成默认配置
3. 在 [cloud.021209.xyz](https://cloud.021209.xyz) 注册，配置 `cloud.qq` / `apiKey`，装备所需模块
4. 在 `config.yml` 将对应模块 `enabled: true`，执行 `/axs status` 验证
5. 阅读 [Wiki · 快速开始](https://xuanmomo233.github.io/ArcartXSuite-Wiki/guide/)

```yaml
# plugins/ArcartX-Suite/config.yml — 云端绑定（节选）
cloud:
  qq: "你的QQ号"
  apiKey: "从云端「设置 → 验证密匙」复制"
  server-code: ""   # 首次绑定成功后自动回填
```

### 模块开发者

1. 从 [ArcartXSuite-Core Releases](https://github.com/xuanmomo233/ArcartXSuite-Core/releases) 下载 `axs-api-1.2.0-beta.jar`（或 `./gradlew :axs-api:jar` 本地构建）
2. 实现 `AbstractAXSModule`，编写 `module.yml`
3. 将产物放入 `plugins/ArcartXSuite/modules/`，在 `config.yml` 启用
4. 详见 [开发者指南](https://xuanmomo233.github.io/ArcartXSuite-Wiki/guide/developer/) · [Capability 详解](https://xuanmomo233.github.io/ArcartXSuite-Wiki/guide/developer/capability-guide)

```kotlin
dependencies {
    compileOnly(files("libs/axs-api-1.2.0-beta.jar"))
    compileOnly("org.spigotmc:spigot-api:1.20.1-R0.1-SNAPSHOT")
}
```

模块代码中 **只能** `import xuanmo.arcartxsuite.api.*`，**禁止**引用宿主 `bridge.*` 或 `module` 实现类。

---

## 环境要求

| 组件 | 要求 |
|------|------|
| Java | 17+（推荐 21） |
| Minecraft | 1.20.1+（Spigot / Paper / Mohist / Arclight） |
| 客户端 | ArcartX 模组（必装） |
| 数据库 | 默认 SQLite；Market 等模块可选 MySQL |
| 跨服 | Redis + Proxy 双后端 CrossServer SDK（可选） |
| 经济桥接 | Vault / PlayerPoints（按模块选装） |

---

## 宿主基础设施

ArcartXSuite-Core 开源仓库包含宿主参考实现，核心职责包括：

- **属性桥接** — AttributePlus / CraneAttribute / MythicLib / Symphony
- **物品桥接** — MythicMobs / NeigeItems / MMOItems / Overture / Tacz
- **经济桥接** — Vault / PlayerPoints
- **跨服传输** — Redis + Proxy 双后端 CrossServer SDK
- **按键绑定** — 客户端 Keybind 服务
- **账号识别** — 正版 / LittleSkin / 离线
- **配置诊断** — `ConfigDiagnosticEngine` 结构体检与字段迁移
- **模块签名** — Ed25519 签名校验（[`scripts/sign-module.py`](https://github.com/xuanmomo233/ArcartXSuite-Core/blob/main/scripts/sign-module.py)）

```text
plugins/
  ArcartX-Suite.jar              ← 宿主（桥接 + 模块加载 + 云端同步）
  ArcartX-Suite/
    config.yml                   ← modules.<id>.enabled + cloud 配置
    modules/
      MyModule.jar               ← 第三方或云端 .axb 解密模块
    data/<module>/               ← 模块运行时数据
    ui/                          ← 从 Jar 导出的 ArcartX UI
```

---

## 参与与反馈

| 类型 | 去向 |
|------|------|
| 插件 Bug / 功能建议 | [ArcartXSuite Issues](https://github.com/xuanmomo233/ArcartXSuite/issues) |
| 文档修正 / 补全 | [ArcartXSuite-Wiki Issues](https://github.com/xuanmomo233/ArcartXSuite-Wiki/issues) |
| SDK / API 问题 | [ArcartXSuite-Core Issues](https://github.com/xuanmomo233/ArcartXSuite-Core/issues) |
| 云端平台问题 | [ArcartxSuite-CloudPlatform Issues](https://github.com/xuanmomo233/ArcartxSuite-CloudPlatform/issues) |

欢迎 Pull Request 修正文档与小改进；大功能请先开 Issue 讨论。

---

## 相关链接

| | |
|---|---|
| 📖 ArcartX-Suite 文档 | https://xuanmomo233.github.io/ArcartXSuite-Wiki/ |
| ☁️ AXS Cloud 云端平台 | https://cloud.021209.xyz |
| 💻 开源 SDK（axs-api） | https://github.com/xuanmomo233/ArcartXSuite-Core |
| 📝 文档仓库 | https://github.com/xuanmomo233/ArcartXSuite-Wiki |
| 🏰 ArcartX 社区 | https://arcartx.com |
| 🔗 ArcartX 官方文档 | https://wiki.arcartx.com/docs |

---

<div align="center">

<sub>
ArcartX-Suite 当前版本 <strong>1.2.0-beta</strong> ·
本页面存放于 <code>.github/profile/README.md</code> ·
ArcartX 与 ArcartX-Suite 均为各自项目的品牌名称
</sub>

</div>

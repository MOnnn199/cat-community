# 猫咪社区 (Campus Idle / Cat Community)

> 一个面向校园的闲置物品交易与猫咪社区 Android 应用。

## 简介

**猫咪社区** 是一款基于 Android 的校园生活类 App，集成了**闲置物品发布/交易**与**猫咪领养/社区**相关功能。用户可以注册登录、发布与管理自己的闲置商品、按分类浏览商品、收藏感兴趣的商品，并进行评论与互动。

所有数据通过**本地 SQLite** 存储，无需后端服务器即可独立运行，适合作为课程设计 / 学习 Demo。

## 功能特性

- **账户系统**：注册、登录、个人资料查看与修改、修改密码
- **闲置商品**：发布商品、我的商品管理、按分类浏览（首页四大分类）
- **收藏**：收藏 / 取消收藏商品，查看「我的收藏」
- **互动**：商品评论（`ReviewCommodityActivity`）、审核 / 回复
- **本地持久化**：基于 SQLite，包含 User / Student / Commodity / Collection / Review 五类数据
- **主题**：猫咪社区自定义图标与界面资源

## 技术栈

| 类别 | 说明 |
| --- | --- |
| 语言 | Java |
| 平台 | Android（minSdk 21，target / compileSdk 28） |
| 构建 | Gradle 3.6.1 + Android Gradle Plugin 3.6.1，buildTools 29.0.2 |
| UI | Android Support Library 28.0.0（appcompat-v7、constraint-layout、recyclerview-v7） |
| 存储 | Android SQLite（`android.database.sqlite`） |
| 网络 | 无，纯本地单机应用 |

## 环境要求

- Android Studio 3.x / 4.x
- JDK 8
- Android SDK Platform 28 与 Build-Tools 29.0.2
- Gradle 5.6.4（项目已内置 Wrapper）

## 运行方式

1. 克隆仓库：

   ```bash
   git clone https://github.com/MOnnn199/campus-idle-market.git
   ```

2. 用 Android Studio 打开项目根目录（导入 Gradle 工程）。
3. 连接 Android 设备或启动模拟器（API 21+）。
4. 点击 **Run 'app'**，或执行 `./gradlew assembleDebug` 后安装生成的 APK。

## 项目结构

```
app/src/main/java/com/leaf/collegeidleapp/
├── activity/    # 各页面：登录、注册、主页、个人中心、商品发布/管理、收藏、评论等
├── adapter/     # ListView / RecyclerView 适配器
├── bean/        # 数据模型：User、Student、Commodity、Collection、Review、JellyInterpolator
├── util/        # SQLite 帮助类（*DbHelper）
├── view/        # 自定义 View（ListViewInScrollView 等）
└── MainActivity.java
```

## 数据存储

应用使用 5 个 SQLite 表进行本地持久化（见 `app/.../util/*DbHelper`）：

- `UserDbHelper` — 用户账户
- `StudentDbHelper` — 学生信息
- `CommodityDbHelper` — 闲置商品
- `MyCollectionDbHelper` — 收藏
- `ReviewDbHelper` — 商品评论

## 许可证

暂未指定开源许可证。如需使用或二次开发，请联系作者。

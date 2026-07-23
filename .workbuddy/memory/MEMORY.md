# 项目长期记忆

## 猫咪社区 Android App（cat/ 目录）
- 类型：校园闲置物品交易 + 猫咪社区 Android App，包名 `com.leaf.collegeidleapp`。
- 技术：Java，Gradle 3.6.1 / AGP 3.6.1，compileSdk 28，Support Library 28.0.0。
- 数据存储：纯本地 SQLite（`util/*DbHelper`，五张表：User/Student/Commodity/Collection/Review），**无后端、无网络请求**。
- 功能：登录注册、个人中心、发布/管理商品、商品分类、收藏、评论。

## GitHub 仓库
- 主仓库：`MOnnn199/campus-idle-market`（公开，默认分支 master）。
- 认证账号：用户提供的 PAT 属于 **MOnnn199**（非旧远程 yunju-ustc）。
- 旧远程 `yunju-ustc/catshequ` 保留为 `catshequ-old`。
- 本机 `.git/refs/remotes` 无法落盘（沙箱限制），本地 `git status` 显示 `[gone]`，远程正常；推送命令：`git push origin master`（需凭据）。

## 约定
- 前端/构建改动由助手完成，用户只写后端 Java（如后续接入后端）。

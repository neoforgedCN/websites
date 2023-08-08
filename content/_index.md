---
title: "安装程序和模组开发者相关信息"
date: 2023-07-19T09:40:37-04:00
draft: false
categories:
author: cpw (由 DefinitlyEvil 翻译)
summary: |
    NeoForged安装文件和其相关的信息。
description: |
    NeoForged安装文件和其相关的信息。
---
# NeoForged安装文件
你可以在下面找到最新版本的安装程序直链。

{{< files "1.20.1" >}}

注意：这个安装文件仍然较forge因为我们希望可以和其它启动器兼容，希望他们不会硬编码太多东西。

# 使用 NeoForge 开发模组

## 对于新项目

1. 前往 [The MDK] 点击 `Use This Template` 以在 Github 创建一个新的 Git 仓库。
2. 在本地使用 Git 克隆刚刚创建的仓库, 开始开发吧! 我们的 [文档] 和 [Wiki] 是学习的好地方.

## 对于现有项目
你也可以在现有项目中即成 neoforge：
1. 把你的 Maven 仓库改为 `https://maven.neoforged.net/releases` instead of `https://maven.minecraftforge.net`
2. 修改 ForgeGradle 版本为 NeoGradle 6.0.13 或更高:
    ```
    plugins {
        ...
        id 'net.neoforged.gradle' version '[6.0.13, 6.2)'
    }
    ```
3. 更新你的 `minecraft` 依赖来使用 `net.neoforged:forge` （版本如上）.

### 注意
1. 目前不同forge分支构建的模组可能互相不兼容。
2. 最近 ForgeGradle/NeoGradle 的推荐的使用方法有一些变化. 更注意 `settings.gradle` 变化了, 并且 `build.gradle` 中 `buildscript` 部分删除了. 参考 [The MDK] 开查看例子和更多内容.

[The MDK]: https://github.com/neoforged/MDK
[文档]: https://docs.neoforged.net
[Wiki]: https://forge.gemwire.uk

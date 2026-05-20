---
title: Obsidian同步免费实现
categories:
  - 技术
tags:
  - 博客
  - 方法
date: 2026-05-20 11:21:21
---
    我在Obsidian总结了很多笔记，目前了解的方法有官方的付费同步，或者通过飞牛同步+WebDav做中转,如下：
1. **Syncthing（最推荐）** - 免费、开源、点对点同步，不经过第三方云盘。 - 支持 Windows、macOS、Linux、Android。 - 缺点：iOS 不太方便，设备最好经常同时在线。 - 适合：电脑 + Android 手机、多台电脑同步。
2. **Git + 插件** - 用 GitHub/Gitee/GitLab 私有仓库同步 Obsidian 库。 - Obsidian 可安装 `Obsidian Git` 插件自动提交和拉取。 - 优点：有版本历史，适合文本笔记。 - 缺点：图片、PDF、大文件不太适合；手机端配置麻烦。 - 适合：主要在电脑上写笔记，懂一点 Git。
3. **云盘同步** - Windows/macOS：OneDrive、Google Drive、Dropbox、坚果云等。 - 把 Obsidian vault 放进云盘目录即可。 - 优点：简单。 - 缺点：移动端尤其 iOS/Android 不一定能直接稳定同步 Obsidian 文件夹；可能出现冲突文件。 - 适合：主要电脑端使用。
4. **Remotely Save 插件** - Obsidian 插件，可同步到 WebDAV、S3、Dropbox、OneDrive 等。 - 搭配坚果云 WebDAV 可以免费使用一定额度。 - 优点：移动端也比较方便。 - 缺点：插件同步不如官方 Sync 稳，首次配置稍麻烦。 - 适合：需要手机和电脑同步，尤其不想折腾 Git。
5. **iCloud** - 如果你全是 Apple 设备，可以把 vault 放在 iCloud Drive。 - 优点：最省事。 - 缺点：Windows 上体验一般，偶尔有同步延迟。

我自己实现的是通过**Syncthing+Syncthomh-fork** 实现Windows和Android
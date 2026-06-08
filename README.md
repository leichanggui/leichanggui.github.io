# leichanggui.github.io

雷常贵的个人主页，使用 Jekyll 和 GitHub Pages 构建。

## 站点结构

```text
.
├── _config.yml                 # 站点配置、导航、个人信息
├── _layouts/
│   ├── default.html            # 主布局
│   └── post.html               # 笔记文章布局
├── _posts/                     # Notes 页面文章
├── assets/main.css             # 全站样式
├── index.html                  # 首页
├── research.md                 # 研究方向
├── projects.md                 # 项目展示
├── publications.md             # 成果列表
├── notes.md                    # 技术笔记
└── contact.md                  # 联系方式
```

## 更新个人信息

优先编辑 `_config.yml`：

- `profile.name`
- `profile.role`
- `profile.org`
- `profile.bio`
- `profile.avatar`
- `email`
- `social`

## 添加笔记

在 `_posts/` 下创建 Markdown 文件，文件名格式：

```text
YYYY-MM-DD-title.md
```

示例 front matter：

```yaml
---
layout: post
title: "文章标题"
date: 2026-06-08 10:00:00 +0800
categories: notes
tags: [post-GWAS, single-cell]
---
```

## 发布

推送到 `main` 分支后，GitHub Actions 会自动构建 Jekyll 并发布到：

https://leichanggui.github.io/

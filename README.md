# 个人博客站点

这是一个使用 Jekyll 和 GitHub Pages 搭建的个人博客站点。

## 项目结构

```
leichanggui.github.io/
├── _config.yml          # Jekyll 配置文件
├── _posts/              # 博客文章目录
│   └── 2024-12-19-welcome-to-jekyll.md
├── _layouts/            # 布局模板
│   ├── default.html
│   └── post.html
├── assets/              # 静态资源
│   └── main.css
├── index.html           # 首页
├── about.md             # 关于页面
├── Gemfile              # Ruby 依赖
├── .gitignore           # Git 忽略文件
└── README.md            # 项目说明
```

## 本地开发环境搭建

### 1. 安装 Ruby 和 Jekyll

**Windows 系统：**

1. 下载并安装 [RubyInstaller for Windows](https://rubyinstaller.org/)
2. 安装完成后，打开命令行工具，运行：

```bash
gem install jekyll bundler
```

**macOS 系统：**

```bash
gem install jekyll bundler
```

**Linux 系统：**

```bash
sudo apt-get install ruby-full build-essential zlib1g-dev
gem install jekyll bundler
```

### 2. 安装项目依赖

在项目根目录下运行：

```bash
bundle install
```

### 3. 启动本地服务器

```bash
bundle exec jekyll serve
```

或者：

```bash
jekyll serve
```

服务器启动后，访问 `http://localhost:4000` 即可预览博客。

### 4. 构建静态网站

```bash
bundle exec jekyll build
```

构建后的文件会生成在 `_site` 目录中。

## 部署到 GitHub Pages

### 1. 创建 GitHub 仓库

1. 登录 GitHub 账号
2. 创建新仓库，仓库名必须为：`leichanggui.github.io`
3. 将仓库设置为 Public（公开）

### 2. 推送代码到 GitHub

```bash
git init
git add .
git commit -m "Initial commit: Jekyll blog setup"
git branch -M main
git remote add origin https://github.com/leichanggui/leichanggui.github.io.git
git push -u origin main
```

### 3. 启用 GitHub Pages

1. 进入仓库设置页面（Settings）
2. 在左侧菜单找到 "Pages"
3. 在 "Source" 部分选择 "Deploy from a branch"
4. 选择分支 `main` 和文件夹 `/ (root)`
5. 点击 "Save"

等待几分钟后，你的博客就可以通过 `https://leichanggui.github.io` 访问了！

## 编写新文章

1. 在 `_posts` 目录下创建新的 Markdown 文件
2. 文件名格式：`YYYY-MM-DD-文章标题.md`
3. 文件开头需要包含 Front Matter：

```yaml
---
layout: post
title:  "文章标题"
date:   2024-12-19 10:00:00 +0800
categories: 分类
tags: [标签1, 标签2]
---
```

4. 然后编写文章内容（使用 Markdown 语法）
5. 保存后提交并推送到 GitHub：

```bash
git add _posts/YYYY-MM-DD-文章标题.md
git commit -m "Add new post: 文章标题"
git push
```

## 自定义配置

编辑 `_config.yml` 文件可以修改：

- 站点标题和描述
- 作者信息
- 社交媒体链接
- 主题设置
- 其他 Jekyll 配置选项

修改后需要重启 Jekyll 服务器才能生效。

## 样式定制

- 修改 `assets/main.css` 来自定义样式
- 或者使用 Jekyll 主题（在 `_config.yml` 中配置）

## 更多资源

- [Jekyll 官方文档](https://jekyllrb.com/)
- [GitHub Pages 文档](https://docs.github.com/en/pages)
- [Markdown 语法指南](https://www.markdownguide.org/)

## 许可证

本项目采用 MIT 许可证。

---

**注意：** 记得将 `_config.yml` 中的邮箱地址替换为你的真实邮箱。


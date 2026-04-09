# Nyima's Blog

基于 [Hexo](https://hexo.io) + [Fluid 主题](https://github.com/fluid-dev/hexo-theme-fluid) 搭建的个人技术博客，通过 GitHub Pages 托管。

## 🚀 快速部署到 GitHub Pages

### 第一步：创建 GitHub 仓库

1. 登录 [GitHub](https://github.com)，点击右上角 **"+"** → **"New repository"**
2. 仓库名设置为 `你的用户名.github.io`（例如 `nyima.github.io`）
3. 选择 **Public**（公开），点击 **"Create repository"**

### 第二步：上传项目代码

**方法 A：通过 Git 命令行（推荐）**

```bash
# 1. 克隆你的新仓库
git clone https://github.com/你的用户名/你的用户名.github.io.git
cd 你的用户名.github.io

# 2. 将本项目的所有文件复制进去（除了 .git 文件夹）
# 或者直接在仓库目录中创建所有文件

# 3. 添加、提交并推送
git add .
git commit -m "Initial commit: Hexo blog with Fluid theme"
git branch -M main
git push -u origin main
```

**方法 B：通过 GitHub 网页上传**

1. 打开你的仓库页面
2. 点击 **"Add file"** → **"Upload files"**
3. 将项目中的所有文件拖拽上传
4. 填写 commit message，点击 **"Commit changes"**

### 第三步：启用 GitHub Pages

1. 打开仓库 → **Settings** → **Pages**
2. **Source** 选择 **"GitHub Actions"**
3. 等待 Actions 自动构建部署完成（约 1-2 分钟）
4. 访问 `https://你的用户名.github.io` 查看博客

> ⚠️ 推送代码后，GitHub Actions 会自动构建并部署，无需手动操作。

## 📁 项目结构

```
hexo-blog/
├── _config.yml              # Hexo 主配置文件
├── _config.fluid.yml        # Fluid 主题配置文件
├── package.json             # Node.js 依赖
├── .gitignore               # Git 忽略规则
├── scaffolds/               # 文章模板
│   ├── post.md
│   ├── draft.md
│   └── page.md
├── source/                  # 博客源文件
│   ├── _posts/              # 博客文章（Markdown）
│   │   └── java-concurrency.md
│   ├── about/               # 关于页面
│   ├── archives/            # 归档页面
│   ├── categories/          # 分类页面
│   └── tags/                # 标签页面
├── themes/                  # 主题目录
│   └── fluid/               # Fluid 主题（通过 npm 安装）
└── .github/
    └── workflows/
        └── deploy.yml       # GitHub Actions 自动部署配置
```

## ✏️ 本地开发

### 环境要求

- [Node.js](https://nodejs.org/) >= 18
- [Git](https://git-scm.com/)

### 安装与运行

```bash
# 1. 安装依赖
npm install

# 2. 本地预览（实时刷新）
hexo server

# 3. 生成静态文件
hexo generate

# 4. 清除缓存
hexo clean
```

浏览器打开 `http://localhost:4000` 即可预览。

## 📝 写新文章

在 `source/_posts/` 目录下创建新的 `.md` 文件，格式如下：

```markdown
---
title: 文章标题
date: 2024-01-15 10:00:00
tags:
  - 标签1
  - 标签2
categories:
  - 分类
---

文章正文内容...
```

或使用命令快速创建：

```bash
hexo new "文章标题"
```

## ⚙️ 自定义配置

| 文件 | 说明 |
|------|------|
| `_config.yml` | Hexo 主配置：站点标题、URL、部署等 |
| `_config.fluid.yml` | 主题配置：导航栏、外观、侧边栏、评论等 |

### 需要修改的地方

1. **`_config.yml`** 中的 `url` 改为你的 GitHub Pages 地址
2. **`_config.fluid.yml`** 中的 `navbar.blog_title` 改为你的名字
3. **`_config.fluid.yml`** 中的 `about` 部分改为你的个人信息
4. 将 `yourusername` 替换为你的实际 GitHub 用户名

## 📜 License

[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

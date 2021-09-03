---
title: "Resume: a zola theme"
date: 2021-09-03T13:30:54.712Z
description: "Resume: a zola theme"
extra:
  link: https://github.com/AlongWY/zola-resume
  image: /media/open-source.png
---
# Zola Resume


## 快速开始

```bash
git clone git@github.com:alongwy/zola-resume.git
cd zola-resume
zola serve
# open http://127.0.0.1:1111/
```

**此方法之后更新主题可能比较麻烦**

## 安装

### 第一步: 初始化网站

```bash
zola init mysite
```

### Step 2: 安装 zola-resume
安装该主题到`themes`目录:

```bash
cd mysite/themes
git clone git@github.com:alongwy/zola-resume.git
```

或者使用 submodule 安装:

```bash
cd mysite
git init  # if your project is a git repository already, ignore this command
git submodule add git@github.com:alongwy/zola-resume.git themes/zola-resume
```

### Step 3: 配置网站
在配置文件中 `config.toml` 开启本主题:

```toml
theme = "zola-resume"
```

或者直接复制 `config.toml.example` 到本目录:

```bash
cp themes/zola-resume/config.toml.example config.toml
```

### Step 4: 添加/修改内容
然后复制:

```
cp -r themes/zola-resume/data .
cp -r themes/zola-resume/content .
```

你可以修改或者添加新内容到 `content/blog`, `content/projects` 等目录，注意其中的 `_index.md` 不要删除。

### Step 5: 运行项目
使用如下命令查看效果:

```
zola serve
```

打开 http://127.0.0.1:1111 查看效果。


### Step 6: 自动构建

复制 github actions 配置文件：

```bash
mkdir -p .github/workflows
cp themes/zola-resume/build.yml .github/workflows/build.yml
```

## 配置 CMS 系统

### Step 1: 修改配置文件

复制 cms 配置文件:

```bash
cp themes/zola-resume/static/admin/config.yml static/admin/config.yml
```

并修改如下部分:

```yaml
# static/admin/config.yml

backend:
  name: github
  repo: USERNAME/REPO             # <-- 记得修改
  branch: BRANCH                  # <-- 记得修改
  cms_label_prefix: netlify-cms/
  site_domain: DOMAIN.netlify.com # 记下来这个位置，之后会用到
```

## 配置后台认证

首先到 [Netlify](https://netlify.com) 注册账号并配置仓库，这个时候会自动构建失败，不用管它。

进入网站 setting 的 `Build & deploy` 选项把 `Build settings` 的 `active` 关掉，这样就不会消耗 netlify 的自动构建时长。

进入 setting 的 `Access control` 找到其中的 `OAuth`，`Install provider` 把 Github 装上。其中的 github app 可以查看这个[文档](https://docs.netlify.com/visitor-access/oauth-provider-tokens/)进行配置。

最后在 setting 的 `Custom domains` 里面添加 `YOURNAME.github.io`，会有警告，但是不用管他，前面有一个 `Default subdomain`，把他记下来填到 `static/admin/config.yml` 里面的 `backend.site_domain` 里面去。


### About 主页
修改 `contents/_index.md` 来改变主页内容

### 其他文件

- [data/certifications.json](https://github.com/AlongWY/zola-resume/blob/main/data/certifications.json)
- [data/social.json](https://github.com/AlongWY/zola-resume/blob/main/data/social.json)
- [data/skills.json](https://github.com/AlongWY/zola-resume/blob/main/data/skills.json)
- [data/experience.json](https://github.com/AlongWY/zola-resume/blob/main/data/experience.json)
- [data/education.json](https://github.com/AlongWY/zola-resume/blob/main/data/education.json)




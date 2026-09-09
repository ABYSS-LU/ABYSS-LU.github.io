# Personal Academic Homepage

这是一个可以直接部署到 GitHub Pages 的个人学术主页框架。页面中的个人资料集中保存在 `_data/profile.yml`，通常不需要修改 HTML。

## 1. 填写个人资料

打开 `_data/profile.yml`，依次替换里面的占位内容：

- 姓名、身份、单位、所在地和个人简介
- 研究方向
- 邮箱、GitHub、Google Scholar、ORCID 和简历链接
- News、教育经历、工作经历、论文、项目、奖项和学术服务

不需要展示某一整个栏目时，把对应列表改成空列表，例如：

```yaml
awards: []
service: []
```

不需要展示某个链接时，将它留空：

```yaml
linkedin: ""
```

## 2. 替换头像和简历

把头像放到 `assets/images/`，然后修改 `_data/profile.yml`：

```yaml
avatar: "/assets/images/your-photo.jpg"
```

建议使用比例接近 1:1、尺寸不小于 500 × 500 的 JPG、PNG 或 WebP 图片。

把 PDF 简历命名为 `cv.pdf` 并放到 `assets/files/`。如果暂时没有简历，把链接留空：

```yaml
cv: ""
```

## 3. 添加论文和项目

复制 `_data/profile.yml` 中现有的论文或项目条目，再替换内容。注意保持 YAML 缩进一致。包含冒号的文本应放在引号中。

## 4. 本地预览

如果机器上已经安装 Jekyll，可以运行：

```bash
bundle exec jekyll serve
```

然后访问 `http://127.0.0.1:4000`。也可以直接推送到 GitHub，通过 GitHub Pages 构建。

## 5. 发布到 GitHub Pages

在 GitHub 创建名为 `<你的用户名>.github.io` 的仓库，然后确认本地远程地址属于你：

```bash
git remote set-url origin https://github.com/<你的用户名>/<你的用户名>.github.io.git
git add .
git commit -m "Build personal academic homepage"
git push -u origin main
```

进入 GitHub 仓库的 **Settings → Pages**，选择从 `main` 分支发布。网站地址通常是：

```text
https://<你的用户名>.github.io
```

## 文件说明

- `_data/profile.yml`：个人资料，今后主要修改这个文件
- `_layouts/academic.html`：页面结构
- `assets/css/academic.css`：颜色、排版和移动端样式
- `assets/images/`：头像和其他图片
- `assets/files/`：简历等下载文件
- `_config.yml`：Jekyll 基础设置

## License and attribution

This repository retains the original MIT license and attribution for components derived from [jekyll-theme-WuK](https://github.com/wu-kan/jekyll-theme-WuK).

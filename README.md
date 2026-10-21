# Yingjie Xu — Academic Homepage

直接使用 [AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io) 模板，与参考站 https://ltt-o.github.io/ 使用同一上游。模板布局、SCSS、字体、图标和导航脚本均保留；授权见 `LICENSE`，上游提交见 `TEMPLATE_SOURCE.json`。

## 内容

- About Me：HKUST(GZ) 博士生，导师 Ying-Cong Chen；研究方向为重建、生成和具身智能。
- Publications：8 篇论文，只列标题、作者、会议和链接，不包含论文简介和图片。
- Honors and Awards：RoboMaster 2022 全国一等奖、中部赛区亚军（团队奖项，附来源）。
- Education：2020–2024 华南理工；2024–2026 HKUST(GZ) M.Phil.；2026 至今 HKUST(GZ) Ph.D.。
- Google Scholar：https://scholar.google.com/citations?user=TyoprpUAAAAJ&hl=en

不包含 News。2026-10-21 核对 Scholar 的 7 条记录，新增 WorldLines，并保留本人指定但尚未列入该 Scholar 页的机器人 ICL 综述，合计 8 篇。WorldLines 的 EMNLP 2026 录用信息来自 arXiv 原文 comments。

## 修改资料

1. `_config.yml`：姓名、邮箱、学校、GitHub、Google Scholar、头像。
2. `_pages/about.md`：个人简介、论文、荣誉、教育经历。
3. `_data/navigation.yml`：顶部菜单。
4. `images/avatar.png`：头像文件，目前为自己的 GitHub 头像；可以直接替换为照片。

`_data/profile.json` 是迁移时保留的资料快照；实际页面由 `_config.yml` 和 `_pages/about.md` 生成。引文与奖项核对记录见 `sources.json`。

## 本地运行

需要 Ruby 3.3 和 Bundler：

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1 --port 8000
```

访问 http://127.0.0.1:8000/ 。如需仅构建静态文件：

```sh
bundle exec jekyll build
```

输出位于 `_site/`。不能再用简单 HTTP 服务直接展示源码目录；预览静态输出时应服务 `_site/`。

## 发布到 GitHub Pages

1. 在 HKCLynn 账号下创建公开仓库 `hkclynn.github.io`，提交本项目到 `main`。
2. 仓库 **Settings → Pages → Build and deployment → Source** 选择 **Deploy from a branch**。
3. 选择 **main / (root)** 并保存，GitHub Pages 会构建 Jekyll 模板。
4. 部署完成后访问 https://hkclynn.github.io/ 。

不要添加 `.nojekyll`，它会让 GitHub 跳过模板构建。无需启用 Scholar 爬虫或添加任何定时任务。

原模板完整文档保存在 `docs/TEMPLATE_README.md`。

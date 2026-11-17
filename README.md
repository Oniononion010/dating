# 约会邀约小程序（GitHub Pages 部署包）

## 目录结构
```
.
├── index.html        # 页面入口（GitHub Pages 必须叫这个名字）
└── assets/
    └── dog.jpg       # 头像图
```

## 上线方式一：网页端拖拽（不用装 git，最省事）
1. 登录 GitHub，右上角 `+` → `New repository`
   - 名称随意，比如 `date-h5`；设为 **Public**；不要勾选初始化 README。
2. 进入仓库，点 `Add file` → `Upload files`，把本文件夹里的 `index.html` 和 `assets` 整个拖进去，Commit。
3. 仓库顶部 `Settings` → 左侧 `Pages`：
   - `Source` 选 `Deploy from a branch`
   - `Branch` 选 `main`，文件夹 `/ (root)`，保存。
4. 等 1 分钟左右，回到 Pages 页面，会出现网址：
   `https://<你的用户名>.github.io/date-h5/`

## 上线方式二：命令行（已装 git）
```bash
cd 本文件夹
git init
git add .
git commit -m "date h5"
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```
然后去仓库 `Settings → Pages`，Branch 选 `main / root` 保存即可。

## 注意
- 仓库必须 **Public**（免费 Pages 私有仓库需 Pro）。
- `index.html` 和 `assets/` 不要拆开，否则头像裂图。
- 想改文案、菜品、时间选项，直接编辑 `index.html`，重新 commit + push，Pages 会自动更新。

# ShapeSki AI - 部署指南

## 方案一：Netlify Drop（最快，30秒上线）

最适合 MVP 快速验证，无需安装任何工具。

**操作步骤：**

1. 打开浏览器访问：https://app.netlify.com/drop
2. 直接将 `index.html` 文件拖入页面
3. 获得一个类似 `random-name-123.netlify.app` 的免费域名
4. 上线完成！

> Netlify Drop 每次重启域名会变，适合 MVP 验证。正式版推荐关联 GitHub 仓库。

---

## 方案二：Vercel（推荐，稳定免费）

**步骤 1：安装 Vercel CLI**
```bash
npm install -g vercel
```

**步骤 2：登录**
```bash
vercel login
```
（按提示输入邮箱，在邮箱中确认）

**步骤 3：部署**
```bash
# 进入项目目录
cd C:\Users\44613\WorkBuddy\2026-05-20-task-1

# 一键部署
vercel

# 按提示选择：
# - Set up and deploy?  → Y
# - Which scope?        → 选择你的账号
# - Link to existing project? → N
# - Project name?        → shapeski-ai
# - Directory?           → ./
# - Override settings?   → N
```

**步骤 4：生产环境部署**
```bash
vercel --prod
```

部署成功后会获得类似 `https://shapeski-ai.vercel.app` 的免费域名。

---

## 方案三：GitHub Pages（完全免费，永久免费域名）

**步骤 1：创建 GitHub 仓库**
1. 打开 https://github.com/new
2. 仓库名：`shapeski-ai`
3. 选择 Public
4. 点击 Create repository

**步骤 2：上传文件**
```bash
cd C:\Users\44613\WorkBuddy\2026-05-20-task-1
git init
git add index.html
git commit -m "feat: init ShapeSki AI MVP"
git branch -M main
git remote add origin https://github.com/你的用户名/shapeski-ai.git
git push -u origin main
```

**步骤 3：开启 GitHub Pages**
1. 进入仓库 → Settings → Pages
2. Source 选择 `main` 分支和 `/ (root)` 文件夹
3. 点击 Save

等待 1-2 分钟，你的网站就会上线：`https://你的用户名.github.io/shapeski-ai/`

---

## 域名绑定（可选）

获得免费域名后，可以绑定自定义域名：

| 平台 | 操作 |
|------|------|
| Vercel | Settings → Domains → 添加域名 |
| Netlify | Site settings → Domain management → Add custom domain |
| GitHub Pages | Settings → Pages → Custom domain |

推荐域名注册商：阿里云、腾讯云、Namecheap

---

## 一键部署脚本

创建 `deploy.bat` 文件，双击即可部署：

```batch
@echo off
echo ==============================
echo   ShapeSki AI 快速部署脚本
echo ==============================
echo.
echo 请选择部署方式：
echo   1. Vercel (推荐)
echo   2. GitHub Pages
echo   3. 打开 Netlify Drop
echo.
set /p choice=请输入选项 (1/2/3):

if "%choice%"=="1" (
    echo 正在安装并部署到 Vercel...
    call npm install -g vercel
    call vercel --prod
) else if "%choice%"=="2" (
    echo 请先在 GitHub 创建仓库，然后运行以下命令：
    echo   git init
    echo   git add index.html
    echo   git commit -m "init"
    echo   git remote add origin 你的仓库地址
    echo   git push -u origin main
) else if "%choice%"=="3" (
    start https://app.netlify.com/drop
)

echo.
echo 部署完成！
pause
```

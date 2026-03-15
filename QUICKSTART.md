# 快速入门指南
==============

## 30秒快速开始
---------------

### 第一步：准备文件
确保你有以下文件在 `JunshiCheat` 文件夹中：
- JunshiCheat.mm
- .github/workflows/simple-build.yml
- 其他文件...

### 第二步：创建 GitHub 仓库
1. 打开 https://github.com/new
2. 仓库名填 `JunshiCheat`
3. 点击 "Create repository"

### 第三步：推送代码
打开 PowerShell，运行：

```powershell
cd "e:\桌面\新建文件夹 (3)\JunshiCheat"
git init
git add .
git commit -m "First commit"
git branch -M main
git remote add origin https://github.com/你的用户名/JunshiCheat.git
git push -u origin main
```

**注意**：把 `你的用户名` 换成你实际的 GitHub 用户名！

### 第四步：查看构建
1. 打开你的 GitHub 仓库
2. 点击顶部的 "Actions" 标签
3. 等待几分钟，构建会自动开始
4. 构建完成后，点击下载 Artifacts

## 常见问题检查清单
------------------

### ✅ 检查清单
- [ ] 文件在 `.github/workflows/` 文件夹中吗？
- [ ] 工作流文件以 `.yml` 结尾吗？
- [ ] GitHub Actions 在仓库设置中启用了吗？
- [ ] 推送到了 `main` 或 `master` 分支吗？

### 🔧 如果 Actions 没有运行
1. 进入仓库设置 → Actions → General
2. 选择 "Allow all actions and reusable workflows"
3. 保存

### 🔧 如果想手动触发构建
1. 点击 Actions 标签
2. 选择 "Simple Build" 工作流
3. 点击 "Run workflow" 按钮
4. 点击绿色的 "Run workflow"

## 就这么简单！
---------------

如果还有问题，查看详细的 [GITHUB_SETUP.md](GITHUB_SETUP.md)

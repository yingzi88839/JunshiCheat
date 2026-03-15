# GitHub 设置指南
==================

## 前置要求
-----------
1. 一个 GitHub 账号
2. Git 已安装在你的电脑上

## 步骤 1：创建新仓库
-------------------
1. 访问 https://github.com/new
2. 填写仓库信息：
   - Repository name: `JunshiCheat`（或你喜欢的名称）
   - Description: 军师超自然作弊插件
   - 选择 **Public** 或 **Private**
   - **不要**勾选 "Initialize this repository with a README"
   - **不要**添加 .gitignore
   - **不要**选择许可证
3. 点击 "Create repository"

## 步骤 2：初始化本地仓库
------------------------
打开命令行（PowerShell 或 CMD），进入你的项目文件夹：

```bash
cd "e:\桌面\新建文件夹 (3)\JunshiCheat"
```

## 步骤 3：初始化 Git
-------------------
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
```

## 步骤 4：连接到 GitHub
-----------------------
将以下命令中的 `YOUR_USERNAME` 替换为你的 GitHub 用户名：

```bash
git remote add origin https://github.com/YOUR_USERNAME/JunshiCheat.git
git push -u origin main
```

## 步骤 5：推送代码后检查
------------------------
1. 访问你的 GitHub 仓库页面
2. 点击 "Actions" 标签
3. 你应该能看到一个工作流正在运行或已经完成
4. 如果工作流失败，点击它查看错误信息

## 常见问题
-----------

### 问题 1：Actions 没有自动运行
**解决方案：**
- 确保你的文件在 `.github/workflows/` 目录中
- 确保工作流文件名以 `.yml` 结尾
- 检查分支名称是否匹配（main 或 master）
- 在仓库设置中启用 GitHub Actions：
  Settings → Actions → General → Allow all actions and reusable workflows

### 问题 2：工作流运行失败
**解决方案：**
- 点击失败的工作流查看详细日志
- 检查是否有编译错误
- 确保源文件存在

### 问题 3：如何手动触发构建
**解决方案：**
1. 访问你的仓库
2. 点击 "Actions" 标签
3. 选择 "Simple Build" 工作流
4. 点击 "Run workflow" 按钮
5. 选择分支并点击 "Run workflow"

## 下载构建产物
--------------
1. 工作流成功完成后
2. 点击该工作流运行记录
3. 向下滚动到 "Artifacts" 部分
4. 点击 "JunshiCheat-dylib" 下载
5. 解压下载的 ZIP 文件，里面包含编译好的 dylib

## 验证文件结构
--------------
确保你的仓库有以下文件结构：

```
JunshiCheat/
├── .github/
│   └── workflows/
│       ├── build.yml
│       ├── build-theos.yml
│       └── simple-build.yml
├── .gitignore
├── CMakeLists.txt
├── JunshiCheat.mm
├── JunshiCheat.xm
├── Makefile
├── README.md
├── TRANSLATED.md
├── build.sh
└── control
```

## 快速测试
-----------
如果不确定，可以先使用 `simple-build.yml` 进行测试，它只编译 arm64 架构，更简单快速。

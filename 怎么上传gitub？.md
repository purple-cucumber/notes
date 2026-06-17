# GitHub 上传代码极简指南

> 适用场景：已在本地用 `git init` 初始化仓库，想把它推送到 GitHub 空仓库。

## 1. 在 GitHub 创建空仓库

1. 登录 GitHub，点右上角 **+** → **New repository**
2. 输入仓库名（例如 `num1`）
3. 选择 Public / Private
4. **不要勾选** README、.gitignore、License
5. 点击 **Create repository**

## 2. 复制三行推送命令

创建后页面会显示 **“…or push an existing repository from the command line”**，下面三行就是：

```bash
git remote add origin https://github.com/你的用户名/仓库名.git
git branch -M main
git push -u origin main
```
## 3.以后每天如何上传
写完代码后，在终端里依次执行：
```bash
git add .                    # 暂存所有更改
git commit -m "描述信息"      # 提交到本地仓库
git push                     # 推送到 GitHub
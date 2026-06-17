# GitHub 上传代码极简指南

> 适用场景：已在本地用 `git init` 初始化仓库，想把它推送到 GitHub 空仓库。

## 1. 在 GitHub 创建空仓库

1. 登录 GitHub，点右上角 **+** → **New repository**
2. 输入仓库名（例如 `num1`）
3. 选择 Public / Private
4. **不要勾选** README、.gitignore、License
5. 点击 **Create repository**

## 2.怎么初始化仓库
依次执行：

```bash
# 1. 初始化本地仓库
git init

# 2. 添加文件（假设你已经有笔记文件，比如 github-upload-guide.md）
git add .

# 3. 提交到本地仓库（这一步必须有，否则推送会报错）
git commit -m "初始提交：添加GitHub上传指南笔记"

```

## 3. 复制三行推送命令

创建后页面会显示 **“…or push an existing repository from the command line”**，下面三行就是：

```bash
git remote add origin https://github.com/你的用户名/仓库名.git
git branch -M main
git push -u origin main
```
## 4.以后每天如何上传
写完代码后，在终端里依次执行：
```bash
git add .                    # 暂存所有更改
git commit -m "描述信息"      # 提交到本地仓库
git push                     # 推送到 GitHub
```
## 5.主播主播，怎么修改文件啊？
更新完改成
```bash
git add .                     # 告诉 Git：“我改好了，准备记录这些改动”
git commit -m "描述做了什么"  # 给这次改动贴个标签，方便以后回忆
git push                      # 同步到 GitHub，点亮小绿点
```
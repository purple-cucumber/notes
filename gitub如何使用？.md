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
## 6.怎么下载gitub上的东西
### 🎯 方法一：直接下载 ZIP（最简单，无需安装任何软件）

如果你只是想快速拿到整个项目的代码，不需要跟 GitHub 保持同步，这是最直接的方法。

1. 打开你想下载的 GitHub 仓库页面。
2. 找到页面右上方的绿色按钮 **`<> Code`**，点击它。
3. 在下拉菜单中，选择 **`Download ZIP`**。
4. 下载完成后，解压这个 ZIP 文件就行了。

---

### 💻 方法二：使用 `git clone` 命令（推荐，方便后续更新）

如果你想长期关注这个项目，并能随时获取更新，推荐用这个方法。它会完整地把整个项目（包括所有修改历史）下载到你的电脑上。

#### 第一步：安装 Git
如果电脑上还没有 Git，需要先安装。可以去 [Git 官网](https://git-scm.com/) 下载安装包，按照默认选项安装就行。

#### 第二步：获取仓库地址
回到 GitHub 项目主页，点击绿色的 **`<> Code`** 按钮。在弹出的菜单里，**确保选中 "HTTPS" 标签**，然后点击地址栏旁边的复制按钮。地址通常长这样：
    ```bash
    https://github.com/用户名/项目名.git
    ```

#### 第三步：在终端中执行克隆命令
1. 打开你的终端（在 PyCharm 底部点击 `Terminal` 就可以）或 Git Bash。
2. 使用 `cd` 命令切换到你想存放项目的目录，比如：
    ```bash
    cd D:\桌面\python_test
    ```
等待命令执行完毕，项目文件夹就会出现在你的当前目录下。

小提示：如果下载太慢，可以试试用国内的代码托管平台 Gitee（码云） 上的镜像仓库，速度会快很多
### ✂️ 方法三：只下载单个文件或文件夹（按需获取）

如果项目很大，但你只需要其中的一个文件或文件夹，可以试试下面这些方法。

#### 使用浏览器插件

在 Firefox 等浏览器上安装 **"GitHub Downloader"** 这类插件，就能在仓库页面上直接点击下载单个文件或文件夹。

#### 使用命令行工具 (ghcd)

这是一个 Python 工具，可以不克隆整个仓库，直接下载指定内容。

#### 1. 安装

    ```bash
    pip install github-content-downloader
    ```
#### 2、下载文件夹
```bash
ghcd https://github.com/用户名/项目名/blob/分支名/文件路径
```
#### 3. 下载文件
```bash
ghcd https://github.com/用户名/项目名/blob/分支名/文件路径
```
小提示：使用 ghcd 工具前，请确保已安装 Python 和 pip。如果下载过程中遇到权限问题，可以尝试在终端（以管理员身份运行）中执行安装命令。

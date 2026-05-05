# Git / GitHub / GitHub Pages / ECS：给社科同学的 10 分钟入门

## 0. 开场：为什么社科同学也需要这些工具

做研究项目时，我们经常遇到这些问题：

- 文件名越来越长：`论文最终版`、`论文最终版2`、`论文真的最终版`。
- 合作者不知道谁改了哪一段。
- 想展示一个课程项目，却只能发压缩包或网盘链接。
- 想让一个小网页、问卷工具、数据看板一直在线，却不知道放在哪里。

Git、GitHub、GitHub Pages 和 ECS 解决的是同一条链路上的不同问题：**记录变化、线上协作、公开展示、运行服务**。

## 1. Git：可回退的研究日志

Git 是一个版本控制工具。它最朴素的作用是：记录项目什么时候改了什么，必要时可以回到过去。

你可以把 Git 想成论文或数据项目的“时间机器”：

- 每次重要修改都做一次 `commit`，相当于保存一个清楚的版本节点。
- 写错了可以回退，不用靠复制一堆文件夹自救。
- 多个人协作时，可以知道谁在什么时候改了哪一部分。
- `branch` 像开一条试验路线，不影响主线成果。

官方解释见：[Git 官方书：About Version Control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)。

![Git version control screenshot](assets/screenshots/git-version-control.png)

看这里：红框标出的是 Git 官方书对“版本控制”的解释。对社科项目来说，版本控制不只适用于代码，也适用于论文、访谈提纲、清洗脚本、数据字典和项目文档。

## 2. GitHub：线上项目资料室

Git 是本地工具，GitHub 是线上平台。GitHub 可以托管 Git 仓库，让项目可以被保存、展示、协作和讨论。

把 GitHub 想成一个“线上项目资料室”：

- `repository` 仓库：一个项目的完整文件夹。
- `README.md`：项目门面，别人点进来第一眼看到的说明。
- `commit`：一次有说明的修改记录。
- `Issues`：问题清单、讨论区、待办事项。
- `Pull Request`：把一组修改拿出来给别人检查和合并。

GitHub 新手教程见：[Hello World](https://docs.github.com/get-started/start-your-journey/hello-world)。

![GitHub hello world screenshot](assets/screenshots/github-hello-world.png)

看这里：GitHub 的新手教程会带你认识仓库、分支、提交和 Pull Request。对没有计算机基础的同学来说，先把它理解成“项目资料室 + 修改记录 + 协作流程”就够了。

## 3. GitHub Pages：把仓库变成网页

GitHub Pages 可以把仓库里的静态内容发布成网页。所谓静态内容，就是 HTML、Markdown、图片、CSS 这类不需要服务器实时计算的内容。

适合放在 GitHub Pages 上的内容：

- 课程项目主页。
- 个人学术主页。
- 研究项目介绍。
- 数据说明文档。
- 读书会、工作坊、会议材料导航。

不适合只用 GitHub Pages 的内容：

- 需要登录系统的应用。
- 需要后台数据库的网站。
- 需要运行 Python、R、Node 服务的工具。
- 需要处理用户上传文件的系统。

官方教程见：[GitHub Pages Quickstart](https://docs.github.com/en/pages/quickstart)。

![GitHub Pages quickstart screenshot](assets/screenshots/github-pages-quickstart.png)

看这里：Pages 的关键是“仓库内容可以直接变成网页”。它适合展示，不适合承担复杂后台服务。

## 4. ECS / CVM：租一台一直在线的云端电脑

ECS 通常指 Elastic Compute Service，CVM 是腾讯云的类似产品名。你可以把它理解成：租一台在云厂商机房里一直开机的电脑。

它能做 GitHub Pages 做不了的事情：

- 跑 Python、R、Node、Java 等后台程序。
- 连接数据库。
- 部署问卷系统、数据看板、爬虫任务、API 服务。
- 让程序 24 小时在线。

但 ECS 也更复杂，因为你要关心：

- 操作系统：Linux 还是 Windows。
- 登录方式：密码、密钥、SSH。
- 安全组：哪些端口允许外部访问。
- 域名和备案：中国大陆服务器绑定域名通常要考虑备案。
- 成本：按量付费、包年包月、带宽和流量费用。

### 阿里云 ECS

官方文档：[阿里云 ECS 文档](https://help.aliyun.com/zh/ecs/)。

![Aliyun ECS screenshot](assets/screenshots/aliyun-ecs.png)

看这里：文档入口通常会覆盖购买、登录、网络、安全组和部署。第一次接触云服务器时，先看“快速入门/新手指引”，不要直接跳到复杂配置。

### 腾讯云 CVM

官方产品页：[腾讯云 CVM](https://intl.cloud.tencent.com/products/cvm)。

![Tencent CVM screenshot](assets/screenshots/tencent-cvm.png)

看这里：不同厂商叫法可能不同，腾讯云常见名称是 CVM，本质上也是云服务器。购买入口和控制台入口是最常用的两个按钮。

### 华为云 ECS

官方产品页：[华为云 ECS](https://www.huaweicloud.com/product/ecs.html)。快速入门参考：[华为云 ECS 快速入门](https://support.huaweicloud.com/qs-ecs/ecs_01_0103.html)。

![Huawei ECS screenshot](assets/screenshots/huawei-ecs.png)

看这里：云厂商页面上通常会同时出现“购买”“控制台”“文档”。新手可以按这个顺序理解：先知道买什么，再知道在哪里管理，最后查文档解决具体问题。

## 5. 四者关系：从本地文件到公开服务

```text
本地项目文件
    ↓ 用 Git 记录变化
Git 仓库
    ↓ push 到 GitHub
GitHub 线上仓库
    ├─ 用 GitHub Pages 发布静态网页
    └─ 用 ECS / CVM 运行更复杂的服务
```

一句话区分：

- **Git** 管版本。
- **GitHub** 管线上仓库和协作。
- **GitHub Pages** 管静态网页展示。
- **ECS / CVM** 管一直在线的云端计算机。

## 6. 10 分钟讲解脚本

### 0:00-1:00 为什么要学

从大家熟悉的问题切入：论文版本混乱、项目文件散落、展示只能发网盘、合作时不知道谁改了什么。说明今天讲的不是“程序员专属工具”，而是现代项目管理和公开展示工具。

### 1:00-3:00 Git

用“研究日志”比喻 Git：每次重要修改留下一个节点。强调三个词：可追踪、可回退、可比较。不要先讲命令细节，先讲它解决什么痛点。

### 3:00-5:00 GitHub

展示 GitHub Hello World 截图。解释仓库像项目资料室，README 像封面说明，commit 像修改记录，Pull Request 像请同学帮你检查一组修改。

### 5:00-7:00 GitHub Pages

说明 Pages 的吸引力：不买服务器，也能把项目说明变成网页。举例：课程展示页、读书会资料页、研究项目主页。

### 7:00-9:00 ECS / CVM

解释云服务器就是一直在线的电脑。强调它比 Pages 强，但也更需要维护：登录、安全组、域名、备案、费用。

### 9:00-10:00 怎么选

用一句判断法收尾：

- 只展示文字、图片、链接：优先 GitHub Pages。
- 需要后台程序、数据库、登录、定时任务：考虑 ECS / CVM。
- 任何项目都建议先用 Git 和 GitHub 管起来。

## 7. 完整演示流程：从本地修改到 GitHub 更新

如果要现场演示，建议不要只讲概念，而是从一个真实仓库走一遍：打开终端、下载仓库、改一个文件、提交、推送、回到 GitHub 网页刷新。这样同学们会立刻明白“本地文件”和“线上仓库”之间到底发生了什么。

### 现场演示流程

演示前先打开两个窗口：

- 浏览器：打开这个仓库的 GitHub 页面。
- 终端：进入本地工作路径。

```bash
cd "/Users/jiangheng/Desktop/Work/2026 年 春夏/【M】routines/git, github, pages and ECS-20260507"
```

第一步，把线上仓库下载到本地：

```bash
git clone https://github.com/JiayuREN1127/learn-git-pages-ECS.git
cd learn-git-pages-ECS
```

第二步，确认自己在哪个仓库、哪个分支、有没有未保存的改动：

```bash
pwd
git status
git branch
```

第三步，打开 `guide.md` 或 `README.md`，随便加一句演示用文字。然后回到终端看 Git 发现了什么：

```bash
git status
git diff
```

第四步，把这次修改放进“准备提交区”，再提交成一个版本节点：

```bash
git add guide.md
git commit -m "update demo guide"
```

第五步，把本地提交推送到 GitHub：

```bash
git push origin main
```

最后回到浏览器刷新 GitHub 仓库页面：同学们能看到本地刚刚改的内容已经出现在网页上。这就是 Git + GitHub 最核心的闭环。

### 演示时可以顺手讲的“私货”

- **README 是项目门面，不是形式主义。** 如果一个项目没有 README，别人点进来基本等于进了一个没有门牌号的房间。
- **每次提交只做一件事。** 不要把“改标题、删数据、修 bug、换图片”混在一个 commit 里，否则以后很难追踪。
- **先 `git status`，再 `git add`。** 这是最便宜的防呆动作，可以避免把临时文件、隐私数据、错误版本一起传上去。
- **不要把敏感信息传到 GitHub。** API Key、账号密码、未脱敏访谈资料、原始个人数据都不应该进公开仓库。
- **会 Markdown 的社科同学很占便宜。** 课程主页、研究说明、数据字典、复现流程、读书会资料，都可以先用 Markdown 管起来。
- **Pages 解决展示，ECS 解决运行。** 静态材料优先 Pages；需要数据库、登录、后台程序时再考虑 ECS。不要一上来就买服务器。

## 8. Git 最常见命令语法速查

Git 命令可以先记成一个句型：

```bash
git <动作> <对象> <选项>
```

例如 `git add guide.md` 的意思是：让 Git 把 `guide.md` 这个文件加入下一次提交。

### 第一次配置

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

作用：告诉 Git 提交记录里显示谁做了修改。`--global` 表示对这台电脑上的所有仓库生效。

### 创建或下载仓库

```bash
git init
git clone <仓库地址>
```

- `git init`：把当前文件夹变成 Git 仓库。
- `git clone`：把 GitHub 上的仓库下载到本地。

新手更常用 `git clone`，因为课程项目或团队项目通常已经有线上仓库。

### 查看当前状态

```bash
git status
git log --oneline
git diff
```

- `git status`：看哪些文件改了、哪些文件准备提交。
- `git log --oneline`：用一行一个版本的方式看提交历史。
- `git diff`：看文件具体改了哪里。

我的建议：**每次提交前都先跑 `git status` 和 `git diff`。**

### 提交修改

```bash
git add <文件名>
git add .
git commit -m "一句话说明这次修改"
```

- `git add <文件名>`：只加入指定文件。
- `git add .`：加入当前目录下所有改动。
- `git commit -m`：把准备好的改动保存成一个版本节点。

新手建议优先用 `git add <文件名>`，少用 `git add .`。后者很方便，也很容易把不该提交的东西一起加进去。

### 连接 GitHub

```bash
git remote -v
git remote add origin <仓库地址>
git push origin main
git pull origin main
```

- `git remote -v`：查看本地仓库连接到哪个 GitHub 地址。
- `git remote add origin`：给本地仓库添加线上地址。
- `git push origin main`：把本地 `main` 分支推到 GitHub。
- `git pull origin main`：把 GitHub 上的更新拉回本地。

一句话：`push` 是上传，`pull` 是下载更新。

### 分支操作

```bash
git branch
git switch -c <新分支名>
git switch <分支名>
git merge <分支名>
```

- `git branch`：看有哪些分支。
- `git switch -c`：新建并切换到一个分支。
- `git switch`：切换到已有分支。
- `git merge`：把另一个分支的修改合并进当前分支。

分支可以理解成“草稿路线”。不确定的修改先放分支里，确认没问题再合并到 `main`。

### 撤销和临时保存

```bash
git restore <文件名>
git restore --staged <文件名>
git stash
git stash pop
```

- `git restore <文件名>`：丢弃某个文件还没提交的修改。
- `git restore --staged <文件名>`：把文件从准备提交区拿出来，但保留文件内容。
- `git stash`：临时收起当前修改。
- `git stash pop`：把临时收起的修改拿回来。

注意：`git restore <文件名>` 会丢掉本地未提交内容，运行前一定要看清楚。

### 一个最常用的日常循环

```bash
git pull origin main
git status
# 修改文件
git diff
git add guide.md
git commit -m "update guide"
git push origin main
```

这就是大多数项目每天反复使用的 Git 流程：先同步、再修改、再检查、再提交、再推送。

## 9. 新手操作清单

第一次练习可以做一个最小项目：

1. 在 GitHub 新建一个仓库。
2. 写一个 `README.md`，说明项目是什么。
3. 在本地用 Git 记录修改。
4. 把本地项目 `push` 到 GitHub。
5. 如果是展示型项目，开启 GitHub Pages。
6. 如果需要后台服务，再考虑 ECS / CVM。

最常见的 Git 命令只需要先认识这几个：

```bash
git clone <仓库地址>       # 把线上仓库下载到本地
git status                # 查看哪些文件改了
git add <文件名>          # 准备提交某些修改
git commit -m "说明"      # 保存一次有说明的版本
git push                  # 推送到 GitHub
git pull                  # 拉取别人或线上已有的修改
```

## 10. 常见误区

- Git 不等于 GitHub：Git 是工具，GitHub 是平台。
- GitHub Pages 不等于服务器：它适合展示静态页面，不适合跑后台程序。
- ECS 不是网盘：它是云端电脑，需要管理系统、安全和费用。
- 不要一开始就追求复杂部署：先把 README、项目结构和版本记录做好。
- 国内云服务器如果绑定域名，通常要提前考虑备案和访问环境。

## 11. 结束语

如果只记住一件事：**Git 和 GitHub 让项目更可靠，GitHub Pages 让项目更容易展示，ECS 让项目可以真正在线运行。**

对社科同学来说，学习这些工具的目的不是变成程序员，而是让研究项目更清楚、更可复现、更容易被别人看到。

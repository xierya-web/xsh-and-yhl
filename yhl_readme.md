# xsh-and-yhl

## 基本信息

- 项目：余徽霖（Stewie / yhl）和一位好朋友每周共同思考的问题与想法记录库
- 仓库：https://github.com/xierya-web/xsh-and-yhl
- 远程地址：`git@github.com:xierya-web/xsh-and-yhl.git`（SSH）
- 克隆日期：2026-11-24（北京时间）
- 本地路径：`~/Desktop/github/xsh-and-yhl`
- 默认分支：main
- 仓库状态：2026-11-24 克隆时是空仓库，还没有任何提交

这是你自己新建的库，不属于开源项目收集。SSH 已按 `my-repository` 同一套钥匙配置（`~/.ssh/id_ed25519_xierya_web_my_repository`），之后在本目录里 `git pull` / `git push` 会走这把钥匙。

## 这个项目是干什么的

用来记录并上传你和一位好朋友每周一起想的问题，以及你们各自或共同的想法。适合按周归档，慢慢积累成一份可以回看的对话和思考笔记。

## 对你来说可以怎么用

建议按「年份文件夹 + 周次文件」存放，文件名用 ISO 周次，例如今天（2026-11-24）是 2026 年第 48 周：

```text
~/Desktop/github/xsh-and-yhl/
  2026/
    W48-问题.md
    W49-问题.md
  yhl_readme.md
```

一个周文件里可以写：日期、提出的问题、你的想法、朋友的想法、未决问题。具体小节你可以之后再定，定了就补到文末「后续注意事项」里。

## 如何新增一周笔记并推送到 GitHub

在终端里进入仓库：

```bash
cd ~/Desktop/github/xsh-and-yhl
```

**第一次提交之前**（现在就是这种状态：空仓库、还没有提交），先建文件夹和本周文件，再提交并做第一次推送：

```bash
mkdir -p 2026
# 用你喜欢的编辑器新建并写好 2026/W48-问题.md 之后：
git add 2026/W48-问题.md
git status
git commit -m "添加 2026 年第 48 周的问题与想法"
git push -u origin main
```

`git push -u origin main` 只需在第一次推送时用，用来把本地 `main` 和 GitHub 上的 `main` 连上。

**以后每周**的习惯是：先拉取，再写，再提交推送，减少和朋友同时改同一文件时的冲突：

```bash
cd ~/Desktop/github/xsh-and-yhl
git pull
# 编辑 2026/W48-问题.md，或新建下一周的 2026/W49-问题.md
git add 2026/W48-问题.md
git status
git commit -m "更新 2026 年第 48 周的问题与想法"
git push
```

如果 GitHub 访问较慢，拉取或推送时可临时走本机 ClashX 代理（不改全局 git 配置）。SSH 推送一般不走 HTTP 代理；若以后改用 HTTPS，可以用：

```bash
git -c http.proxy=http://127.0.0.1:7890 -c https.proxy=http://127.0.0.1:7890 pull
```

本文件 `yhl_readme.md` 是本地说明，目前没有提交也没有推送，是否放进仓库由你决定。

## 朋友如何一起写

1. 在 GitHub 打开 https://github.com/xierya-web/xsh-and-yhl ，进入仓库的 Settings → Collaborators，把朋友的 GitHub 账号加为协作成员，并让对方接受邀请。具体按钮名称以 GitHub 页面为准。
2. 朋友在自己的电脑上同样用 `git clone` 把仓库拉下来（对方需要有访问权限，私有仓库还需配置好自己的 GitHub 登录或 SSH 钥匙）。
3. **每次开始写之前先 `git pull`**，写完再 `git add`、`git commit`、`git push`。不要两个人同时改同一个周文件的同一段而不先拉取，否则可能出现合并冲突。
4. 如果还是冲突了，把终端里的提示发给我，我可以帮你看怎么处理。也可以约定：每人写在文件里署好名的小节，或者一周由一个人先写、另一个人再补充。

## 如何更新（同步远程已有内容）

```bash
cd ~/Desktop/github/xsh-and-yhl
git status
git pull
```

空仓库在完成第一次 `git push` 之前，远程还没有可拉取的提交，这时不必先 pull。

## 后续注意事项

# Academic 个人主页 · 操作指南

> 全程在浏览器里完成，不用装软件。第一次大约 30 分钟。
> 做完后网址是：`https://你的用户名.github.io`

---

## 这个模板是怎么组织的

```
website/                     ← 上传这个文件夹「里面」的所有东西
├── _config.yml              ← ✏️ 名字、头衔、学校、邮箱、各种链接、菜单（只改一次，所有页面同步）
├── index.md                 ← ✏️ 首页 About：自我介绍、研究兴趣、News
├── publications.md          ← ✏️ 论文页
├── teaching.md              ← ✏️ 教学页
├── files/                   ← ✏️ 你的文件放这里：照片 photo.jpg、简历 cv.pdf、论文 PDF
│   └── cv.pdf               （占位文件，换成你的）
├── 404.html                 ← 找不到页面时显示的页面，不用管
├── _layouts/  _includes/    ← 网站外框和图标，不用管
└── assets/                  ← 样式和默认头像（只有想换颜色才需要打开 assets/css/site.css）
```

**你日常只需要动 4 个文件 + 1 个文件夹**：`_config.yml`、`index.md`、`publications.md`、`teaching.md`、`files/`。

GitHub 会自动把 `.md` 文件变成网页（这个功能叫 Jekyll，GitHub Pages 自带，不用设置）。

---

## Step 1 · 注册 GitHub

https://github.com → **Sign up**。用户名会出现在网址里，建议用正式的英文名或拼音。

## Step 2 · 创建仓库

1. 右上角 **+** → **New repository**
2. Repository name 填：`你的用户名.github.io`（必须一字不差）
3. 选 **Public** → **Create repository**

> 💡 如果你之前已经按第一版模板建过这个仓库并上传了文件：先把旧的 `index.html`、`style.css`、`avatar.svg` 删掉（点开文件 → 右上角 `…` → **Delete file** → Commit），再继续下一步。不删的话，旧的 `index.html` 会和新的首页冲突。

## Step 3 · 上传文件（这一步最容易出错）

1. 仓库页面点蓝色小字 **uploading an existing file**（或 **Add file → Upload files**）
2. 在电脑上**打开** `website` 文件夹，`Ctrl + A`（Mac: `Cmd + A`）**全选里面的所有东西**（包括 `_layouts`、`_includes`、`assets`、`files` 这几个文件夹）
3. **拖进**网页上传区域
   - ⚠️ 必须用**拖**的。点 "choose your files" 弹出的选择框不能选文件夹
   - ⚠️ 拖的是文件夹**里面**的东西，不是 `website` 文件夹本身
   - 建议用 Chrome 或 Edge
4. 等进度条走完，确认列表里能看到 `_config.yml`、`_layouts/default.html` 这类带文件夹路径的文件
5. 页面底部点绿色 **Commit changes**

上传完，仓库首页应该**直接**看到 `_config.yml`、`index.md`、`_layouts` 等。如果只看到一个 `website` 文件夹，说明拖错了，删掉重来。

## Step 4 · 确认上线

1. 仓库 → **Actions** 标签：会看到一个叫 *pages build and deployment* 的任务，等它变成绿色 ✓（1–3 分钟）
2. 打开 `https://你的用户名.github.io` 🎉
3. 如果 Actions 里什么都没有：**Settings → Pages**，Source 选 **Deploy from a branch**，Branch 选 **main** / **(root)** → Save

---

## Step 5 · 换成你的内容

**修改任何文件的方法都一样**：在仓库里点开文件 → 右上角 ✏️ → 改 → 右上角绿色 **Commit changes…** → 再点一次 **Commit changes** → 等 1–2 分钟 → 刷新网站（强制刷新：Windows `Ctrl + F5`，Mac `Cmd + Shift + R`）。

### 建议的修改顺序

**① `_config.yml`：基本信息**

```yaml
name: "Your Name"                          ← 你的名字
tagline: "PhD Candidate in Your Field"     ← 名字下面那行红字
department: "Department of Your Field"
institution: "University Name"
```

链接部分：有就填，没有就改成空引号 `""`，左侧栏那一项会自动消失。

⚠️ `_config.yml` 对格式很敏感：**只改引号里的内容**，不要动冒号、短横线和每行开头的空格。改坏了网站不会更新，Actions 里会出现红色 ✗。点进去能看到出错的是哪一行。

**② 照片和简历**

1. 照片改名为 `photo.jpg`，简历改名为 `cv.pdf`
2. 仓库里点进 `files` 文件夹 → **Add file → Upload files** → 拖进去 → Commit
3. 同名文件会直接覆盖旧的，代码不用改

照片建议：竖版（4:5 左右），压缩到 500KB 以内。⚠️ 文件名区分大小写，`photo.JPG` 和 `Photo.jpg` 都不行。iPhone 的 HEIC 格式照片要先转成 JPG。

**③ `index.md`：自我介绍 + News**

**④ `publications.md`：论文**

**⑤ `teaching.md`：教学**

每个文件开头都有中文注释说明格式。注意每个文件最上面 `---` 包起来的几行**不要删**。

### Markdown 速查（够用了）

| 写法 | 效果 |
|---|---|
| `**文字**` | **粗体** |
| `*文字*` | *斜体*（期刊名用这个） |
| `[文字](https://链接)` | 链接 |
| 空一行 | 新的一段 |
| `- 开头` | 列表 |
| `1. 开头` | 编号列表（论文用这个） |
| `## 开头` | 小标题 |

### 论文怎么写

```markdown
1. **Your Name**, Coauthor A, and Coauthor B (2025). Title of paper. *Journal Name*. [PDF](链接) [Code](链接)
```

- 链接 `[PDF]`、`[arXiv]`、`[Code]`、`[Slides]` 会显示成小按钮，按钮名可以随便起
- 论文 PDF 也可以上传到 `files` 文件夹，链接写成 `/files/文件名.pdf`
- 每组论文最后的 `{: .pubs}` 不要删，删了就变成普通列表（不会出错，只是不好看）
- 同理，News 最后的 `{: .news}` 也不要删

### 加一个新页面（比如 Personal、Research）

1. 仓库首页 → **Add file → Create new file**，文件名填 `personal.md`
2. 内容开头写这几行，下面接着写正文：
   ```
   ---
   layout: default
   title: Personal
   permalink: /personal/
   ---
   ```
3. 在 `_config.yml` 的 `nav:` 下面加两行（注意对齐前面的空格）：
   ```yaml
     - title: "Personal"
       url: "/personal/"
   ```

不需要某个页面（比如 Teaching）：删掉 `teaching.md` 文件，并删掉 `_config.yml` 里 Teaching 那两行。

### 换主题色

打开 `assets/css/site.css`，改最上面 `--brand: #9b2335;` 这一行。文件里列了几个备选色：酒红、藏青、墨绿、钢蓝、深紫、炭黑。

---

## ⚠️ 常见问题

1. **网站没更新** → 先看 Actions：黄色圈表示还在构建，等一下；绿色 ✓ 表示已经好了，强制刷新就行；红色 ✗ 表示出错，点进去看是哪个文件哪一行，最常见的原因是 `_config.yml` 的引号或空格被改坏了
2. **404** → 检查 `index.md` 和 `_config.yml` 是不是在仓库最外层，而不是在 `website/` 文件夹里
3. **照片不显示** → 检查是不是 `files/photo.jpg`（全小写，jpg 不是 jpeg）
4. **改坏了** → 点开文件 → 右上角 **History** 能看到每个旧版本。也可以直接把压缩包里的原文件重新上传，覆盖掉
5. **隐私** → Public 仓库所有人可见，历史版本也查得到。不要放手机号、住址
6. **邮箱防爬虫** → 很多学者会写成 `name [at] university [dot] edu`。要这样做的话，把 `_config.yml` 里的 email 留空，再在 `index.md` 里手写一行这种格式

---

## 进阶（以后再说）

- **自定义域名**：买域名后在 Settings → Pages → Custom domain 设置
- **Blog**：Jekyll 自带博客功能（建一个 `_posts` 文件夹），需要时再加
- 在中国大陆访问 `github.io` 有时会慢或不稳定；Google Fonts 在大陆可能加载不了，这时会自动换成系统字体，内容不受影响

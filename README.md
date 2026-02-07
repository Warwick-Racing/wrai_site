# Warwick AI Racing 网站 - GitHub Pages 部署包

本目录是**纯静态网站**，可直接用于 GitHub Pages，无需再构建。

## 上传到 GitHub Pages

### 方式一：用本目录作为仓库根（推荐）

1. 新建一个 GitHub 仓库（名字随意，例如 `wrai-site`）。
2. 把本目录里的**所有内容**（`index.html`、`404.html`、`assets/` 文件夹）上传到仓库**根目录**。
3. 仓库 Settings → Pages → Source 选 **Deploy from a branch**。
4. Branch 选 `main`，Folder 选 **/ (root)**，保存。
5. 几分钟后访问：`https://你的用户名.github.io/仓库名/`。

### 方式二：用本目录作为 docs 文件夹

1. 把本目录里的**所有内容**复制到仓库的 `docs/` 文件夹（即仓库根下要有 `docs/index.html`、`docs/assets/` 等）。
2. Settings → Pages → Source 选 **Deploy from a branch**，Folder 选 **/docs**。
3. 访问：`https://你的用户名.github.io/仓库名/`。

## 目录说明

- `index.html`：首页，资源使用相对路径，可在任意子路径下打开。
- `404.html`：与首页相同，用于 GitHub Pages 子路径刷新时仍能打开单页应用。
- `assets/`：JS、CSS、图片等静态资源。

无需安装 Node、无需执行 `npm run build`，直接上传即可当网页使用。

**提示**：若站点地址是 `用户名.github.io/仓库名/`（项目页），首页可以打开，但点击内链（如 Team、Cars）后刷新可能 404；若希望完全正常，可新建仓库名为 `你的用户名.github.io`，把本目录内容放到该仓库根目录，则站点在 `https://你的用户名.github.io/`，所有路由均可正常使用。

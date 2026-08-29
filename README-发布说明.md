# GitHub Pages 发布说明

本目录是已经生成好的静态网站，不需要安装依赖或运行构建命令。

## 发布

1. 新建或打开一个 GitHub 仓库。
2. 把本目录内的全部文件和 `assets` 文件夹上传到仓库根目录，不要只上传 `index.html`。
3. 打开仓库的 **Settings → Pages**。
4. 在 **Build and deployment** 中选择 **Deploy from a branch**，分支选择 `main`，目录选择 `/(root)`。
5. 保存并等待 GitHub Pages 给出默认网址。

## 映射域名

仓库根目录已经包含 `CNAME` 文件，内容是：

```text
longcan.shenzhe.org
```

在 Cloudflare 中，把 `longcan` 的 CNAME 改为你的 GitHub Pages 默认域名，例如：

```text
你的GitHub用户名.github.io
```

不要在目标中加入仓库名。Cloudflare 代理状态先选择 **DNS only**。随后在 GitHub Pages 的 **Custom domain** 中填写 `longcan.shenzhe.org`，验证通过后启用 **Enforce HTTPS**。

注意：域名当前如果仍指向 `custom-domains.chatgpt.site`，必须先替换成 GitHub Pages 的 CNAME；同一个名称不能保留两条相互冲突的 CNAME。

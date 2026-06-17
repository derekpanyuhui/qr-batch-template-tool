# 批量二维码模板合成工具

这是一个可直接本地打开、也可直接部署到 GitHub Pages 的纯前端网页工具。

## 功能

- 批量识别 URL：支持换行、逗号、空格、整段文案、CSV
- 上传单张或多张模板图
- 自动生成二维码并合成到模板
- 支持拖拽调整位置
- 支持自动识别二维码候选区域
- 支持单张 PNG、批量 PNG、ZIP 下载
- 完全离线可运行

## 本地使用

直接双击 [index.html](./index.html) 即可。

如果浏览器对本地文件有额外限制，也可以在当前目录临时起一个静态服务：

```bash
python3 -m http.server 8080
```

然后打开：

```txt
http://127.0.0.1:8080/
```

## GitHub Pages 部署

这个仓库已经包含 GitHub Pages 工作流：

- [deploy-qr-batch-template-tool.yml](../.github/workflows/deploy-qr-batch-template-tool.yml)

它会把 `qr-batch-template-tool/` 目录单独发布成 Pages 站点。

### 步骤

1. 把整个仓库推到 GitHub。
2. 进入仓库的 `Settings -> Pages`。
3. 在 `Build and deployment` 里把 `Source` 设为 `GitHub Actions`。
4. 确保代码在 `main` 分支。
5. 之后每次更新 `qr-batch-template-tool/` 目录并推送，GitHub 会自动重新发布。

### 访问地址

通常会是：

```txt
https://你的用户名.github.io/你的仓库名/
```

注意这里不会带 `qr-batch-template-tool/` 子路径，因为工作流发布的就是这个目录本身。

## 目录

- [index.html](./index.html)：主页面
- [vendor/qrcode.min.js](./vendor/qrcode.min.js)：本地二维码库
- [vendor/jszip.min.js](./vendor/jszip.min.js)：本地 ZIP 打包库

# 批量二维码模板合成工具

这是一个纯前端、完全离线可运行的 GitHub Pages 工具站。

## 功能

- 批量识别 URL：支持换行、逗号、空格、整段文案、CSV
- 上传单张或多张模板图
- 自动生成二维码并合成到模板
- 支持拖拽调整位置
- 支持自动识别二维码候选区域
- 支持单张 PNG、批量 PNG、ZIP 下载
- 完全离线可运行

## 在线使用

部署完成后，直接打开仓库对应的 GitHub Pages 地址即可。

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

## 仓库结构

- [index.html](./index.html)：主页面
- [vendor/qrcode.min.js](./vendor/qrcode.min.js)：本地二维码库
- [vendor/jszip.min.js](./vendor/jszip.min.js)：本地 ZIP 打包库

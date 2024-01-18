# LXGW WenKai GB / 霞鹜文楷 GB 网络字体仓库

> 其他版本霞鹜文楷字体的网络字体仓库：
>   - [霞鹜文楷 / LXGW WenKai](https://github.com/CMBill/lxgw-wenkai-web)：原版。
>   - [霞鹜文楷屏幕阅读版 / LXGW WenKai Screen](https://github.com/CMBill/lxgw-wenkai-screen-web)：适用于 PC 和 Android 手机屏幕显示且无需特别切换到粗体。
>   - [霞鹜文楷 TC / LXGW WenKai TC](https://github.com/CMBill/lxgw-wenkai-tc-web)：繁体中文版。

## 简介
[LXGW WenKai GB / 霞鹜文楷 GB](https://github.com/lxgw/LxgwWenkaiGB) 是 [霞鹜文楷](https://github.com/lxgw/LxgwWenKai) 进一步调整字形和笔形后，符合 G 源字形规范的字体，目前包含《通用规范汉字表》8105 个汉字。字体详情请参阅原字体仓库。

为使原字体更适合进行网络分发，本仓库使用 Github Action，利用[中文网字计划](https://chinese-font.netlify.app/)开发的[字体分包工具](https://github.com/KonghaYao/cn-font-split)对原字体分包，网页加载时只需获取所使用的文字所在的分包，大幅降低所需加载的大小，提升网页加载速度。

为方便使用，本仓库的版本号将与字体原仓库版本号一致。目前只提供了 `v1.011` 及之后的版本。

## 使用
直接将文后提供的链接以 `<link>` 的形式添加到网页的 `<head>` 内即可

```html
<html>
<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/lxgw-wenkai-gb-web/style.css" />
  <style>
    body {
      font-family: "LXGW WenKai GB";
      font-weight: normal;
    }
  </style>
</head>
<body>
  
</body>
</html>
```

这样引入 `style.css` 的可以调用仓库包含的所有字体，使用字体时以表格中所示 `font-family` 与 `font-weight` 在 CSS 中调用即可。

| 字体                      | `font-family`               | `font-weight` |
| ------------------------- | --------------------------- | ------------- |
| LXGW Wenkai GB            | `LXGW Wenkai GB`            | `normal`      |
| LXGW Wenkai GB Bold       | `LXGW Wenkai GB`            | `bold`        |
| LXGW Wenkai GB Light      | `LXGW Wenkai GB Light`      | `normal`      |
| LXGW WenKai Mono GB       | `LXGW WenKai Mono GB`       | `normal`      |
| LXGW WenKai Mono GB Bold  | `LXGW WenKai Mono GB`       | `bold`        |
| LXGW WenKai Mono GB Light | `LXGW WenKai Mono GB Light` | `normal`      |

如果只需某一特定的字体，也可只引用其对应分包的 CSS 文件，将如下表格中 `repositoryURL` 替换为仓库的链接即可。

| 字体                      | 链接                                                              |
| ------------------------- | ----------------------------------------------------------------- |
| LXGW Wenkai GB            | `https://repositoryURL/lxgwwenkaigb-regular/result.css`     |
| LXGW Wenkai GB Bold       | `https://repositoryURL/lxgwwenkaigb-bold/result.css`        |
| LXGW Wenkai GB Light      | `https://repositoryURL/lxgwwenkaigb-light/result.css`       |
| LXGW WenKai Mono GB       | `https://repositoryURL/lxgwwenkaimonogb-regular/result.css` |
| LXGW WenKai Mono GB Bold  | `https://repositoryURL/lxgwwenkaimonogb-bold/result.css`    |
| LXGW WenKai Mono GB Light | `https://repositoryURL/lxgwwenkaimonogb-light/result.css`   | 

例如若只需调用 LXGW Wenkai Mono GB，则只需引入：
```
https://cdn.jsdelivr.net/npm/lxgw-wenkai-gb-web/fonts/lxgwwenkaimonogb-regular/result.css
``` 

## 链接
### 自行部署
如果下方提供的链接连接效果不甚理想，建议自行部署并配合自己的 CDN 使用。可以直接 Fork 本仓库并启用 Github Pages，使用时将下方链接修改为自己的仓库地址即可，亦可直接克隆本仓库到服务端、对象存储等。

### 使用 CDN
#### 作为 npm 包
目前已作为 npm 包上传到 npmjs，可以使用 npm 包的镜像引用，如JsDelivr 的 npm 镜像：

```
https://cdn.jsdelivr.net/npm/lxgw-wenkai-gb-web/style.css
```

也可指定版本号，将链接中的 `$VERSION` 替换为目标版本号（但 npm 的语义化版本号会省略版本号数字开头的 0）如 `1.11` 或 `v1.11` 均可。目前仅只提供 `v1.011` 之后的版本。

```
https://cdn.jsdelivr.net/npm/lxgw-wenkai-gb-web@VERSION/style.css
```

#### 使用 JsDelivr 对 GitHub 仓库的 CDN
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-gb-web@latest/style.css
```

注意，分包后产生的字体和 CSS 文件位于 `latest` 分支，因此**必须加上** `@latest`，否则无法访问到对应文件。也可指定版本号，将链接中的 `$VERSION` 替换为目标版本号，如 `1.011` 或 `v1.011` 均可。目前仅只提供 `v1.011` 之后的版本。
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-gb-web@VERSION/style.css
```

### 直接使用本仓库链接
只提供最新版本

```
https://cmbill.github.io/lxgw-wenkai-gb-web/style.css
```

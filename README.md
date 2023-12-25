# LXGW WenKai GB / 霞鹜文楷 GB 网络字体仓库

## 仓库仍在完善，但可以初步使用
## 简介
[LXGW WenKai GB / 霞鹜文楷 GB](https://github.com/lxgw/LxgwWenkaiGB) 是 [霞鹜文楷](https://github.com/lxgw/LxgwWenKai) 进一步调整字形和笔形后，符合 G 源字形规范的字体，目前包含《通用规范汉字表》8105 个汉字。字体详情请参阅原字体仓库。

为使原字体更适合进行网络分发，本仓库使用 Github Action，利用[中文网字计划](https://chinese-font.netlify.app/)开发的[字体分包工具](https://github.com/KonghaYao/cn-font-split)对原字体分包，网页加载时只需获取所使用的文字所在的分包，大幅降低所需加载的大小，提升网页加载速度。

为方便使用，本仓库的版本号将与字体原仓库版本号一致。目前只提供了 `v1.011` 及之后的版本。

## 使用
### 自行部署
如果下方提供的链接连接效果不甚理想，建议自行部署并配合自己的 CDN 使用。可以直接 Fork 本仓库并启用 Github Pages，使用时将下方链接修改为自己的仓库地址即可，亦可直接克隆本仓库到服务端、对象存储等。

### 使用 JsDelivr 的 CDN
#### 最新版本
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-screen-web/style.css
```

#### 特定版本 
将链接中的 `$VERSION` 替换为目标版本号，如 `1.011` 或 `v1.011` 均可。目前仅只提供 `v1.011` 之后的版本。
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-screen-web@VERSION/style.css
```
例如请求 `v1.011` 版本的字体：
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-screen-web@1.011/style.css
```

### 直接使用本仓库链接
只提供最新版本

```
https://cmbill.github.io/lxgw-wenkai-screen-web/style.css
```
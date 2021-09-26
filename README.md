# cloudimages

[TOC]

------

# PciGo + Typora实现上传图片到Gitee

## **1. 下载PciGo+Typora**

PciGo开源地址: https://github.com/Molunerfinn/PicGo

PciGo下载地址: https://github.com/Molunerfinn/PicGo/releases

Typora: https://www.typora.io/

程序员应该都了解 **Typora** 是专注于编写 Markdown 格式的编辑软件，使用方便，支持多种格式导出。

**PicGo** 是一款免费的图床管理应用，支持拖拽上传，剪切板上传等方式。你可以用它快捷地将图片上传到图床并获得网络链接。

注意：请不要把 PicGo 安装到 C 盘 Program Files 下。

## **2. 配置 PicGo (CDN 加速)**

- [**github图床配置**](https://mp.weixin.qq.com/s?__biz=MzI3NjQyMzI2Ng==&mid=2247488356&idx=1&sn=6bb64cf8a7055fa1aabcf0876f5baa19&chksm=eb74e469dc036d7fb13d49a7d6dd9e929e3d344ac2ff6b27827af960505b69149d6ba5c1961a&mpshare=1&scene=24&srcid=0131cUJo6gsfR6shXmwrgN5g&sharer_sharetime=1612076631883&sharer_shareid=baffa657065a4a928bb14a038bc2b5d2#rd)
- [**gitee图床配置**](https://www.cnblogs.com/geq2020/p/12506466.html)

这里使用 github/gitee 搭建的免费图床

常见问题:

1. **设置中没有gitee图床**

- 这里注意一下，必须要先安装[**node.js**](https://nodejs.org/en/)才能安装插件，没装的自己装一下，然后重启就行。

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218191007897.png)

### 2.1. 建立gitee（码云）图床仓库

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218191126814.png)

### 2.2. 配置PicGo需要码云的token(私人令牌)，点击设置

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218191154291.png)

### 2.3. 点击左下角的私人令牌，然后点击新建

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218191213053.png)

### 2.4. 按照下图配置，点击提交

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218191236106.png)

### 2.5. 账号验证，按照提示输入密码; 私人令牌生成成功，点击复制

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218190842462.png)

### 2.6. 配置PicGo，点击图床设置——Gitee图床，进行配置

- owner：所有者，写上你的码云账号名

- repo：仓库名称，刚刚新建的图床仓库名称, 一般写(gitee的地址省略): xqg1316/cloudimages
- path：图片存储根路径，自己新建即可, 一般写: img
- token：填入刚刚复制的码云的私人令牌
- message：不用填
- customPath：提交消息，这一项和下一项customURL都不用填。在提交到码云后，会显示提交消息，插件默认提交的是 Upload 图片名 by picGo - 时间

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218190410992.png)

- 点击 “确定”。
- 如果想用 Typora 等博客编写程序直接上传到 Gitee 图床，就需要设为 “默认图床” 。

## **3. 设置 Typora**

### 3.1. 打开Typora后，点击菜单栏 -> 文件 -> 偏好设置

1）插入图片时...下边的选择框内选择上传图片

2）勾选上“对本地位置的图片应用上述规则”

3）上传服务选择PicGo(app)

4）将PicGo路径项设置为本地PicGo的安装路径

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218190410991.png)

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218190438267.png)

### 3.2. 点击PicGo界面左侧的PicGo设置->设置Server，并按下图设置（默认已设置）

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218190515658.png)

![img](https://gitee.com/xqg1316/cloudimages/raw/master/image/image-20210218190531955.png)
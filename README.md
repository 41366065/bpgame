<div align="center"><b>[ bpgame  在web bilibili上运行的游戏扩展 ]</b></div>  

# 项目介绍

#### 目前版本：v0.2.0

**注意: 扩展仍在开发中（目前为半残疾），在stable版本出来前还请谨慎使用**

  
**bpgame是一个能够在b站上快速实现有趣想法的扩展**<font size="1">~~因b站互动视频功能垃圾~~</font>  
**观看官方示例预览插件的功能吧** -----> [介绍视频](https://www.bilibili.com/video/BV1P24y1U7Lg)

### 目前封装的功能有
- **视频控制（跳转，暂停...）**
- **文件IO（可在本地存储）**
- **一些基本功能，如按键控制**  
- **基于Pixijs的开发工具箱**
---

# &#x2728;如何安装和使用
### 目前因扩展未完善，请在开发者模式下使用
### 如果因扩展影响了web版b站的正常使用，请随时关闭此扩展  
#### 1. 安装
- 先确保电脑安装了较新版本的正版Chrome浏览器（非360Chrome等）
- 下载该扩展压缩包并解压
- 点击install.exe，此时会在注册表中添加本地websocket服务器bpws.exe的路径，再点击一次则为删除
- 在Chrome扩展（浏览器右上角中）勾选开发者模式
- 选择<加载已解压的扩展程序>，选择下载的扩展文件夹, 安装完毕！

#### 2. 安装游戏
- 游戏均要放在扩展文件夹**Assets/games**文件夹下（新安装的扩展内置官方示例的游戏，可用于测试安装成功）
- 下载他人分发的游戏文件夹解压到 **Assets/games** 文件夹，在 **Assets/games/gamelist.json** 中添加 **bv号和文件夹的对应关系**
- 找到他人分发的游戏视频，按下enter即可进入bpgame游戏模式
- 一般游戏会配置退出功能，如要中途强制退出则按**两下esc**，界面将退出全屏并清除游戏资源

更详细的图文教程可参照 -----> [图文教程](https://www.bilibili.com/read/cv17949898) 

#### 3. 开始游戏
- 除**enter进入游戏**和**两下esc**为扩展内置按键外，其他游戏操作均以up主分发时为准

# &#x270f; 使用bpgame插件开发自己的《video game》
参照官方文档 -----> （暂缺）  
---
# &#x2665; 参与项目开发
***有任何问题和想法都可在issue中提出！***  
### &#x1F4DA; 主要代码文件
- **[background后台](src/background.js) ---> 主要监听页面改动和一些全局处理**
- **[页面脚本](src/bplistener.js) ---> 动态注入iframe, 页面DOM改动等**
- **[API](src/api/bpcore.js) ---> 内置的生命周期管理脚本，为开发提供便利**  
- **[toolbox](src/api/toolbox/) ---> 组件库**


### &#x1F680; Roadmap
- **完善api和组件库**
- **开发文档编写**
- **popup扩展程序界面，简化安装游戏步骤等**
- **更换扩展icon**
- **提供本地类b站视频开发环境**
- **升级版本为0.3**
- **等等...**

**技术交流群：829678270**
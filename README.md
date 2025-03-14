# Check Steam-Link

一个AstrBot插件。
A plugin for AstrBot.

# 功能介绍
## 已实现
- 自动检测对话中出现的steam商店页链接，并返回对应页面的网页截图和摘要信息。
- 更详细的信息解析。
- 检测steam个人主页链接，并返回个人主页截图。
  目前支持的格式如下：
```
https://store.steampowered.com/app/881020/Granblue_Fantasy_Relink/ # 游戏商店页链接
https://steamcommunity.com/id/inori_333/ # 个人主页链接
```
可解析的信息：
```
游戏名称
发行时间
开发商
发行商
游戏类别（保留前五个）
游戏简介
游戏评分
游戏价格
是否支持中文（包括简体中文和繁体中文）
```
## 待实现
- 返回更更详细的商店页文字信息。
- 返回与链接游戏相关的其他信息，比如从SteamDB获取的价格变化等等。
- 支持参数设置，比如是否需要返回截图，截屏的宽度和高度，返回摘要的详细等级等等。

# 使用方法
## 软件依赖
程序依赖无头参数下的Chrome浏览器进行本地截屏，**您的主机需要安装Chrome浏览器以及对应的ChromeDriver驱动**，没有的话去官网装一个。
## 第三方库依赖
程序依赖以下第三方库：
- selenium
- webdriver-manager
- requests
- beautifulsoup4

但是，您应该无需手动安装任何第三方库，本插件会自动检测您的环境，并安装缺失的库。
## 配置依赖
1.复制您的ChromeDriver所在位置，如果不记得放在哪了可以使用Everything等常见搜索工具，或者直接重新下载一个。
2.打开本插件目录，也就是在您的astrbot安装目录下打开./AstrBot/data/plugins/astrbot_plugin_steamshot
3.使用IDE或记事本打开main.py
4.在`def capture_screenshot(url, save_path):`上方添加一行内容：
```
CHROMEDRIVER_PATH = "C://Users//Administrator//.wdm//drivers//chromedriver//win64//134.0.6998.35//chromedriver-win32//chromedriver.exe"
```
**其中的路径信息需要替换为您的Chromedriver.exe所在的路径**。
## 前端使用
无需使用任何指令，插件会自动检测对话中出现的steam链接，并返回对应页面的网页截图和摘要信息。
(当然目前也不支持任何指令就是了)

# 使用示例
![使用示例](sample.png)
![使用示例2](sample2.png)

# 支持
[帮助文档](https://github.com/inori-3333/astrbot_plugin_steamshot)

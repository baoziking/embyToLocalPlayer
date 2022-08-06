# embyToLocalPlayer

需要python。若用mpv播放，可更新服务器观看进度。

**缺点**

* 本地需要安装python
* 目前主要windows平台，其他尚未测试。
* 会提示没有兼容的流，可另装脚本自动关闭提示。

**优点**

* 在首页也可以播放。点击原来的播放按钮就可以。不改变页面布局。
* 可回传播放进度到服务器。若需要此功能，配置文件里填mpv的播放器。
* 文件本地或挂载或远端均可。（脚本菜单里选择）
* mpv potplayer mpc 支持服务端的外挂字幕。(播放前先选择字幕)
* 不影响其他功能使用。
* 适配多视频版本，如2160p与1080p双文件的情况。

**建议**

* 最佳体验请用 mpv ,嫌配置麻烦可以用 mpv.net
* potplayer播放http会疯狂写盘并把整个文件下载下来。非挂载不建议使用。

## 使用说明

> 基础配置

1. 下载 `embyToLocalPlayer.zip` 并解压到任意文件夹 [链接](https://github.com/kjtsune/embyToLocalPlayer/releases)
2. 安装 tampermonkey [官网](https://www.tampermonkey.net/)
3. 安装并修改或添加匹配网址 `embyToLocalPlayer.js` [发布页](https://greasyfork.org/zh-CN/scripts/448648-embytolocalplayer?locale_override=1)
4. 安装 python (勾选add to path) [官网](https://www.python.org/downloads/)
5. 配置 `embyToLocalPlayer.ini` 

> [二选一] 简易模式 [推荐]

6. 下载解压并安装 AutoHotKey v2 [官网](https://www.autohotkey.com/) [链接](https://www.autohotkey.com/download/ahk-v2.zip)
7. 双击运行 `embyToLocalPlayer_debug.ahk` 
8. 现在可网页播放测试，若正常，创建 `embyToLocalPlayer.ahk` 快捷方式，并放入开机启动文件夹即可。( `win + r` 输入 `shell:startup` 回车)

> [二选一] 一般模式

6. 打开命令行。修改并输入 `python C:/<path_to>/embyToLocalPlayer.py` 
7. 现在可网页播放测试，若正常，修改 `embyToLocalPlayer.vbs` 里的python路径和.py文件路径。
8. .vbs放入开始文件夹即可 ( `win + r` 输入 `shell:startup` 回车)
9. 删除文件夹里所有 `.ahk` 的文件。

> 可选操作

* 安装 `embyErrorWindows.js` 可自动关闭提示没有兼容流的窗口。[发布页](https://greasyfork.org/zh-CN/scripts/448629-embyerrorwindows?locale_override=1)
* `active_video_player.ahk` 是用来激活播放器。不然mpv播放后需要鼠标点击激活窗口才可以使用mpv键盘快捷键。需要[二选一]的简易模式。
* 问题反馈群，提问前先尽量自行排查一下。[https://t.me/embyToLocalPlayer](https://t.me/embyToLocalPlayer)
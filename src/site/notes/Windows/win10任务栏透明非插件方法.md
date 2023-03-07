---
{"dg-publish":true,"permalink":"/Windows/win10任务栏透明非插件方法/"}
---

### 注册表操作
打开注册表以下路径
==计算机\\HKEY_CURRENT_USER\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Explorer\\Advanced==
右侧新建 DWORD(32位)值 
重新命名为 TaskbarAcrylicOpacity
修改其 16进制数值为 0
### 个性化操作
以上注册表操作完成后
桌面右键打开**个性化**
找到颜色，选择颜色时选自定义
windows模式暗，应用模式亮
打开*透明效果*
### 重启资源管理器
任务栏右键，打开任务管理器
按住 w ，等他遍历到 Windows 资源管理器
右键重启资源管理器
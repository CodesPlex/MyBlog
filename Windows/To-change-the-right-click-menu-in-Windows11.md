# Windows11右键菜单更改

> 作者：hipython2023
>
> 尊重项目原创性！

## 把Windows11右键菜单风格切换为Windows10右键菜单风格

以管理员权限，打开命令提示符cmd控制台，输入以下的命令：

切换到Win10版右键菜单：

```sh
reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
taskkill /f /im explorer.exe & start explorer.exe
```

恢复到Win11版右键菜单：

```sh
reg delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f 
taskkill /f /im explorer.exe & start explorer.exe
```
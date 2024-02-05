# 卸载小组件

> 作者：hipython2023
>
> 尊重项目原创性！

## 卸载全是广告的Windows11小组件

以管理员权限，打开命令提示符cmd控制台，输入以下的命令：

```sh
winget uninstall MicrosoftWindows.Client.WebExperience_cw5n1h2txyewy
taskkill /f /im explorer.exe & start explorer.exe
```

## 重新安装Windows11小组件

以管理员权限，打开命令提示符cmd控制台，输入以下的命令：

```sh
winget install 9MSSGKG348SP
```
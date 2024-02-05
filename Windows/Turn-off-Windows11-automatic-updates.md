# 关闭Windows自动更新

> 作者：hipython2023
>
> 尊重项目原创性！

## 永久暂停Windows的自动更新

以管理员权限，打开命令提示符cmd控制台，输入以下的命令：

```sh
reg add "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsUpdate\UX\Settings" /v FlightSettingsMaxPauseDays /t reg_dword /d 9999 /f
```
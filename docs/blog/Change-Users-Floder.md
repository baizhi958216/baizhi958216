# 重装!把用户目录放在其它地方

## 重启进入OOBE
在选择地区的时候按下键盘`CTRL+SHIFT+F3`重启

## 创建应答文件

relocate.xml

```xml
<?xml version="1.0" encoding="utf-8"?>
<unattend xmlns="urn:schemas-microsoft-com:unattend">
    <settings pass="oobeSystem">
        <component name="Microsoft-Windows-Shell-Setup" processorArchitecture="amd64" publicKeyToken="31bf3856ad364e35" language="neutral" versionScope="nonSxS"
            xmlns:wcm="http://schemas.microsoft.com/WMIConfig/2002/State"
            xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
            <FolderLocations>
                <ProfilesDirectory>D:\Users</ProfilesDirectory>
            </FolderLocations>
        </component>
    </settings>
</unattend>
```

## 重启继续安装
- 进入`C:\windows\system32\sysprep`

- 地址栏运行`cmd`

终端输入并执行  
```bash
sysprep.exe /oobe /reboot /unattend:d:\relocate.xml
```

## 跳过联网
网络连接界面按下`SHIFT+F10`

运行
```bash
OOBE\BYPASSNRO
```
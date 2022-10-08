# 转储刷机包里的 payload.bin

## 情景

`a/b` `dynamic a/b` 刷机包里的分区(`system.img`, `boot.img` 等)塞 `payload.bin` 里了  
 现在需要从 `payload.bin` 里将这些分区`"解压"`出来

## 操作

### 下载 payload-dumper-go

- 一个工具[payload-dumper-go](https://github.com/ssut/payload-dumper-go/releases)
  ![gLNhC.png](https://s1.328888.xyz/2022/10/08/gLNhC.png)  
   我下载的是[payload-dumper-go_1.2.2_windows_amd64.tar.gz](https://github.com/ssut/payload-dumper-go/releases/download/1.2.2/payload-dumper-go_1.2.2_windows_amd64.tar.gz)

### 解压`tar.gz`得到`payload-dumper-go.exe`

![gLFjB.png](https://s1.328888.xyz/2022/10/08/gLFjB.png)

### 转储

- 刷机包放于同一目录
- 终端运行

```bash
.\payload-dumper-go.exe .\update.zip
```

![gLCck.png](https://s1.328888.xyz/2022/10/08/gLCck.png)

## 结果

得到`payload.bin`里的镜像
![gL1NJ.png](https://s1.328888.xyz/2022/10/08/gL1NJ.png)

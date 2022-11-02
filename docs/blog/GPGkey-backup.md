# 备份与恢复GPG密钥

## 查看本机gpg密钥id
```bash
gpg --list-keys
```

## 备份公钥
```bash
gpg --export 密钥id -o publickey.gpg
```
## 备份私钥
```bash
gpg --export-secret-keys 密钥id -o secretkey.gpg
```

默认导出二进制格式, 加入`--armor`选项可以将密钥以ascii导出.

## 恢复
```bash
gpg --import publickey.gpg
gpg --import secretkey.gpg
```
# 多平台换行符

在不同的操作系统，对于换行符的表示是不一样的。也就是说，当我们在编辑一个文件时，在键盘上按下回车键的时候，对于不同的操作系统保存到文件中的换行符是不一样的。

- CR: 表示回车 `\r`
- LF: 表示换行 `\n`
- CRLF: 表示回车换行 `\n`

敲下回车键，不同的操作系统保存到文件的值：

- Windows: CRLF
- Linux/Unix: LF
- Max OS: CR
- Max OS X: LF

## Git 自动对换行符进行转换

Git 为了解决该问题，会自动对换行符进行转换。转换的方案有3种：

1. 在提交时将 CRLF 转换为 LF，在拉取（检出 checkout）时将 LF 换行符替换成 CRLF（Windows 默认方案）。
2. 在提交时将 CRLF 转换为 LF，在拉取（检出）时不进行转换（Linux 和 MacOS 默认方案）。
3. 不进行转换。

## 指定换行符转换方案

```sh
# 提交时转换为 LF，检出时转换为 CRLF
git config --global core.autocrlf true

# 提交时转换为 LF，检出时不转换
git config --global core.autocrlf input

# 提交检出均不转换
git config --global core.autocrlf false
```

## 开启 safecrlf 检查

```sh
# 拒绝提交包含混合换行符的文件
git config --global core.safecrlf true

# 允许提交包含混合换行符的文件
git config --global core.safecrlf false

# 提交包含混合换行符的文件时给出警告
git config --global core.safecrlf warn
```

## 通过 .gitattributes 进行修改

.gitattributes 是针对一个单一的仓库的。[官方文档](https://git-scm.com/docs/gitattributes)

## 参考

1. [Git中CRLF与LF的转换](https://blog.csdn.net/u011069294/article/details/103809307)

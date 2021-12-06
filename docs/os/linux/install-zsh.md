# Linux 安装 zsh

在 Ubuntu 或 CentOS 系统中安装 zsh，并进行简单配置。

## 安装 zsh

```sh
# 查看服务器有哪些 shell 可用
cat /etc/shells

# 查看当前使用的 shell
echo $SHELL

# Ubuntu 下安装 zsh
apt -y install zsh

# CentOS 下安装 zsh
yum -y install zsh
```

## 安装 oh-my-zsh

获取安装脚本

```sh
wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh
```

!!! info "国内镜像"
    如果无法下载，也可以使用国内镜像
    ```sh
    wget https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh
    ```
    下载后需要对其进行修改
    ```sh title="install.sh"
    {--REPO=${REPO:-ohmyzsh/ohmyzsh}--}
    {--REMOTE=${REMOTE:-https://github.com/${REPO}.git}--}
    {++REPO=${REPO:-mirrors/oh-my-zsh}++}
    {++REMOTE=${REMOTE:-https://gitee.com/${REPO}.git}++}
    ```

执行脚本

```sh
sh install.sh
```

## 插件配置

安装字体

```sh
git clone https://github.com/powerline/fonts.git
cd fonts && sh install.sh
```

安装插件

```sh
cd ~/.oh-my-zsh/custom/plugins
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
git clone https://github.com/zsh-users/zsh-autosuggestions.git
```

编辑配置文件

``` title="~/.zshrc"
plugins=(
    git
    wd
    zsh-syntax-highlighting
	zsh-autosuggestions
)
```

应用配置

=== "zsh"

    ```sh
    zsh
    ```

=== "source"

    ```sh
    source ~/.zshrc
    ```

## 参考

1. [Ubuntu|安装oh-my-zsh](https://www.jianshu.com/p/ba782b57ae96)
2. [oh-my-zsh国内镜像安装和更新方法](https://www.jianshu.com/p/6b47198fd430)
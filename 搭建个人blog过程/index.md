# 搭建个人blog过程


作为一个希望在后端开发这个道路上越走越远的学生，我还是很希望自己可以成为一个大佬的，所以我觉得应该去做一个个人blog，所以才有了这个❤️Alancy’s site

这个博客是基于hugo开源网站生成器以及github所建立的，但是目前网络上关于hugo网站搭建的教程只适用于旧版本，因此我在这里分享一下25年4月新版hugo搭建网站的教程(macOS)

如有愚钝之处，请您轻点骂🫡

### 第一步：homebrew安装

如果您的mac上已经安装了homebrew，请直接跳转第二步！

在浏览器上搜索🍺[Homebrew](https://brew.sh)，进入官网后将看到

<img src="./images/image-20250420191328185.png">

将这段代码复制到终端并执行。

下载完成后，执行`ls`命令 ，可以看到在当前目录下存在一个`install`文件夹。

`cd`进入，再次执行`ls`命令，可以看到install文件夹下存在`install.sh`文件。

此时，进入[清华大学开源软件镜像站](https://mirrors.tuna.tsinghua.edu.cn)中搜索homebrew

<img src="./images/image-20250420192052622.png">

点击进入第一个[homebrew](https://mirrors.tuna.tsinghua.edu.cn/help/homebrew/)，复制页面中所提示的首次安装homebrew应在终端输入设置的环境变量：

```shell
export HOMEBREW_ API_DOMAIN="https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles/api" 
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.tuna.tsinghua.edu.cn/homebrew-bottles"
export HOMEBREW_BREW_GIT_REMOTE="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git"
export HOMEBREW_CORE_GIT_REMOTE="https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git"
export HOMEBREW_PIP_INDEX_URL="https://pypi.tuna.tsinghua.edu.cn/simple"
```

在终端内执行`cd ~`进入家目录，通过`code .`在visual studio code中打开。

新建`.bashrc`文件，将复制好的代码粘入文件并保存。

新建`.zshrc`文件，输入一下代码并保存：

```shell
source .bashrc
#homebrew path
export PATH="/opt/homebrew/bin:$PATH"
export HOMEBREW_NO_INSTALL_CLEANUP=1
export HOMEBREW_NO_ENV_HINTS=1
export HOMEBREW_NO_ENV_HINTS=1
export HOMEBREW_NO_ENV_HINTS=1
```

回到终端，执行以下命令并输入密码：

```shell
/bin/nash install.sh
```

回车后等待安装，安装完成后，执行`brew version`命令后，返回homebrew版本号，即为安装成功。

### 第二步：安装hugo

进入终端，执行以下命令以安装hugo：

```shell
brew install hugo
```

执行Hugo version命令，返回hugo版本，即为安装成功。

### 第三步：建立你的第一个网站

在终端执行以下命令以建立第一个项目：

```shell
hugo new site your-site
```

 在hugo官网中找到一款你喜欢的主题(文章中以LoveIt为例)

进入[LoveIt主题Github官网](https://github.com/dillonzq/LoveIt)，选择版本并克隆到`/your-site/themes`中

进入[LoveIt主题官方文档](https://hugoloveit.com/theme-documentation-basics/)，按照相关步骤并根据自身需求依次进行配置（配置文件的图像 路径应在/static下面）。

执行hugo server命令，正常执行即为配置成功。


我的vim配置
===
这个配置fork自
	
	git://github.com/tlhunter/Vim-PHP-IDE.git
	
自己做了符合自己的修改
	
这个Vim的配置可以让Vim看起来类似IDE,我已经长使用的是MacVIM,所以在不同的环境中可能会发生写怪异的错误,目前为之,我只是计划在github上来简单管理我的Vim配置,特别是可以让我轻易部署到不同的环境,我不认为这是一个社区项目.

我使用这个配置在Linux下大部分使用正常

预览
--
这份配置目的是运行单个MacVIM在一个屏幕使用,同时使用多文件编辑,在左侧是文件树,使用的是 _Nerdtree_ ,在右侧是当前文件的tags,使用的是 _ctags_.

当你编辑文件,你可以在在左边浏览,或者使用 _,t_ 来快速查找并打开一个文件,如果你想编辑其他文件,就像之前打开,或者使用 _o_ 来打开文件,或者使用 _i_ 分屏打开文件. 当你想在不同的文件之间切换,那下面的切换键会对你有帮助

Buffer 操作
---
* 使用 _,q_ 来关闭当前的buffer(一个不同的buffer将会替换它)
* 使用 _Ctrl h Ctrl l_ 来在不同的buffer之间切换 (或者使用 _Ctrl Left Ctrl Right_)

窗口
---
* 使用 _,h ,j ,k ,l_ 来在不同的窗口之间切换
* 使用 _,Q_ 来关闭当前窗口
* 使用 _,n_ 来打开或关闭左侧文件树
* 使用 _,y_ 来打开或关闭右侧tags
* 使用 _,t_ 来快速查找并打开文件

文件树 (NERDTree)
---
* 使用标准的活动键来移动
* 使用 _Ctrl j_ 和 _Ctrl k_ 来移动上下级文件夹
* 使用 _C_ 在当前文件路径创建一个新的节点
* 使用 _:Bookmark BookmarkName_ 来标记一个当前路径
* 使用 _B_ 来打开标记目录

Tag 列表 (Tag List)
---
* 使用 _s_ 来从新排序tags

HTML代码补全 (Zen Coding)
---
编辑HTML时,到编辑模式,输入:

    div>p#foo$*3>a

按Ctrl + Y 然后按逗号,你将看到:

    <div>
        <p id="foo1">
            <a href=""></a>
        </p>
        <p id="foo2">
            <a href=""></a>
        </p>
        <p id="foo3">
            <a href=""></a>
        </p>
    </div>

更多的信息,请看: https://raw.github.com/mattn/zencoding-vim/master/TUTORIAL

安装
---
在你的终端执行这些命令来安装(前提是你已经安装了GVim或者MacVIM),下面会有用rake来编译command-t的操作(这需要你的机器安装ruby环境)

    cd ~
    git clone git@github.com:cloudsben/PHPVim.git .vim
    ln -s ~/.vim/vimrc ~/.vimrc
    cd ~/.vim
    git submodule init
    git submodule update
    cd ~/.vim/bundle/command-t/
    rake make

功能
---
* 左侧的文件树
* 右侧函数,变量,类的tags
* 不同buffer的切换


安装需要环境
---
安装配置在你的Mac上(linux可以用apt来安装): http://thomashunter.name/blog/installing-vim-taglist-with-macvim-in-os-x/
* Ruby (用来编译 command-t)

截图
---
![Screenshot](http://thomashunter.name/wp-content/uploads/20120907-MacVim.png "Screenshot of Configuration")

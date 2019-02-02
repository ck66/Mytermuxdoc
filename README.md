# Hello,Termux

Termux是一个Android上的终端应用，它在Android上提供了一个轻量的独立环境，用于运行Linux应用。

假定你正在使用Linux或类Unix作为桌面OS，你可能很自然地想到在自己的Android手机上使用一些CLI应用，例如git,emacs,vim。那么，Termux可以满足你的需求。你只需要阅读[Termux.md](https://github.com/myfreess/Mytermuxdoc/wiki/Termux)，了解Termux作为一个Android应用的特殊之处以及Termux的独立环境与Unix的不同之处。


假定你对Unix一无所知，学习使用Termux也不会耗费你多少时间的。你需要从[Home.md](https://github.com/myfreess/Mytermuxdoc/blob/master/Home.md)开始读。我还制作了几份配置文件建议，并且写了详尽的注释，希望你会喜欢上Linux，并为Termux和Linux发行版的社区做一些力所能及的工作。这是myfreess当前能力的极限了，但不是你的。你会比myfreess做得更好。

# 目录:

+ [Proot.md](https://github.com/myfreess/Mytermuxdoc/wiki/Proot):关于Proot的简明文档。

+ [metasploit.md](https://github.com/myfreess/Mytermuxdoc/wiki/metasploit):Metasploit安装指南.

+ [FAQ.md](https://github.com/myfreess/Mytermuxdoc/wiki/FAQ):常见问题解答.

+ [fun.md](https://github.com/myfreess/Mytermuxdoc/blob/master/fun.md):一些有趣的东西。

+ [Old.md](https://github.com/myfreess/Mytermuxdoc/blob/master/Old_README.md):旧时所写，过于教程向。

+ [Install.sh](https://github.com/myfreess/Mytermuxdoc/blob/master/Install.sh):Package安装速查表，jupyter、pillow、Metasploit、nokogiri、zeronet安装,都在这里面了。

+ [Package.sh](https://github.com/myfreess/Mytermuxdoc/blob/master/Package.sh):工具使用速查表


# 写作:

pull request即可，但一定记得，在自己改动的文本旁边标上自己的名字。

还有，本人使用滚动更新法来更新文档，fork需谨慎

```bash
#自动化擦除commit工具
autocc()
{
if [ -d .git ]; then
        echo "看来commit即将消失……"
        old_branch=$(git branch | awk '{print $2}')
        git checkout --orphan null_branch
        git add -A
        git commit -am "porting to new branch"
        git branch -D $old_branch
        git branch -m $old_branch
        echo "如果git返回错误信息"
        echo "删除.git/hooks/pre-push"
        git push -f origin $old_branch
        unset old_branch
fi
}
```


# 文档状态

稳定，只修改陈旧过时内容和错误，不再添加新内容。

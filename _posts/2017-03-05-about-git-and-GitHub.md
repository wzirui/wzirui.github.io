# git & GitHub 初领略

暑假花了一点时间简单学习了一下git和GitHub的用法，因为短期内可能不会用得很频繁，这里总结一下基本使用方法和不错的学习资源，便于以后回顾和进一步学习。



## Git

git是目前较为流行的命令行版本控制工具，支持分支管理和远程协作等特性。

#### 不错的学习资源：

- [廖雪峰的git教程][1]  
写得还是挺不错，讲得比较清楚完整。对git来说，想要理解入门本身有一点复杂，建议看这个教程的时候遇到问题先放着，看到后面的章节很多问题就能自然解决了。git的远程协作这块不太好理解，建议多上手试验。

- [菜鸟教程的git教程][2]  
内容相对简单一些，可以作为上面[廖雪峰的git教程][1]的补充，建议从第三章“git工作流程”开始看，最后再看前两章。其中第四章“Git 工作区、暂存区和版本库”对工作区、暂存区和版本库的概念感觉比[廖雪峰][1]讲得清楚一些。

- [git简易指南][3]  
不适合初学者学习，没有讲解，更像是一个cheatsheet，但是作为cheatsheet整理得也不算好，建议对git熟悉了以后再看看，查漏补缺，文末提供了很多资源链接，适合进一步拓展学习。

- [git官方网站][4]和[git官方教科书《Pro Git》][5]  
官方资源，非常不错。《Pro Git》我还没有来得及仔细看，但是浏览了目录感觉内容应该很详尽，还有中文翻译版。如果只想看一份学习材料的话首推这个，毕竟应该是git的开发人员亲自写的。

- [阮一峰的博客][6]  
里面有多篇关于git和GitHub的文章，可以用其网站提供的搜索功能来查找相关文章。文章还没有仔细看过，但内容质量应该是不错的。文章的主题比较分散，建议对git有一定了解后再看。

#### 个人体会：

git命令行本身就提供了相对完善的信息提示，遇到一些基本的问题可以直接参考命令行提示。对于具体的某个指令想要详细了解其用法的话，还可以在命令行使用这个指令加`--help`参数，来查阅指令文档，非常详细。

由于git指令比较多，可以试着整理一个命令清单，能自己整理最好，回顾起来方便。另外，[廖雪峰的教程][1]在最后分享了一个清单，[阮一峰的这篇博客][7]也可以参考学习。

关于git图形化界面，我没有尝试过，但是感觉掩盖了一些git的本质，不是很推荐。

最后，简单说说对git的理解。在一个git仓库中，不同分支的所有提交版本共同近似构成一个版本树，树的每个结点是一个提交，每个新提交构成现有提交版本的子节点；每个分支维护一个指针，指向整个版本树某个结点，就代表这个分支当前的头部，从头部结点向祖先结点回溯，就可以得到该分支的版本序列（`git log`呈现的效果）。唯一的例外是merge两个分支的时候（非`fast-forward`的情况），新的提交作为新的子节点具有两个父结点，这时候用`git log --graph`向前回溯就能看到分支结构，当然最终两个祖先分支一定会再次汇合在某个祖先结点。

[1]: http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
[2]: http://www.runoob.com/git/git-tutorial.html
[3]: http://www.bootcss.com/p/git-guide/index.html
[4]: https://git-scm.com/
[5]: https://git-scm.com/book/en/v2
[6]: http://www.ruanyifeng.com/blog/developer/
[7]: http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html?bsh_bid=938838579



## GitHub

在学习了关于git的一些资料以后，现在你应该已经有了自己的GitHub账号，并且尝试创建过GitHub仓库。这一部分我主要写写GitHub还提供其它哪些不错的资源和功能。

#### 资源：

- [GitHub Guides](https://guides.github.com/)  
关于GitHub各种功能的简介，每个文章都很简单，适合对GitHub各个方面有一个入门级的认识，但想要深入理解某个功能的话还需要参考别的资料。

- [GitHub Help](https://help.github.com/)  
如果想要详细理解某类功能的话可以在这里查找，文章都是以专题的形式组织的，信息很全，条理清晰。在GitHub Help首页上，向下拉可以看见所有的专题。如果觉得手动查找麻烦，可以对某个关键词进行搜索，搜索结果是一个个文章，文章名字旁边有其所属的专题名称，点击以后可以进入相应的专题。

- [GitHub Services](https://services.github.com/)  
有一些GitHub官方提供的教程和资源。其中[On demand Training](https://services.github.com/on-demand/)是一个不错的git和GitHub教程。[这个资源页面](https://services.github.com/classnotes/)信息也很丰富，有一个不错的cheatsheet。

- [GitHub Blog](https://github.com/blog)  
关于GitHub的新特性、推广、使用、新闻事件等等相关的文章，貌似都是GitHub员工写的。内容对一般用户用处不大，如果不是GitHub深度发烧友的话不需要太多关注。

#### 使用：

- **Collaboration & Work Flow**  
git提供了版本管理和远程协作的基本工具，但是一个团队或开源社区具体使用怎样的协作方式，则是因人而异。想要了解目前主流的工作方式，可以参阅之前给出的学习资源，还可以看看这个[GitHub Help的专题](https://help.github.com/categories/collaborating-with-issues-and-pull-requests/)。

- **[GitHub Pages](https://pages.github.com/)**  
在仓库中添加静态网页，并通过特定的url进行访问，就可以构建项目主页或是自己的静态博客，具体使用方法将会在后面介绍。

- **[Gist](https://gist.github.com/)**  
类似于微型仓库，可以提交代码段、笔记或博客文章，并通过特定方式管理。在特定的显示方式下，也可以实现个人博客的效果。可以参考[这个专题](https://help.github.com/categories/gists/)和[知乎这个回答](https://www.zhihu.com/question/21343711)。不过目前必须翻墙才能使用。



## Markdown

markdown是一种标记语言，简洁有效，被GitHub社区大力推广和使用。在写Readme文件，发起Pull Request和Issue，以及使用GitHub Pages的时候，往往都会用到markdown，所以在这里介绍一下。

[献给写作者的Markdown新手指南](http://www.jianshu.com/p/q81RER)
和
[Markdown写作浅谈](http://www.jianshu.com/p/PpDNMG)
是对markdwon语言总体的初级介绍。

[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
和
[这个专题](https://help.github.com/categories/writing-on-github/)
详细介绍了markdwon语法，以及GitHub对markdwon的原生支持。

[Mou](http://25.io/mou/)
是一款不错的基于Mac的markdwon编辑器。



## GitHub Pages & Jekyll





## 一些实验
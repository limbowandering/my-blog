## 前言

这里是我学习Vim的笔记.



昨天我才意识到我自己这个人是多么矛盾, 我其实喜欢做的事情却因为莫名的胆怯, 畏惧, 和拖延症让我一直分不清我该做什么, 其实我就是喜欢我正在做的事情的. 

我相信键盘是比鼠标快的. 加上其他理由, 身为程序员, Emacs和Vim才是程序员该用的编辑器. 

我还是个Vim菜鸡. 这里的文档我会一直学习, 一直更新的.



## 目录

- [安装](#installation)

- ## [其他](#others)



## <a id="installation">安装</a>

因为平时我Windows和Mac和Linux都用... 所以这上面我都装了Vim.

### Windows安装Vim





```json
"  Gvim中文菜单乱码解决方案

" 设置文件编码格式
set encoding=utf-8
set fileencodings=utf-8,chinese,latin-1,gbk,gb18030,gk2312
if has("win32")
 set fileencoding=chinese
else
 set fileencoding=utf-8
endif

"解决菜单乱码
source $VIMRUNTIME/delmenu.vim
source $VIMRUNTIME/menu.vim

"解决consle提示信息输出乱码
language messages zh_CN.utf-8
--------------------- 
作者：JeanCheng 
来源：CSDN 
原文：https://blog.csdn.net/gatieme/article/details/55047156 
版权声明：本文为博主原创文章，转载请附上博文链接！
```



## <a id="others">其他</a>

一款chrome插件. Vimium. 
apt-cyg
=======

apt-cyg is a Cygwin package manager. It includes a command-line installer for
Cygwin which cooperates with Cygwin Setup and uses the same repository.

[github.com/transcode-open/apt-cyg][1]

[1]:https://github.com/transcode-open/apt-cyg

Operations
----------

~~~
install
  Install package(s).

remove
  Remove package(s) from the system.

update
  Download a fresh copy of the master package list (setup.ini) from the
  server defined in setup.rc.

download
  Retrieve package(s) from the server, but do not install/upgrade anything.

show
  Display information on given package(s).

depends
  Produce a dependency tree for a package.

rdepends
  Produce a tree of packages that depend on the named package.

list
  Search each locally-installed package for names that match regexp. If no
  package names are provided in the command line, all installed packages will
  be queried.

listall
  This will search each package in the master package list (setup.ini) for
  names that match regexp.

category
  Display all packages that are members of a named category.

listfiles
  List all files owned by a given package. Multiple packages can be specified
  on the command line.

search
  Search for downloaded packages that own the specified file(s). The path can
  be relative or absolute, and one or more files can be specified.

searchall
  Search cygwin.com to retrieve file information about packages. The provided
  target is considered to be a filename and searchall will return the
  package(s) which contain this file.
~~~

Quick start
-----------

apt-cyg is a simple script. To install:

    lynx -source rawgit.com/transcode-open/apt-cyg/master/apt-cyg > apt-cyg
    install apt-cyg /bin

Example use of apt-cyg:

    apt-cyg install nano
    
    
    
```

https://github.com/transcode-open/apt-cyg


https://blog.csdn.net/taanng/article/details/42216993
添加常用Linux命令

给Cygwin添加more/col/whereis等命令：安装util-linux包:apt-cyg install util-linux
给Cygwin添加telnet/ftp工具:apt-cyg install inetutils
给Cygwin安装dig命令
安装bind-utils包:apt-cyg install bind-utils
检查系统中已设置好DNS: ipconfig /all
得到Windows格式的路径名?
cygpath -d -m "`pwd`"

mount 查看挂在目录
进入F盘 
cd f:

配置盘符的链接
http://oldratlee.com/post/2012-12-22/stunning-cygwin
到F盘，要/cygdrive/df，可以新建符号链接/f，这样可以减少录入（MSYS的做法）
进入F盘 
cd /f

利用cygwin(其实windows 下 git bash 可以轻松实现
cp /f/kindleFile/三十六计.epub  /g/documents/
不需要创建软件接
)
cygwin下 文件复制(tab 自动补全)
window资源管理器 图形界面复制文件到 手机 kindle 太慢 



ln -s /cygdrive/f /f

自动补全不区分大小写
~/.bashrc文件中添加：

shopt -s nocaseglob
~/.inputrc文件中添加：

set completion-ignore-case on

$ cp /f/kindleFile/三十六计.epub  /g/documents/


dos环境 
cmd
复制
xcopy.exe F:\kindleFile\三十六计.epub  G:\

xcopy.exe f:kindleFile\xx\费曼物理学讲义.pdf g:

在linux环境下
xcopy.exe f:\\kindleFile\\xx\\费曼物理学讲.pdf g:
(自动补全不可用)
```

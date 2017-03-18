错误信息

使用TortoiseGit执行pull命令时显示

git.exe pull --progress --no-rebase -v "origin"

fatal: unable to access 'https://github.com/konsumer/arduinoscope.git/': error setting certificate verify locations:
CAfile: D:\Program Files\Git\mingw64/bin/curl-ca-bundle.crt
CApath: none

Git version 2.9.2.windows.1

解决方法

先打开git bash窗口 
执行命令：

git config --system http.sslcainfo "C:\Program Files (x86)\git\bin\curl-ca-bundle.crt"
（注意修改为正确的文件路径）或
git config --system http.sslverify false
我使用git config --system http.sslverify false命令解决问题。


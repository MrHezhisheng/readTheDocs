该文件夹功能包括但不限于测试的！

git 常用命令：

查看上提交的日志信息
>git log 
 :q
限定指定日期范围的log:
>git log --after '10-1-2019'
注意：使用 --after和--before 指定前后log

查看显示有变更的文件
>git status 

添加当前目录的所有文件到暂存区
>git add .

提交暂存区的指定文件到仓库区
>git commit -m "版本修改注释"

将上面的代码推送到远程存储库
>git push origin master 

将其本地存储库与远程存储库同步
>git pull 

检出，切换分支
>git checkout 

丢弃工作区的修改（改动）：
>git checkout -- <文件>...
eg:
mk10812@ITHPZJ01054 MSYS /h/esp32/mpy_latest/submodule/esp-idf
$ git status
位于分支 v3.1
您的分支和 'origin/master' 出现了偏离，
并且分别有 506 和 3703 处不同的提交。
  （使用 "git pull" 来合并远程分支）
尚未暂存以备提交的变更：
  （使用 "git add <文件>..." 更新要提交的内容）
  （使用 "git checkout -- <文件>..." 丢弃工作区的改动）
        修改：     components/bootloader/subproject/main/esp32.bootloader.ld
        修改：     components/driver/include/driver/uart.h
        修改：     components/driver/uart.c
修改尚未加入提交（使用 "git add" 和/或 "git commit -a"）
mk10812@ITHPZJ01054 MSYS /h/esp32/mpy_latest/submodule/esp-idf
$ git checkout -- components/

提交该分支到远程仓库
>git push --set-upstream origin new_branch

回退版本信息，丢弃修改内容
>git reset --hard HEAD

备份当前工作区的内容，保存到git 栈中，从最近的一次commit中读取相关内容
>git stash

从git栈中获取到最近一次stash进去的内容，恢复工作区的内容
>git stash pop

指定要合并的分支：
>git branch --set-upstream-to=origin v3.1
eg:
mk10812@ITHPZJ01054 MINGW64 /c/msys32/home/mk10812/project/mpy_/submodule/esp-idf (v3.1)
$ git branch --set-upstream-to=origin v3.1
Branch 'v3.1' set up to track remote branch 'master' from 'origin'.

查看远程分支
#git branch -a
带有“*”号的表示当前分支 

查看本地分支
#git branch

切换分支命令
#git checkout -b v1 origin/v1

切换回master
#git checkout master

git clone下载代码，中途断掉怎么办？
#git submodule update --init --recursive

python如何创建自己的pipy:(python2 运行有问题，但是Python3正常)
>python2 setup.py check 
>pip2 install twine
>python2 setup.py register
>python2 setup.py sdist upload

如何打包python包并上传到pypi库
1、执行打包代码"sudo python3 setup.py sdist"
2、注册登录"python3 setup.py register"
3、打包并上传代码到pipy库"sudo python3 setup.py sdist upload"

该文件夹功能包括但不限于测试的！

git 常用命令：

查看上提交的日志信息
>git log 
 :q
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
提交该分支到远程仓库
>git push --set-upstream origin new_branch

python如何创建自己的pipy:(python2 运行有问题，但是Python3正常)
>python2 setup.py check 
>pip2 install twine
>python2 setup.py register
>python2 setup.py sdist upload

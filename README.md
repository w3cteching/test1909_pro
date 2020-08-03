

# git是什么

1. git是一款分布式项目版本管理的工具

    git：分布式

    svn:集中式

# git常用命令

1. git init

```
在当前项目的目录下生成一个.git隐藏文件夹，为了跟踪项目代码
```



1. git add:将工作区的文件添加到暂存区
2. git commit:将暂存区的文件提交到到本地仓库（也称分支）
3. git push：将本地仓库快照提交到远程

```3.
将本地项目提交到远程的托管平台

常用托管平台：github,码云，gitlab....

提交到远程仓库之前：

1.在github上创建一个远程仓库
2.创建ssh(公钥和密钥)
 在本地上通过命令生成： ssh-keygen
 
 ssh-keygen -t rsa -b 4096 -C "aaaa@example.com"
 
 会自动生成 
 id_rsa（密钥）      
 id_rsa.pub（公钥）
 
3.本地创建一个用户名和邮箱

  git config --global user.name 'hjl888666'
  git config --global user.email 'hjl888666@126.com'
  
  测试是否与远端连通：
   ssh -T git@github.com
   
成功提示：   
Hi w3cteching! You've successfully authenticated, but GitHub does not provide shell access.
  
4.创建本地与远程仓库关联(git remote)

  格式：git remote add 远程主机名 远程仓库地址
  
  git remote -v ：查看远程仓库地址信息
  
  例如：
  git remote add origin git@github.com:w3cteching/test1909_pro.git

5.将本地代码推送到远端仓库

  git push -u origin master
  
  如果git push报错，首先咱们先拉取到本地，再推送
  
  git pull origin master --allow-unrelated-histories
   

```



1. git remote:
2. 
3. git pull
4. git fetch
5. git clone
6. git status:查看当前文件状态
7. 查看提交日志：

```
git log  
 简写：git log --pretty=oneline  只显示commit id 和提交说明
git reflog:查看所有历史提交记录
```



1. ....



> 记住：git管理的不是文件，管理的是”修改“
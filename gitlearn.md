## 学习git
</n>
使用 cd /d/git(目录位置)定位项目库。

使用git init 使它成为可以git控制的仓库。  
使用  
git config --global user.name "Your Name"  
git config --global user.email "email@example.com"  
来声明你的身份。

使用git add （文件名加后缀）例如 
git add reamme.txt  来添加到仓库  
使用git commit -m "说明"来提交到仓库.  
使用 git status 查看修改后但是并没有提交的文件  
使用 git diff +文件名 查看具体修改的内容  
**修改：**  
> git add 添加文件  
> git commit -m "文件名" 提交文件  
> 或者 git commit -am “文件名” 一步到位

**版本回溯:**
> 使用 git log 显示commit的记录  
> 回到上一个版本用git reset --hard HEAD^
> 回到上上个版本用git reset --hard HEAD^^  
> 回到上n个版本用 git reset --head HEAD~n  
> 回到现在版本（命令行窗口没有关闭）git reset --hard 版本号前几位但是也不能太少  
> 如果关闭了命令行窗口可以使用git reflog 记录你每次命令  
> 查看文件内容用cat 文件名

**git的工作区和暂存区:**  
>目录文件就是一个*工作区*，我的电脑工作区就是gitt文件夹  
>*版本库*是.git文件夹，版本库中有*暂存区*以及git自动为我们添加的一个*master分支*  
>git add 是把文件加入到暂存区，可以一次加多个，git commit 是把暂存区的文件提交到当前分支  

使用git checkout --file 来撤销修改到最近的一次 git add  或者 git commit 中  
使用rm在工作区删除文件  
使用 git rm file 删除文件 并用 git commit 提交 来从版本库中删除

**git与github对接操作**
> 如果第一次用要先 ssh-keygen -t rsa -C "youremail@example.com"创建自己的ssh密钥，在给出的路径下可以见到.pub是公钥,复制公钥，保留另一个私钥。    
> github允许你有多个密钥，这样的话，可以多人协作完成项目  
> 创建自己的githu仓库，在本地命令行中运行git remote add origin git@github.com:michaelliao/learngit.git（注意替换）  
> 接下来可以把本地库中的文件推送到远程库中  
> $ git push -u origin master（首次推送），之后的每次推送用git push origin master  
> 查看远程库消息git remote -v，解绑远程库git remote rm origin

**远程库克隆**
>首先在github上建立一个远程库。  
>然后克隆到本地上：git clone git@github.com:leemikeaaa/name.git(注意替换,已经提前转换到一个本地库中)  


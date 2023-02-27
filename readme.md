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
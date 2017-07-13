##一.github提交代码
###1.首先获得私钥,可在任何地方打开命令行输入以下:

	ssh -keygen -t rsa
###2.继续按回车键,直到在c盘生成一个.ssh文件则成功生成了私钥,一般默认生成在c盘/用户/administor/.ssh里,可点击进去查看,默认生成的.ssh文件会隐藏,可通过手动设置让隐藏的文件显示

###3.打开.ssh文件,将里面id-rsa.pub里的内容全部复制

###4.打开github,点击右上角setting---SHH and GPSS keys---New SSHkey,将复制的内容粘贴到key里面.

###5.创建仓库

###6.在仓库里面有个ssh地址将其复制.

###7.需要把项目放在哪,就在哪打开执行命令,输入:
	git clone 空格加上复制的SSH地址
###8.按下回车键后,会询问是否与本地连接,yes or no?输入yes,按回车
###9.此时本地的.ssh文件下会自动生成一个known_hosts的文件,这就意味着服务器已经把公钥给了本地
###10.同时仓库也克隆成功,在打开命令行所在地可以找到.
###11.此时可以在本地的项目里面也就是仓库,修改或编辑
###12.项目完成后按如下方式提交项目同步到github:
- CD 空格加上文件名称
- git add.(如果有多个文件需要提交则去掉.,把文件名称一个一个的添加,文件夹名称之间空格隔开
- git commit m"简单描述"
- git push
###13.这样代码或项目就已提交到github,可登入github进行查看确认.

##二.gitbook和github的连接
###1.首先需要创建好仓库,并把仓库克隆到本地
###2.在仓库点击右上角setting--->左侧installel Github Apps--->configure--->only select reponsitories(选择仓库),点击save保存.
###3.登录gitbook,点击左上角'+NewBook',在create a newbook里点击github.
###4.填写title,描述信息,选择仓库,最后点击creat book,这样gitbook和github就连接好了
###5.如果要在本地生成离线笔记,则在所在笔记文件夹再新建一个名为SUMMARY.md的文件,用于编写笔记的目录
###6.最后在所在文件位置执行如下指令
gitbook init

gitbook build --gitbook==2.6.7
###7.这样本地就生成了.html格式的笔记
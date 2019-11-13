 

1. 初始化git仓库（仓储）

‘git init’   //这个仓库会存放git对我们项目代码备份的文件



2. 配置个人信息:在git中设置当前使用的用户是谁(区分这个代码是谁做的)

每次备份,都会把备份者的信息存储起来

‘git config –-global user.name “steven”   //配置用户名,全局配置一次就好

‘git config –-global user.emil “[120816458@qq.com](mailto:120816458@qq.com) “// 配置邮箱

 

3. 把代码存储到.git仓库中

把代码放到仓库门口(暂存区):

‘git  add  ./readme.md’(文件路径)

把仓库门口的代码放到里面的房间中(版本库):

‘git commit –m(说明信息,必须有) “我们的第一个版本”

 

4. 代码更新,功能完善

‘git add ./readme.md

‘git commit –m “这是第二个版本”

这时仓库里就有两个版本的代码,方便以后回退

 

5. 第三版更新

‘git add ./readme.md

​        ‘git status //如果不知道具体执行哪一步,查看状态,看看执行到哪一步了

‘git commit –m “第三版” 

![img](file:///..\image\clip_image002.jpg)

Status:如果提交后又修改代码,则会出现红色的modified的字样,没修改即是:nothing to commit 

![img](file:///..\image\clip_image004.jpg)

Status:表明放到了门口(绿色),并没有提交(commit)



6. 在项目中添加了一个新的文件01.js

‘git add  ./    //把修改过的所有文件都放大大门口

​        ‘git commit  –m “添加一个新文件,加一个新功能”

 

7. 直接放到仓库中,不经过大门口

‘git commit  - -all  –m “标签”

 

8. git log 查看提交的日志

‘git log - -oneline   //每次提交显示在一行,简介明了

 

9. 版本退回(回复代码)

‘git log - -oneline’  //查看日志

‘git reset - -hard Head ~0   //0表示回退到最近一次修改前的版本,

 

10.通过版本号来切换版本

‘git reset - -hard ca3cc90

![img](file:///..\image\clip_image005.png)

ca3cc90(每次提交的版本号唯一标志)

 

‘git reflog’   //把每一次切换的记录都会显示出来

‘git log’ 只会显示Head标识以及以前的修改信息

 

 

10. 创建分支

‘git branch dev’

‘git branch’  //就可以看到我们创建到分支了

‘git checkout dev ‘//切换到dev 分支

分支中操作自己的代码

‘git checkout master’ //切回主分支

‘git merge dev ‘ //把dev 分支中提交的合并过来

 

11.

‘git branch –d dev’  //删除dev分支,要在别的分支删除

 

 

12.把代码上传到github

Github仓库地址:https://github.com/LCRuby/BlockChain.git

‘git  push  <https://github.com/LCRuby/BlockChain.git> master  //传到远程的master分支

 

![img](file:///..\image\clip_image006.png)

13.从服务器拿数据

要先在本地创建一个.git目录

‘git pull <https://github.com/LCRuby/BlockChain.git> master  //远程服务器master分支

 

还有一种方法是clone [地址]  //一般第一次时用这个

Git clone <https://github.com/LCRuby/BlockChain.git> 即可

 

14.用ssh方式上传代码

​        公钥和私钥

​        私钥自己用,公钥在网站上

生成公钥和私钥:

​        ‘ssh –keygen –t rsa –C  “1208164258@.com”

​        把公钥配置到远程服务器上(gitub)

​        ‘git push [git@github.com:LCRuby/test.git](mailto:git@github.com:LCRuby/test.git) master  //用ssh进行上传

这样别人上传就不需要我们的用户名和密码了

 

15.命令简写

 

![img](file:///..\image\clip_image007.png)

把长串的链接，，重命名为oriagin

 

![img](file:///..\image\clip_image008.png)

 

这里加上-u表示，下次直接可以git(pull/push)使用，不用再加ssh链接地址和master（仓储分支）

 

 

 

 

 

![img](file:///..\image\clip_image010.jpg)![img](file:///..\image\clip_image012.jpg)

![img](file:///..\image\clip_image013.png)

![img](file:///..\image\clip_image015.jpg)

‘git log ''只会显示Head标识以及以前的修改信息

 ![img](file:///..\image\clip_image017.jpg)

![img](file:///..\image\clip_image019.jpg) ![img](file:///..\image\clip_image021.jpg)

![img](file:///..\image\clip_image023.jpg) ![img](file:///..\image\clip_image025.jpg)![img](file:///..\image\clip_image027.jpg)

![img](file:///..\image\clip_image029.jpg)

![img](file:///..\image\clip_image031.jpg)![img](file:///..\image\clip_image033.jpg)
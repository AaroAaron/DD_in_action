
1、下载GitBash：http://www.git-scm.com/download/
默认选项安装
2、使用快捷方式打开

3、获取ssh秘钥，输入GitHub，使本地安装的Git Bash与网页的github建立信任关系，即github允许你gitbash上传拷贝项目文件
  01、获取秘钥命令：
$ ssh-keygen -t rsa -C “注册github的邮箱好” （此处为好男人自己的qq邮箱，1582665639@qq.com）
  02、输入以上命令后回车，会提示你key保存的目录，默认在C盘（这个无所谓毕竟很小的一个文件）——再按回车；
  03、输入密码（自己设定的密码，要牢记）——回车——再次输入确认密码——回车；
  04、出现红框中的提示说明秘钥已经创建成了。

4、复制刚刚生成的秘钥：更具上图提示的目录找到id_rsa.pub文件，用记事本或notepad++打开全部复制即可（ctrl+A —— ctrl+c）；

5、对本地的git bash与网页的guthub进行连接：
  01、登录你的github，点击头像下的下拉三角——Setting——SSH and GPG keys——New SSH key——输入标题名字(哪一个文件的ssh秘钥)与秘钥
  02、测试使用已经绑定成功：
      在git bash界面输入命令：
$ ssh -T -git@github.com 
       —— 回车 —— 输入yes —— 回车 —— 输入刚刚创建秘钥时设置的密码 —— 回车，
      提示successfuly即绑定成功了。
      ![如下图：](https://github.com/George-pig/DD_in_action/blob/master/2019070411152473.png)
$ git config --global user.name "your name"  git config --global user.email "your email"

6、把创建的库克隆下来到本地电脑中，方便以后进行上传代码
  自己的文件储存在d盘之中，所以你先需要将git bash定位在d盘中
$ cd /D
  库创建完成之后 会有一个网址出现在网页中
$ git clone 库创建完成后的网址
  D盘中出现以库名所创建的文件夹。
  
  打开这个文件夹，然后在其中创建一个任意格式，任意名称的文件。
  比如说文件夹test
  之后重新定位git 把位置，定位在你库的文件夹。
$ cd /D/test
  查看当前定位文件夹中的文件
$ ls
  
7、上传项目
  输入
$ git status
  查看当前版本库状态，在Untracked files(未跟踪文件)下，会出现红色的readme.txt，代表此文件还未被Git所管理。
使用
  如果想删除自己建立的分支，使用git branch -D feature，注意执行此命令后分支被强制删除，无法恢复。
$ git add readme.txt，将该文件加入缓冲区，如果你确定所有的修改都需要提交，可以使用$ git add .来加入所有修改。现在用
$ git status查看，将看到文件名变为绿色。

$ git commit -m '记录更新'
记录此次提交并上传

$ git push origin master
  在这里登陆你之前注册的GitHub账号之后点击login

8、克隆GitHub作者的内容
  01、复制作者克隆网址
  02、打开GitBash，$ cd /E/DD_in_action/文件夹，将位置定位到需要保存的位置
  03、输入$ git clone https://examples.com


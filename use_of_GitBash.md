
1、下载GitBash：http://www.git-scm.com/download/
默认选项安装
2、使用快捷方式打开

3、获取ssh秘钥，输入GitHub，使本地安装的Git Bash与网页的github建立信任关系，即github允许你gitbash上传拷贝项目文件
  01、获取秘钥命令：ssh-keygen -t rsa -C “注册github的邮箱好” （此处为好男人自己的qq邮箱，1582665639@qq.com）
  02、输入以上命令后回车，会提示你key保存的目录，默认在C盘（这个无所谓毕竟很小的一个文件）——再按回车；
  03、输入密码（自己设定的密码，要牢记）——回车——再次输入确认密码——回车；
  04、出现红框中的提示说明秘钥已经创建成了。

4、复制刚刚生成的秘钥：更具上图提示的目录找到id_rsa.pub文件，用记事本或notepad++打开全部复制即可（ctrl+A —— ctrl+c）；

5、对本地的git bash与网页的guthub进行连接：
  01、登录你的github，点击头像下的下拉三角——Setting——SSH and GPG keys——New SSH key——输入标题名字(哪一个文件的ssh秘钥)与秘钥
  02、测试使用已经绑定成功：
      在git bash界面输入命令：ssh -T -git@github.com —— 回车 —— 输入yes —— 回车 —— 输入刚刚创建秘钥时设置的密码 —— 回车，
      提示successfuly即绑定成功了。如下图：
      


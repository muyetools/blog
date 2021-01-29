---
layout: mypost
title: 配置git+Sourcetree，图形化管理github
categories: [git,Sourcetree]
---  
>因本人博客就是搭建在github的，修改博客内容使用的工具就是[git](https://git-scm.com/)和[Sourcetree](https://www.sourcetreeapp.com/)，两款都是免费的工具，用起来很顺手；也把这个搭建的过程记录下，供自己及需要的人进行参考。   

### 一、注册github
　　这里建议先安装[github加速](https://microsoftedge.microsoft.com/addons/detail/github%E5%8A%A0%E9%80%9F/ljceflkaahacpphaioldeledefadpmdp?hl=zh-CN)插件，这里是Microsoft Edge浏览器的地址；    
　　登录[Github](https://github.com/)网站，如果没有注册的先注册，点击[Sign up](https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)进行注册，注册只需要填写用户名，邮箱、密码，重复密码，填写后，点击注册即可，非常简单，这里就不多加补充。
### 二、下载安装git和Sourcetree   
　　git的下载建议去[腾讯软件](https://pc.qq.com/search.html#!keyword=git)下载，因为[git官网](https://git-scm.com/)国内下载速度确实太慢了。git的安装一路默认next下去就好了，不需要更改什么配置，安装在C盘就好了，安装好后，在任意空白的地方单击鼠标右键可以看到Git Bash here  
![Git Bash here](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/001.jpg)  
　　Sourcetree下载去[官网](https://www.sourcetreeapp.com/)下载就好了，速度还挺快的，或者在腾讯软件里面也能找到；  
　　双击打开安装包，出现如下图,选择bitbucket：
![图6](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/006.jpg)  
　　点击下一步后会跳转到登录账号的网页界面，　　
![007](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/007.jpg)
　　第一次安装的时候需要先注册一个账号，这里注册账号也仅需要邮箱即可注册，注册后，邮箱会收到一个链接，点击“verify your eamil”验证你的邮箱，，，注册完后填写注册的邮箱进行登录，第一次注册后的登录需要填写一个用户名，建议设置为字母；然后点继续；接下来有个问卷调查的界面，选择“SKIP”跳过就好了，如果接下来报错如下图，可能是你浏览器的问题，建议设置谷歌浏览器为默认浏览器再进行登录；
![008](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/008.jpg)
　　出现如下图点击"Grant access"
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/009.jpg)
　　接下来就会有段文字提示你成功了，然后关闭浏览器，软件界面就会提示
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/010.jpg)   
　　点击下一步,选择高级选项，勾选“默认配置自动换行处理（推荐）”，继续点击下一步
 ![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/011.jpg)
软件继续开始下载，因网络问题，下载可能有点慢，需要点耐心，如果一直失败，可能需要一个梯子，这个自己想办法解决，直到出现“工具安装完成”点击下一步，后面一直默认下一步即可；安装好后，安装界面会自动关闭，你点击桌面图标打开会出现如下图，说明安装成功，这个时候你可以先选中否，先配置好git；
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/012.jpg)

### 二、配置git 和 Sourcetree
1. 鼠标右键点击空白位置，左键点击上图中的“Git Bash Here”就会打开git的命令行界面；
2. 设置用户名和邮箱；  
```
git config --global user.name 'github用户名称'    
```  
```
git config --global user.email 'github登录邮箱'
```  
3. 生成私钥和公钥
```
ssh-keygen -t rsa -C 'github登录邮箱'
```  
输入后一直按回车键，会提示你是否需要设置密码，一般不设置就好；  
![图](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/002.jpg)  
生成的密钥文件一般保存在"C/users/用户名/.ssh/"文件夹中，具体可看上方截图中的your public key has been saved in "路径"；
4. 打开密钥文件夹    
"id_rsa"是私钥，“id_rsa.pub”是公钥  
![密钥](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/003.jpg)  
用windos自带的记事本程序打开公钥，可以看到一大串文本字符，复制这些字符串；  

6. 点击[sign in](https://github.com/login?return_to=%2Fjoin%3Fref_cta%3DSign%2Bup%26ref_loc%3Dheader%2Blogged%2Bout%26ref_page%3D%252F%26source%3Dheader-home)登录github的账号，登录后点击右上角的头像，选择设置"setting",找到ssh key菜单项，选择"new Ssh Key" 然后粘贴刚才复制的公钥填入到key当中，标题可以随便命名，自己好记就行，如下图所示：
![图](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/004.jpg)
填写后点击“Add SSH Key”进行保存；
7. 验证SSH key  
```  
ssh -T git@github.com
```  
输入“ssh -T git@github.com”对刚才新增的公钥进行验证，第一次验证可能有个选项需要你输入，输入yes即可，如果出现如下图所示，说明验证通过，配置完成后".SSH"文件夹中会多一个known_hosts的文件，不要删除；
![图5](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/005.jpg)  
7. Sourcetree 软件配置
我们都知道git是一个命令行的软件，而Sourcetree则是将命令行都转化成了可视化操作的界面，也就是点点点就是完成github项目的管理。
上一步我们已经安装好了 Sourcetree，现在我们打开它,如下图点击“工具”-“选项”
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/013.jpg)
8. 配置SSH私钥
　　请按下图中一样配置好，注意框中的选项“Open SSH”，然后点击确认，这样 Sourcetree 软件就配置好了，接下来就能正常使用了；
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/014.jpg)

9. github创建项目
　对于咱们新手来说，第一次肯定要创建一个项目或者fork别人的一个项目，这里讲讲创建，进入github，点击右上角头像，然后选择 New repository 来新建一个项目仓库，按我下图中填写你所需要的仓库属性；项目名称最好填写英文，
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/018.jpg)
填写完后，仓库就创建完了，然后如下图，复制项目地址；
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/019.jpg)

10.使用 Sourcetree 克隆clone项目；
粘贴刚才的地址在url栏中，选择你要将项目保存在本地的地址，然后点克隆
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/020.jpg)
11. 克隆后项目里面的文件就会被下载下来，由于我们是新建的项目，所以里面只有一个RDADME的描述文件，我们新建一个txt文件，然后回到Sourcetree就会发现有个未暂存的文件，点击暂存所有，就会到已暂存文件当中，然后我们点击左上角的拉取，拉取成功后，点击右下角的提交，在提交前可以在下面的对话框中填写关于你本次提交的内容是干嘛用的，描述下，再点击推送，稍等一会，文件就被提交上去了，
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/021.jpg)
如果过程中，出现下面的对话框，点击打开浏览器就行了  
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/022.jpg)  
如果过程中，出现以下对话框，输入github的账号密码，点击登录就行了；  
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/023.jpg)  
回到github界面，发现已经被上传成功了，鼓励一下自己，你真棒！
![](https://muye-1302115079.cos.ap-guangzhou.myqcloud.com/%E5%9B%BE%E5%BA%8A/markdown/%E9%85%8D%E7%BD%AEgit%2BSourcetree/024.jpg)
### 觉得教程不错，记得点个赞，留个言哟！
# ssh-keygen--t-ed25519--C-
申请LSPosed官方内测教程
首先我们打开MT管理器，进入终端模拟器

复制粘贴到终端模拟器以下文本，将双引号里面的电子邮箱替换成你 GitHub 绑定的邮箱

ssh-keygen -t ed25519 -C "电子邮箱"

粘贴之后，把你自己GitHub绑定的电子邮箱替换到这里面，然后点击回车

点击回车之后，这里提示你设置密码
如果不想设置密码，就直接点击回车即可
我这里就不设置了，直接点进回车
点击回车之后还会再次让你输入刚才设置的密码，如果没有设置密码就直接再点击一次回车即可
如果有设置密码，就输入刚才设置的密码，然后点击回车

之后会提示你的 身份验证信息（账号标识）和公钥存放的位置分别在哪个地方
这时候我们可以退出终端，打开公钥存放的目录
/data/user/0/bin.mt.plus/files/term/home/.ssh/id_ed25519.pub
复制上面的路劲，然后按照图片上面的操作即可跳转到路径的地方

打开这个路径之后，我们点击 id_ed25519.pub 选择编辑文本
复制里面的内容(ssh开头)

我们打开GitHub的主页： https://github.com/dashboard 

登录你自己的账号，随后进入设置，点击SSH and GPG keys，随后找到SSH keys点击New SSH key

点击New SSH key之后，找到：Add new SSH Key

第一个输入框是输入你密钥名称（自己给密钥起个名字）
第二个输入框粘贴你刚才从id_ed25519.pub中复制的密钥
两个都输入完成之后点击 Add SSH key(添加密钥)

之后出现You have successfully added the key '你起的名字'. 就代表密钥已经添加成功了

接下来我们开始申请LSPosed内测：
打开LSPosed官方频道
第一步：解密base64
复制echo里面的内容

aHR0cHM6Ly90Lm1lLytWb1g3U1N6UjZVVXlOMkkx
HYRK3Yp2VeEgngjF8hpuoyvYYIjEKQQr
https://t.me/+NfHztfyNBZs2ZDll

我们可以在这个网站里面进行解密base64： https://www.toolhelper.cn/EncodeDecode/Base64 

输入base64编码，随后点击base64解码即可解密成功

成功之后我们点击内测的频道链接，请求加入群组

发送申请之后，会有个机器人主动给我们发信息
点击Verify 验证

这个地方就是申请条件
接下来教你们如何用GitHub SSH私钥签名并提交《重点》

echo -n apsyP94WVCcHzt1g8WRts1U1KqHbRTHC | ssh-keygen -Y sign -n lsposed -f ~/.ssh/<your-key>

apsyP94WVCcHzt1g8WRts1U1KqHbRTHC
这个是我的挑战码（每个人的挑战码都不一样）

ssh-keygen -Y sign
使用 ssh-keygen 工具的签名模式

<your-key>:
指定身份验证信息（账号标识）文件的完整路径

随后复制下方代码，在终端执行：
echo -n 挑战码 | ssh-keygen -Y sign -n lsposed -f 身份验证信息（账号标识）的完整路径

执行完上述命令后，终端会返回一个签名
格式如下：
-----BEGIN SIGNATURE-----
<签名内容>
-----END SIGNATURE----

接下来我们复制这个签名提交即可
输入你的GitHub用户名和刚才生成的SSH密钥

点击Submit（提交）
教程到这里就结束啦～
有什么问题可以在评论区留言哦

#Lsposed#
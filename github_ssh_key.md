## GitHub 创建 SSH key

1. 启动终端


2. 检查是否已经有SSH Key：
    
    >cd ~/.ssh
    
    >ls
    
    列出该目录下的文件，看是否存在 id_isa 和 id_isa.pub 文件（也可以是别的文件名，只要 yourName 和 yourName.pub 存在）
    
3. 生成新的Key：（引号内的内容替换为你自己的邮箱）

   >ssh-keygen -t rsa -C "your_email@youremail.com"

  输出显示：

    >Generating public/private rsa key pair. Enter file in which to save the key 
    (/Users/your_user_directory/.ssh/id_rsa):<press enter>

  直接回车，不要修改默认路劲。

    >Enter passphrase (empty for no passphrase):<enter a passphrase>
    Enter same passphrase again:<enter passphrase again>

  设置一个密码短语，在每次远程操作之前会要求输入密码短语！闲麻烦可以直接回车，不设置。

4. 成功：

    >Your identification has been saved in /Users/your_user_directory/.ssh/id_rsa.
    Your public key has been saved in /Users/your_user_directory/.ssh/id_rsa.pub.
    The key fingerprint is:
    ... ...

5. 提交公钥：

   5.1 
   在刚刚安装成功的提示中有文件位置
   
   ![](https://upload-images.jianshu.io/upload_images/9691564-227e65ce11905591.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
   
   在此找到“id_rsa.pub”文件，打开，复制内容到剪贴板。
   
   5.2 打开 https://github.com/settings/ssh ，点击 Add SSH Key 按钮，粘贴进去保存即可。
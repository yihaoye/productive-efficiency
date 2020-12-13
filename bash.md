## 最常用的 Unix/Linux 命令
  
ssh 登录到远程主机  
`$ ssh -l jsmith remotehost.example.com`  
  
比较的时候忽略空白符  
`$ diff -w name_list.txt name_list_new.txt`  
  
设置全局环境变量  
`$ export ORACLE_HOME=/u01/app/oracle/product/10.2.0`  
  
`ls -a`  
`pwd`  
`cd`  
  
ftp命令和sftp命令的用法基本相似连接ftp服务器并下载多个文件  
`$ ftp IP/hostname`  
`ftp> mget *.html`  
  
显示远程主机上文件列表  
`ftp> mls *.html -`  
  
设置一个每十分钟执行一次的计划任务  
`*/10 * * * * /home/ramesh/check-disk-space`  
  
查看当前正在运行的所有进程  
`$ ps -ef | more`  
  
kill用于终止一个进程。一般我们会先用ps -ef查找某个进程得到它的进程号，然后再使用kill -9 进程号终止该进程。你还可以使用killall、pkill、xkill来终止进程  
`$ ps -ef | grep vim` -> (ramesh    7243  7222  9 22:43 pts/2    00:00:00 vim)  
`$ kill -9 7243`  
  
删除文件前先确认  
`$ rm -i filename.txt`  
  
递归删除文件夹下所有文件，并删除该文件夹  
`$ rm -r example`  
  
拷贝文件1到文件2，并保持文件的权限、属主和时间戳  
`$ cp -p file1 file2`  
  
拷贝file1到file2，如果file2存在会提示是否覆盖  
`$ cp -i file1 file2`  
  
将文件名file1重命名为file2，如果file2存在则提示是否覆盖  
`$ mv -i file1 file2`  
  
你可以一次查看多个文件的内容，下面的命令会先打印file1的内容，然后打印file2的内容  
`$ cat file1 file2`  
  
chmod 用于改变文件和目录的权限  
给指定文件的属主和属组所有权限(包括读、写、执行)  
`$ chmod 755 file.txt`  
755的权限就是：rwxr-xr-x。第一位7等于4+2+1，所以就是rwx，所有者有读取、写入、执行的权限；第二位5也是4+0+1，r-x，同组用户具有读取、执行权限；第三位5，代表公共用户有读取、执行的权限。  
  
在home目录下创建一个名为temp的目录  
`$ mkdir ~/temp`  
  
ifconfig用于查看和配置Linux系统的网络接口  
查看所有网络接口及其状态  
`$ ifconfig -a`  
  
mysql可能是Linux上使用最广泛的数据库，即使你没有在你的服务器上安装mysql，你也可以使用mysql客户端连接到远程的mysql服务器  
连接一个远程数据库，需要输入密码  
`$ mysql -u root -p -h 192.168.1.2`  
  
连接本地数据库  
`$ mysql -u root -p`  
你也可以在命令行中输入数据库密码，只需要在-p后面加上密码作为参数，可以直接写在p后面而不用加空格  
  
使用yum安装apache  
`$ yum install httpd`  
  
更新apache  
`$ yum update httpd`  
  
卸载/删除apache  
`$ yum remove httpd`  
  
ping一个远程主机，只发5个数据包  
`$ ping -c 5 gmail.com`  
  
使用wget从网上下载软件、音乐、视频  
`$ wget http://prdownloads.sourceforge.net/sourceforge/nagios/nagios-3.2.1.tar.gz`  
  
下载文件并以指定的文件名保存文件  
`$ wget -O taglist.zip http://www.vim.org/scripts/download_script.php?src_id=7701`  
  
查找指定文件名的文件(不区分大小写)  
`$ find -iname "MyProgram.c"`  
  
查找 home 目录下的所有空文件  
`$ find ~ -empty`  
  
以上参考[链接](https://gywbd.github.io/posts/2014/8/50-linux-commands.html)  

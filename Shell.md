#### Shell

​	date	//显示日期

​	echo arguments	//打印参数 参数由空格分隔

​	echo  "hello world"	//打印hello world

​	echo和date这些是计算机自带的内置函数，shell可以搜索它们通过环境变量//环境变量在启动shell时设置，例如主目录的地址，用户名。

​	echo $PATH	//打印路径列表，shell在这些路径中搜索程序	//$PATH是路径变量(path variable)

​	which echo	//打印echo的路径	

​	/c/Users/Jay/bin	//这个路径中，开头的斜杠表示从文件系统的顶部开始，然后查看名为“c”的目录，然后查看名为“Users”的目录，然后查看名为“Jay”的目录，然后查看名为“bin”的目录。

​	windows系统上路径常用反斜杠"\\"，Linux和macOS上常用斜杠"/"。

​	绝对位置和相对位置：字面意思

​	pwd	//打印当前所在路径	//print working directory

​	cd /c	//切换到"c"目录	//change directory

​	.		//当前目录	//current directory

​	cd ..	//切换到父目录	//父目录 parent directory

​	Is	//打印当前目录所有文件	//list

​	Is 路径	//打印此路径下所有文件

​	cd ~	//回到主目录

​	cd -	//回到之前的目录	

​	ls --help	//打印ls的使用说明

​	ls -l	//打印当前目录所有文件，并显示详细信息	//use a long listing format

```
	drwxr-xr-x 1 Jay 197121       0 Jun 20 19:00 etc/
	-rwxr-xr-x 1 Jay 197121  137224 Jun  3 08:04 git-bash.exe*
```

​	d —— directory	r —— read	w——write	x——execute	- —— 没有权限

​	权限顺序：文件的所有者	拥有该文件的组	其他人

​	对于directory：	read —— 你是否被允许看到这个目录中的文件列表

​					    write——你是否被允许在该目录中重命名、创建或删除文件

​							//对文件有 write 对目录没有 write 不能删除文件

​					    execute——你是否被允许进入此文件	//可称为search

​							//若想要打开读取或写入文件，必须拥有该目录以及其所以父目录的执行权限

​	mv oldname newname	//重命名	//mv Shell.md Bash.md	//move

​	cp 原文件路径或名字 目的路径或名字
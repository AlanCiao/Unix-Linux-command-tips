#为搜索出来的字符串加上颜色
可以使用“`--color`”选项为`grep`查找出来的字符串着色：  
举个例子：  

    [root@localhost command]# grep --color [Cat] <<<"nixCraft"
输出为：  
nix<font color=red>C</font>r<font color=red>a</font>f<font color=red>t</font>

也可使用`egrep`命令：  

	[root@localhost command]# egrep --color -i 'Mon' ./scan.txt  
输出为：  
Nmap 6.46 scan initiated <font color=red>Mon</font> Jan 12 10:58:32 2015 as: nmap -PR -oN scan.txt 192.168.1.0/24  
Nmap done at <font color=red>Mon</font> Jan 12 10:58:32 2015 -- 256 IP addresses (0 hosts up) scanned in 0.04 seconds

	

技巧出处：[https://twitter.com/nixcraft/status/231473119817261056](https://twitter.com/nixcraft/status/234569703715135488)。
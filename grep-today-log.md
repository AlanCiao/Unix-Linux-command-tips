#只查看今天的日志
使用“`grep "$(date +%b\ %e)" /var/log/syslog`”命令只查看今天的日志信息：  
举个例子：  

    -bash-3.2$ grep "$(date +%b\ %e)" /var/log/syslog
	Jan 12 00:10:18 PONTUS sendmail[5727]: [ID 801593 mail.info] t0BNA1Lo005727: from=sa@xx.com, size=176, class=
	0, nrcpts=1, msgid=<201501112310.t0BNA1Lo005727@PONTUS.xx.net>, relay=root@localhost
	Jan 12 00:10:34 PONTUS sendmail[5914]: [ID 801593 mail.info] t0BNA1Lo005727: to=cc@xx.net, delay=00:00:33, xd
	elay=00:00:16, mailer=relay, pri=120176, relay=mailhost.xx.net. [10.10.8.90], dsn=2.0.0, stat=Sent (t0BNAWRn0
	00026 Message accepted for delivery)
	

技巧出处：[https://twitter.com/nixcraft/status/231473119817261056](https://twitter.com/nixcraft/status/231473119817261056)。
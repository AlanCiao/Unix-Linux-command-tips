#列举不符合某种模式的文件
使用“`ls -I`”命令可以列举不符合某种模式的文件：  
举个例子：  

    [root@localhost include]# ls -I 'z*'
	acl                   execinfo.h           ldap.h          nspr4                sched.h
	aio.h                 fcntl.h              ldap_schema.h   nss3                 scsi
	aliases.h             features.h           ldap_utf8.h     nss.h                search.h
	alloca.h              fenv.h               ldif.h          numpy                security
	alsa                  fmtmsg.h             libart-2.0      obstack.h            selinux
	ansidecl.h            fnmatch.h            libaudit.h      openssl              semaphore.h
	antlr                 fontconfig           libcgroup       panel.h              sepol
	a.out.h               form.h               libcroco-0.6    pango-1.0            setjmp.h
	argp.h                fpu_control.h        libdrm          paths.h              sgtty.h
	argz.h                freetype2            libelf.h        pcap-bpf.h           shadow.h
	ar.h                  fstab.h              libexslt        pcap.h               signal.h
	arpa                  ft2build.h           libgen.h        pcap-namedb.h        slapi-plugin.h
	.....


显示不以字母`z`开头的文件名。  

技巧出处：[https://twitter.com/nixcraft/status/217200352267739137](https://twitter.com/nixcraft/status/217200352267739137)。
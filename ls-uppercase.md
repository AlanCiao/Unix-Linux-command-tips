#`ls`命令显示以大写字母作为文件名开头的文件
使用“`ls /path/to/[[:upper:]]*`”命令可以显示以大写字母作为文件名开头的文件。  
举个例子：  

    [root@localhost /]# ls /usr/bin/[[:upper:]]*
	/usr/bin/AtoB            /usr/bin/GenIssuerAltNameExt   /usr/bin/PKCS12Export
	/usr/bin/AuditVerify     /usr/bin/GenSubjectAltNameExt  /usr/bin/POST
	/usr/bin/BtoA            /usr/bin/GET                   /usr/bin/PrettyPrintCert
	/usr/bin/CMCEnroll       /usr/bin/HEAD                  /usr/bin/PrettyPrintCrl
	/usr/bin/CMCRequest      /usr/bin/HtFileType            /usr/bin/RSA_SecurID_getpasswd
	/usr/bin/CMCResponse     /usr/bin/HttpClient            /usr/bin/RunSimTest
	/usr/bin/CMCRevoke       /usr/bin/IBMgtSim              /usr/bin/TokenInfo
	/usr/bin/CRMFPopClient   /usr/bin/Mail                  /usr/bin/X
	/usr/bin/ExtJoiner       /usr/bin/OCSPClient            /usr/bin/Xorg
	/usr/bin/GenExtKeyUsage  /usr/bin/PKCS10Client


技巧出处：[https://twitter.com/nixcraft/status/275006059209424896](https://twitter.com/nixcraft/status/275006059209424896)。
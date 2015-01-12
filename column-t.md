#以表格方式显示输出
使用“`column -t`”命令可以用表格化方式显示输出：  
举个例子：  

    [root@localhost /]# mount
	/dev/sda3 on / type ext4 (rw)
	proc on /proc type proc (rw)
	sysfs on /sys type sysfs (rw)
	devpts on /dev/pts type devpts (rw,gid=5,mode=620)
	tmpfs on /dev/shm type tmpfs (rw)
	/dev/sda1 on /boot type ext4 (rw)
	/dev/sda8 on /data1 type ext4 (rw)
	/dev/sdb1 on /data2 type ext4 (rw)
	/dev/sdc1 on /data3 type ext4 (rw)
	/dev/sda2 on /home type ext4 (rw)
	/dev/sda5 on /usr type ext4 (rw)
	/dev/sda6 on /var type ext4 (rw)
	none on /proc/sys/fs/binfmt_misc type binfmt_misc (rw)
	none on /sys/kernel/config type configfs (rw)
	[root@localhost /]# mount | column -t
	/dev/sda3  on  /                         type  ext4         (rw)
	proc       on  /proc                     type  proc         (rw)
	sysfs      on  /sys                      type  sysfs        (rw)
	devpts     on  /dev/pts                  type  devpts       (rw,gid=5,mode=620)
	tmpfs      on  /dev/shm                  type  tmpfs        (rw)
	/dev/sda1  on  /boot                     type  ext4         (rw)
	/dev/sda8  on  /data1                    type  ext4         (rw)
	/dev/sdb1  on  /data2                    type  ext4         (rw)
	/dev/sdc1  on  /data3                    type  ext4         (rw)
	/dev/sda2  on  /home                     type  ext4         (rw)
	/dev/sda5  on  /usr                      type  ext4         (rw)
	/dev/sda6  on  /var                      type  ext4         (rw)
	none       on  /proc/sys/fs/binfmt_misc  type  binfmt_misc  (rw)
	none       on  /sys/kernel/config        type  configfs     (rw)
	[root@localhost /]#
对比之后可以发现“`mount | column -t`”命令输出很清晰。  

技巧出处：[https://twitter.com/nixcraft/status/190898232228978688](https://twitter.com/nixcraft/status/190898232228978688)。
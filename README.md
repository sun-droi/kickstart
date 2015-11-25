# kickstart


tftp
boot memu: /var/ks/tftpboot/pxelinux.cfg


NFS: 
/etc/exports
	var/nfs          *
	/var/ks/packages  *
	/var/ks/centos6.5 *
	/var/ks/centos6.6 *


kickstart configure:
/var/www/html/


Post Scripts:
var/ks/packages


Service:
	1. NTP
	2. ssh-key pub
	3. Ansible



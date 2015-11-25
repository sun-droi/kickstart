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

Post Scripts and source files
/var/ks/packages
├── big_data.sh
├── bin.tar.gz
├── conf
│   ├── authorized_keys
│   ├── hostname_IP.sh
│   ├── hosts
│   ├── ntp.conf
│   ├── profile
│   ├── rc.local
│   ├── refresh-packagekit.conf
│   ├── snmpd.conf
│   ├── sshd_config
│   └── zabbix_agentd.conf
├── hosts.bak
├── repo
│   ├── ambari.repo
│   ├── CentOS-Base.repo
│   ├── HDP.repo
│   └── zabbix.repo
├── rpm
│   ├── epel-release-6-8.noarch.rpm
│   ├── htop-1.0.3-1.el6.rf.x86_64.rpm
│   ├── openssl-1.0.1e-30.el6.11.x86_64.rpm
│   ├── opt.tar.gz
│   ├── sbt
│   ├── sbt-0.13.8.rpm
│   ├── sbt-launch.jar
│   ├── zabbix-2.2.9-1.el6.x86_64.rpm
│   ├── zabbix-agent-2.2.9-1.el6.x86_64.rpm
│   └── zabbix-release-2.2-1.el6.noarch.rpm
└── tmp
    ├── ambari.repo
    ├── authorized_keys
    └── id_rsa.pub


Service:
	1. NTP
	2. ssh-key pub
	3. Ansible



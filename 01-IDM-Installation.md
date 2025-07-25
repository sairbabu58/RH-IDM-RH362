# Free IPA. Installation

# Issues:

https://access.redhat.com/solutions/6998846
```
$ yum reinstall platform-python-setuptools python3-requests
```
```
[root@service ~]# ipa-server-install 

ImportError: cannot import name 'parse_version' from 'pkg_resources' (unknown location)

```



# Installation:

https://www.digitalocean.com/community/tutorials/how-to-set-up-centralized-linux-authentication-with-freeipa-on-centos-7
https://centlinux.com/install-freeipa-on-rocky-linux/
```
$ Create a VM with 2 CPU and 4 GiB Memory
$ Configure IP and Hostname
$ Disable selinux and firewalld 
```

# Configuring the Random Number Generator
```
$ yum install rng-tools
$ systemctl start rngd
$ systemctl enable rngd
$ systemctl status rngd
```





```
$ dnf install -y freeipa-server freeipa-server-dns freeipa-client
```
```
$ ipa-server-install 
$ ipa-server-install --uninstall
```
```
$ ipactl status
$ ipa config-show
```

# Create admin user
```
$ kinit admin
$ ipa user-find admin
```
```
$ https://ipa.ocp.example.com/ipa/ui
```




https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/9/html-single/installing_identity_management/index

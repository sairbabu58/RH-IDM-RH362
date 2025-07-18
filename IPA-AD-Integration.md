 
# Configure IPA Server with different domain 'ocp.cancom.intern.local'
# Configure AD server with different domain  'test-ad.ocp4.local'

# DNS resolution is most IMP point.
# If require add dns entry on /etc/resolv.conf file 
```
nameserver IP-SERVER-IP
nameserver AD-SERVER-IP
nameserver DNS-SERVER-IP
```

https://access.redhat.com/solutions/7039515

https://access.redhat.com/articles/4301061

https://access.redhat.com/solutions/7039508

https://access.redhat.com/articles/6983735

https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/7/html/windows_integration_guide/trust-during#trust-req-ports

https://access.redhat.com/solutions/4237481

https://www.linuxsysadmins.com/integrating-idm-with-ad-cross-forest-trust/#google_vignette

```
$ kinit admin
$ ipa config-show
$ ipa trustconfig-show
```
```
$ ipa dnsconfig-show
$ ipactl restart
```
```
$ systemctl restart named-pkcs11
$ systemctl status named-pkcs11
$ systemctl restart ipa-dnskeysyncd
$ systemctl status ipa-dnskeysyncd
$ ipactl status
$ dig -t SRV _ldap._tcp.cancom.intern.local
$ dig -t SRV _kerberos._tcp.cancom.intern.local

```

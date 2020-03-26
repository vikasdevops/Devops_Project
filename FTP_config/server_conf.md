# server config
- Steps of FTP implementations
```
$ yum install vsftpd -y
```
- start the service
```
$ systemctl start vsftpd
$ systemctl restart vsftpd
$ systemctl enable vsftpd
```

- check active or inactive
```
$ systemctl status vsftpd
```
- firewall conf
```
$ firewall-cmd --permanent --add-service=ftp
$ firewall-cmd --reload

- config the file of vsftpd
```
$ vim /etc/vsftpd/vsftpd.conf
```
> anonymous_enable=NO     
uncommit chroot_local_user=YES    
add this line below it    
allow_writeable_chroot=YES
```
- restart the service
```
$ systemctl restart vsftpd
```
- Add directory to share
```
$ mkdir ftp-data
$ useradd ftpuser -d /ftp-data
$ passwd ftpuser


```
$ semange fcontext -a -t public_content_t `/ftp-data(/.* )?`          
$ restorecon --vvRF /ftp-data/

```


 - open browser    
   or
  -  ftp://(ip address)

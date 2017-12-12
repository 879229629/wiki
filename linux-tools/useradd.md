## useradd

新增用户

```
//
useradd -m username
//
passwd username
```

```
[zenggang@host ~]$ id
uid=1000(zenggang) gid=1000(zenggang) groups=1000(zenggang)

[root@host ~]# id zenggang
uid=1000(zenggang) gid=1000(zenggang) groups=1000(zenggang)

groupadd admin

usermod -a -G admin zenggang

// admin group sudo
%admin  ALL=(ALL)       ALL

```


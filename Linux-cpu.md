## 查看 CPU 信息

总核数 = 物理CPU个数 X 每颗物理CPU的核数 

总逻辑CPU数 = 物理CPU个数 X 每颗物理CPU的核数 X 超线程数

查看物理CPU个数 

```
grep 'physical id' /proc/cpuinfo | sort -u
```

查看每个物理CPU中core的个数(即核数)

```
grep 'core id' /proc/cpuinfo | sort -u | wc -l
```

查看逻辑CPU的个数

```
grep 'processor' /proc/cpuinfo | sort -u | wc -l
```

cpu 架构,主频及超线程

```
lscpu
```

32 bit or 64 bit

```
getconf LONG_BIT
```

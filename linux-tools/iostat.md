## iostat

磁盘 I/O 情况

iostat -xdk 1

 - -k     Display statistics in kilobytes per second.
 - -m     Display statistics in megabytes per second.
       

```
[zenggang@iZwz9e4qykj1h8fv8c7c8vZ ~]$ iostat -xdk 1
Linux 3.10.0-514.10.2.el7.x86_64 (iZwz9e4qykj1h8fv8c7c8vZ) 	12/11/2017 	_x86_64_	(1 CPU)

Device:         rrqm/s   wrqm/s     r/s     w/s    rkB/s    wkB/s avgrq-sz avgqu-sz   await r_await w_await  svctm  %util
vda               0.00     4.85    0.37    7.47    12.47   288.25    76.68     0.09   11.74   15.17   11.57   0.88   0.69

Device:         rrqm/s   wrqm/s     r/s     w/s    rkB/s    wkB/s avgrq-sz avgqu-sz   await r_await w_await  svctm  %util
vda               0.00     0.00    0.00    0.00     0.00     0.00     0.00     0.00    0.00    0.00    0.00   0.00   0.00

Device:         rrqm/s   wrqm/s     r/s     w/s    rkB/s    wkB/s avgrq-sz avgqu-sz   await r_await w_await  svctm  %util
vda               0.00     0.00    0.00    0.00     0.00     0.00     0.00     0.00    0.00    0.00    0.00   0.00   0.00

Device:         rrqm/s   wrqm/s     r/s     w/s    rkB/s    wkB/s avgrq-sz avgqu-sz   await r_await w_await  svctm  %util
vda               0.00     0.00    0.00    0.00     0.00     0.00     0.00     0.00    0.00    0.00    0.00   0.00   0.00

Device:         rrqm/s   wrqm/s     r/s     w/s    rkB/s    wkB/s avgrq-sz avgqu-sz   await r_await w_await  svctm  %util
vda               0.00     0.00    0.00    0.00     0.00     0.00     0.00     0.00    0.00    0.00    0.00   0.00   0.00

```

- rkB/s 每秒读取数据量 kB
- wkB/s 每秒写数据量 kB
- svctm I/O 请求平均服务时间, 单位毫秒
- await I/O 请求平均等待时间, 单位毫秒; 值越小,性能越好
- util 一秒钟有百分几的时间用于 I/O操作;接近 100%时, 表示磁盘宽带跑满, 需要优化程序或加磁盘
- rkB/s, wkB/s 根据系统应用程序不同有不同值, 但有规律: 长期,超大值读写，肯定不正常,需要优化程序读写
- svctm, await 值接近 表示几乎没有磁盘 I/O 等待, 磁盘性能好; 如果 await 远高于 svctm, 表示I/O队列等待过长，需要优化程序或换更加快磁盘
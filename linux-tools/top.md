## top 

```
top -c 然后按数字 1

top - 00:06:05 up 2 days, 15:26,  1 user,  load average: 0.00, 0.00, 0.00
Tasks: 142 total,   1 running, 141 sleeping,   0 stopped,   0 zombie
Cpu0  :  0.0%us,  0.3%sy,  0.0%ni, 99.7%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Cpu1  :  0.0%us,  0.3%sy,  0.0%ni, 99.7%id,  0.0%wa,  0.0%hi,  0.0%si,  0.0%st
Mem:   1039732k total,   897680k used,   142052k free,    54484k buffers
Swap:   266236k total,      368k used,   265868k free,   732428k cached

  PID USER      PR  NI  VIRT  RES  SHR S %CPU %MEM    TIME+  COMMAND                                                        7883 zenggang  20   0  808m  31m  22m S  0.3  3.1   7:25.12 vault server -dev
26685 root      20   0  2768 2028 1752 R  0.3  0.2   0:00.25 top -c                                                            1 root      20   0  2964 2076 1936 S  0.0  0.2   0:00.92 /sbin/init
    2 root      20   0     0    0    0 S  0.0  0.0   0:00.00 [kthreadd]                                                        4 root       0 -20     0    0    0 S  0.0  0.0   0:00.00 [kworker/0:0H]
    6 root      20   0     0    0    0 S  0.0  0.0   0:00.09 [ksoftirqd/0]                                                     7 root      20   0     0    0    0 S  0.0  0.0   0:07.08 [rcu_sched]
    8 root      20   0     0    0    0 S  0.0  0.0   0:00.00 [rcu_bh]                                                          9 root      RT   0     0    0    0 S  0.0  0.0   0:00.03 [migration/0]
```

### load average

- 任务队列平均长度(1分支,5分钟,15分钟前到现在平均值)
- 这三个值一般不大于CPU逻辑数, 如果长期大于说明 cpu 忙,负载高;否则表示cpu比较空闲
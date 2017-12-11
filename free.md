## free

free [-m/-g]

```
[zenggang@vpn ~]$ free -m
             total       used       free     shared    buffers     cached
Mem:          1015        865        149          0         51        708
-/+ buffers/cache:        104        910
Swap:          259          0        259
```

- 物理内存: 1015 M
- 应用程序可用内存: 910 M
- 应用程序可用内存/物理内存 > 70% 内存充足
- 应用程序可用内存/物理内存 < 20% 内存不足
- 20% < 应用程序可用内存/物理内存 < 70% 内存基本够用
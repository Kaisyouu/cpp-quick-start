# cpp-quick-start

core相关
* 打印当前core文件转储的位置
```bash
cat /proc/sys/kernel/core_pattern
```

* 常用的core_pattern
```bash
/var/crash/core.%e.%p.%t.%h.%s
```

* 查看core文件大小限制
```bash
ulimit -c
ulimit -c unlimited     # 取消限制，仅当前会话有效
```

* 修改核心转储文件格式
```bash
echo "/var/crash/core.%e.%p.%t.%h.%s" | sudo tee /proc/sys/kernel/core_pattern
sysctl -p
```
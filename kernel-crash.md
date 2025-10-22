安装对应版本的kernel-debuginfo包

`crash /usr/lib/debug/lib/modules/`uname -r`/vmlinux vmcore`


```
# 1: 启用sysrq 0: 关闭sysrq
echo 1 > /proc/sys/kernel/sysrq
# c: 触发crash重启
echo c > /proc/sysrq-trigger
```

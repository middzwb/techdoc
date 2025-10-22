安装对应版本的kernel-debuginfo包

`crash /usr/lib/debug/lib/modules/`uname -r`/vmlinux vmcore`


```
# 1: 启用sysrq 0: 关闭sysrq
echo 1 > /proc/sys/kernel/sysrq
# c: 触发crash重启
echo c > /proc/sysrq-trigger
```


mod -s epc /root/zwb/epc/epc.ko

查看成员偏移

```
# 16进制
struct epc_proc_request -ox
epc_proc_req_t -ox

# 某个成员偏移 10进制
epc_proc_req_t.r_timeout -o
# 16进制
epc_proc_req_t.r_timeout -x

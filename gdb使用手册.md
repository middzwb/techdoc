## gdb

**打断点**

```
b <file>
b <file>:<line>
```

**调试**

```
n 单步调试
```

**启动带参数的进程**

gdb增加`--args`参数即可，例：

```
gdb --args /opt/h3c/bin/epc -c 1 2 3
```

**格式化打印地址值**

格式为`x/nfu addr`
nfu参数含义

- n: 单元长度
- f: format 格式。x->16进制；u->10机制，c->char，o->8进制，t->2进制
- u: 打印单元。 b->byte,h->2字节，w->4字节，g->8字节

例：

```
x/16ub 0x12345678
```
10进制打印16个字节

**container_of**

```
p &(((struct mds_cdentry*)0)->rb_node)
```

**log**

```
(gdb) set logging file my-gdb-log.txt
(gdb) set logging on
(gdb) set logging off
(gdb) show logging

```

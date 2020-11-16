+++
Title = "Wireshark"
Date = 2020-03-26T16:41:35+08:00
Categories = []
# Keywords = []
Tags = []
Description = ""
Draft = true
+++


过滤器

捕获过滤器

BPF 过滤器

原语：  限定词 名称/数字

其中原语限定词分为：

type 指示类型 e.g. ``` host example.com ```
dir 出入方向 ``` dst port 80 ```
proto 协议类型 ``` udp ```

原语运算符 ``` and, or, not, &&, ||, ! ```

type 类型限定词

- host, port
- net ``` net ip mask 掩码 ```
- portrange

dir 类型限定词
- src, dst, src or dst, src and dst
- ra, ta, addr1, addr2, addr3, addr4


基于协议域过滤
### 猫咪银行

遇到这种买卖的web题一开始想到的是竞争，但随便点几下后发现有时间限制；  
然后测试理财产品买入功能容易发现买入分钟数过大时，取出时间和利息都会变的奇怪；  
输入0xffffffff以及0xffffffffffffffff测试了下溢出临界，前者正常后者异常，可能是是8字节存储；  
于是尝试计算  0xffffffffffffffff/60、0x7fffffffffffffff/60等容易引起恰好溢出的分钟数，在输入买入分钟0x7fffffffffffffff/60(153722867280912930)后则可以立即取出一笔巨款并购买flag。  

[返回](../)
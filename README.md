项目目的
=

send a tx on Bitcoin testnet, and parse the tx data down to every bit

项目实现
=

此项目由于测试币未申请成功，因此选取了比特币测试网交易信息中的一个交易进行分析，此处我们选取的为：c298fcc5eb1c39743426d86e3c11770a4b261189e0274ef88cdef732bd343bfc

![image](https://github.com/CLiangH/Picture/blob/main/bitcoin1.png)

关于交易信息的追踪，我们在此调用BlockCypher的API接口

![image](https://github.com/CLiangH/Picture/blob/main/bitcoin2.png)

在此图中我们可以看到，BlockCypher给出了许多接口，其中包括Bitcoin主链、Testnet测试链、Dash、BlockCypher等，我们在此调用Testnet测试链的API接口即可。（注意：只能用内网）

运行指导
=

函数直接打印其分析结果。

运行截图
=

根据图片我们可以看到，此笔交易有一笔输入，两笔输出，其中一笔输出是转给自己，说明这是在进行找零操作

纵观全局，里面包含区块头、难度、时间戳、Merkle根输入输出等参数信息，例如："preference": "medium"、"confirmed": "2022-07-25T16:07:49Z"、
  "received": "2022-07-25T16:07:49Z"

![image](https://github.com/CLiangH/Picture/blob/main/bitcoin3.png)

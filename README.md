# go-ethereum
以太坊客户端，以太坊客户端主要分成两类。一个是后台命令行客户端，如:geth（go语言）,parity（Rust语言）,他们是一个与以太坊网络交互的命令行客户端。
其余的命令行客户还有 ethereumjs-lib（javascript）,pyethapp(python),ruby-ethereum(ruby) ....主要 geth 使用的比较普遍，这里我就使用geth作为命令行客户端。
    2.mist 是属于可视化钱包，这么说吧，你在geth 客户端中生成的用户，以太坊币数量可以通过mist 钱包可视化展示。当然mist 不只有这些简单的功能，最重要的是能部署智能合约，发布，调用。其他还有很多轻钱包，如 lightWallet,metamask...
   下面是geth和mist下载地址，这里我使用的是windows系统安装。
      Geth :  https://geth.ethereum.org/downloads/    ## 本篇使用1.8.2，免安装zip
      Mist :  https://github.com/ethereum/mist/releases   ## 本篇使用0.10.0，免安装zip


MACdeMacBook-Air:bin MAC$ geth
INFO [11-23|22:00:23.135] Maximum peer count                       ETH=25 LES=0 total=25
INFO [11-23|22:00:23.147] Starting peer-to-peer node               instance=Geth/v1.8.17-stable/darwin-amd64/go1.11.1
INFO [11-23|22:00:23.148] Allocated cache and file handles         database=/Users/MAC/Library/Ethereum/geth/chaindata cache=768 handles=128
INFO [11-23|22:00:23.164] Writing default main-net genesis block 
INFO [11-23|22:00:23.727] Persisted trie from memory database      nodes=12356 size=1.88mB time=106.219704ms gcnodes=0 gcsize=0.00B gctime=0s livenodes=1 livesize=0.00B
INFO [11-23|22:00:23.730] Initialised chain configuration          config="{ChainID: 1 Homestead: 1150000 DAO: 1920000 DAOSupport: true EIP150: 2463000 EIP155: 2675000 EIP158: 2675000 Byzantium: 4370000 Constantinople: <nil> Engine: ethash}"
INFO [11-23|22:00:23.730] Disk storage enabled for ethash caches   dir=/Users/MAC/Library/Ethereum/geth/ethash count=3
INFO [11-23|22:00:23.730] Disk storage enabled for ethash DAGs     dir=/Users/MAC/.ethash                      count=2
INFO [11-23|22:00:23.730] Initialising Ethereum protocol           versions="[63 62]" network=1
INFO [11-23|22:00:23.731] Loaded most recent local header          number=0 hash=d4e567…cb8fa3 td=17179869184 age=49y7mo1w
INFO [11-23|22:00:23.731] Loaded most recent local full block      number=0 hash=d4e567…cb8fa3 td=17179869184 age=49y7mo1w
INFO [11-23|22:00:23.731] Loaded most recent local fast block      number=0 hash=d4e567…cb8fa3 td=17179869184 age=49y7mo1w
INFO [11-23|22:00:23.732] Regenerated local transaction journal    transactions=0 accounts=0
INFO [11-23|22:00:23.735] Starting P2P networking 
INFO [11-23|22:00:26.407] UDP listener up                          self=enode://ee23dd982fbcf787a18fe47f26e4a3d41170988ff2c2a6822d892cf1df2af1321732dc1e11c8dd98ab8e3714259b00ff39f34c68f0337a4011310d4232bee4bb@111.196.31.117:30303
INFO [11-23|22:00:26.408] RLPx listener up                         self=enode://ee23dd982fbcf787a18fe47f26e4a3d41170988ff2c2a6822d892cf1df2af1321732dc1e11c8dd98ab8e3714259b00ff39f34c68f0337a4011310d4232bee4bb@111.196.31.117:30303
INFO [11-23|22:00:26.413] IPC endpoint opened                      url=/Users/MAC/Library/Ethereum/geth.ipc
INFO [11-23|22:00:27.616] Mapped network port                      proto=udp extport=30303 intport=30303 interface="UPNP IGDv1-PPP1"
INFO [11-23|22:00:28.818] Mapped network port                      proto=tcp extport=30303 intport=30303 interface="UPNP IGDv1-PPP1"
INFO [11-23|22:00:46.425] Block synchronisation started




MACdeMacBook-Air:bin MAC$ geth --datadir data0 init genesis.json 
INFO [11-23|22:13:31.919] Maximum peer count                       ETH=25 LES=0 total=25
INFO [11-23|22:13:31.928] Allocated cache and file handles         database=/Users/MAC/Downloads/brew-1.0.5/Cellar/ethereum/1.8.17/bin/data0/geth/chaindata cache=16 handles=16
INFO [11-23|22:13:31.935] Writing custom genesis block 
INFO [11-23|22:13:31.937] Persisted trie from memory database      nodes=0 size=0.00B time=253.398µs gcnodes=0 gcsize=0.00B gctime=0s livenodes=1 livesize=0.00B
INFO [11-23|22:13:31.939] Successfully wrote genesis state         database=chaindata                                                                       hash=a0e580…a5e82e
INFO [11-23|22:13:31.939] Allocated cache and file handles         database=/Users/MAC/Downloads/brew-1.0.5/Cellar/ethereum/1.8.17/bin/data0/geth/lightchaindata cache=16 handles=16
INFO [11-23|22:13:31.943] Writing custom genesis block 
INFO [11-23|22:13:31.944] Persisted trie from memory database      nodes=0 size=0.00B time=3.865µs   gcnodes=0 gcsize=0.00B gctime=0s livenodes=1 livesize=0.00B
INFO [11-23|22:13:31.944] Successfully wrote genesis state         database=lightchaindata                                                                       hash=a0e580…a5e82e



=a0e580…a5e82e td=262144 age=49y7mo1w
INFO [11-23|22:14:43.829] Loaded local transaction journal         transactions=0 dropped=0
INFO [11-23|22:14:43.829] Regenerated local transaction journal    transactions=0 accounts=0
INFO [11-23|22:14:43.830] Starting P2P networking 
INFO [11-23|22:14:45.937] UDP listener up                          self=enode://f70f8613917de3e9868185608e243fee1046b907af9747626220eba47b6a3042e679b347793cb1ae03c1f5724e92760b0a9f33a6681d9cd36299a618fc411f54@[::]:30303
INFO [11-23|22:14:45.938] RLPx listener up                         self=enode://f70f8613917de3e9868185608e243fee1046b907af9747626220eba47b6a3042e679b347793cb1ae03c1f5724e92760b0a9f33a6681d9cd36299a618fc411f54@[::]:30303
INFO [11-23|22:14:45.942] IPC endpoint opened                      url=/Users/MAC/Downloads/brew-1.0.5/Cellar/ethereum/1.8.17/bin/data0/geth.ipc
Welcome to the Geth JavaScript console!

instance: Geth/v1.8.17-stable/darwin-amd64/go1.11.1
 modules: admin:1.0 debug:1.0 eth:1.0 ethash:1.0 miner:1.0 net:1.0 personal:1.0 rpc:1.0 txpool:1.0 web3:1.0



set dynamicportrange protocol=tcp startport=10000 numberofports=65534

MACdeMacBook-Air:bin MAC$ geth --datadir data1 --networkid 11 console --port 33034

Ethereum Wallet简介

Ethereum Wallet客户端对应的是Mist项目，现在此客户端大多都称为Ethereum Wallet，也有称作Mist客户端的，知道它们两个指的是通一个客户端即可。此客户端使用JavaScript进行开发，支持windows、linux和OSX三类操作系统，是一个图形化操作界面的客户端。介绍到这里，大家可能就明白了，如果你想通过API来调用以太坊的接口，选择此方式是行不通的。

Ethereum Wallet客户端主要是为用户提供可视化操作的客户端，下载安装之后通过相应的图形化界面即可进行创建账户、转账、查询余额等操作。【下载地址】，【安装教程】

Ethereum Wallet客户端主要功能

创建账户
兑换以太币：内置了比特币、其它竞争币与以太币兑换功能
部署智能合约：代币合约、众筹合约、自治组织合约等
以太币转账操作
备份钱包
等其他功能 
以上所有功能操作都是启动客户端程序之后，通过操作界面或菜单进行操作。智能合约部分需要事先编写好对应的代码，通过客户端进行发布。


admin.addPeer("enode://f70f8613917de3e9868185608e243fee1046b907af9747626220eba47b6a3042e679b347793cb1ae03c1f5724e92760b0a9f33a6681d9cd36299a618fc411f54@[::]:30303");


Geth客户端主要功能

JavaScript Console：通过后台进行命令操作；
Management API：管理相关的API；
JSON-RPC server：JSON-RPC相关调用API 
无论通过API或则console都可以进行相关操作，比如：
账号管理（创建账号、锁定账号、解除锁定等）；
查询账户信息；
查询交易信息；
查询gasPrice；
交易；
挖矿&停止挖矿；
部署智能合约
等其他相关功能。
使用Geth客户端可以通过对接API（目前交易平台常常使用的方式），或直接通过命令行进行操作。与Ethereum Wallet相比，没有可视化的操作界面，基本上都是通过命令来完成的。


命令用法
geth [选项] 命令 [命令选项] [参数…]
版本：
1.7.3-stable
命令:
account    管理账户
attach     启动交互式JavaScript环境（连接到节点）
bug        上报bug Issues
console    启动交互式JavaScript环境
copydb     从文件夹创建本地链
dump       Dump（分析）一个特定的块存储
dumpconfig 显示配置值
export     导出区块链到文件
import     导入一个区块链文件
init       启动并初始化一个新的创世纪块
js         执行指定的JavaScript文件(多个)
license    显示许可信息
makecache  生成ethash验证缓存(用于测试)
makedag    生成ethash 挖矿DAG(用于测试)
monitor    监控和可视化节点指标
removedb   删除区块链和状态数据库
version    打印版本号
wallet     管理Ethereum预售钱包
help,h     显示一个命令或帮助一个命令列表
ETHEREUM选项:
--config value          TOML 配置文件
--datadir “xxx”         数据库和keystore密钥的数据目录
--keystore              keystore存放目录(默认在datadir内)
--nousb                 禁用监控和管理USB硬件钱包
--networkid value       网络标识符(整型, 1=Frontier, 2=Morden (弃用), 3=Ropsten, 4=Rinkeby) (默认: 1)
--testnet               Ropsten网络:预先配置的POW(proof-of-work)测试网络
--rinkeby               Rinkeby网络: 预先配置的POA(proof-of-authority)测试网络
--syncmode "fast"       同步模式 ("fast", "full", or "light")
--ethstats value        上报ethstats service  URL (nodename:secret@host:port)
--identity value        自定义节点名
--lightserv value       允许LES请求时间最大百分比(0 – 90)(默认值:0) 
--lightpeers value      最大LES client peers数量(默认值:20)
--lightkdf              在KDF强度消费时降低key-derivation RAM&CPU使用
开发者（模式）选项:
--dev               使用POA共识网络，默认预分配一个开发者账户并且会自动开启挖矿。
--dev.period value  开发者模式下挖矿周期 (0 = 仅在交易时) (默认: 0)
ETHASH 选项:
--ethash.cachedir                        ethash验证缓存目录(默认 = datadir目录内)
--ethash.cachesinmem value               在内存保存的最近的ethash缓存个数  (每个缓存16MB ) (默认: 2)
--ethash.cachesondisk value              在磁盘保存的最近的ethash缓存个数 (每个缓存16MB) (默认: 3)
--ethash.dagdir ""                       存ethash DAGs目录 (默认 = 用户hom目录)
--ethash.dagsinmem value                 在内存保存的最近的ethash DAGs 个数 (每个1GB以上) (默认: 1)
--ethash.dagsondisk value                在磁盘保存的最近的ethash DAGs 个数 (每个1GB以上) (默认: 2)
交易池选项:
--txpool.nolocals            为本地提交交易禁用价格豁免
--txpool.journal value       本地交易的磁盘日志：用于节点重启 (默认: "transactions.rlp")
--txpool.rejournal value     重新生成本地交易日志的时间间隔 (默认: 1小时)
--txpool.pricelimit value    加入交易池的最小的gas价格限制(默认: 1)
--txpool.pricebump value     价格波动百分比（相对之前已有交易） (默认: 10)
--txpool.accountslots value  每个帐户保证可执行的最少交易槽数量  (默认: 16)
--txpool.globalslots value   所有帐户可执行的最大交易槽数量 (默认: 4096)
--txpool.accountqueue value  每个帐户允许的最多非可执行交易槽数量 (默认: 64)
--txpool.globalqueue value   所有帐户非可执行交易最大槽数量  (默认: 1024)
--txpool.lifetime value      非可执行交易最大入队时间(默认: 3小时)
性能调优的选项:
--cache value                分配给内部缓存的内存MB数量，缓存值(最低16 mb /数据库强制要求)(默认:128)
--trie-cache-gens value      保持在内存中产生的trie node数量(默认:120)
帐户选项:
--unlock value              需解锁账户用逗号分隔
--password value            用于非交互式密码输入的密码文件
API和控制台选项:
--rpc                       启用HTTP-RPC服务器
--rpcaddr value             HTTP-RPC服务器接口地址(默认值:“localhost”)
--rpcport value             HTTP-RPC服务器监听端口(默认值:8545)
--rpcapi value              基于HTTP-RPC接口提供的API
--ws                        启用WS-RPC服务器
--wsaddr value              WS-RPC服务器监听接口地址(默认值:“localhost”)
--wsport value              WS-RPC服务器监听端口(默认值:8546)
--wsapi  value              基于WS-RPC的接口提供的API
--wsorigins value           websockets请求允许的源
--ipcdisable                禁用IPC-RPC服务器
--ipcpath                   包含在datadir里的IPC socket/pipe文件名(转义过的显式路径)
--rpccorsdomain value       允许跨域请求的域名列表(逗号分隔)(浏览器强制)
--jspath loadScript         JavaScript加载脚本的根路径(默认值:“.”)
--exec value                执行JavaScript语句(只能结合console/attach使用)
--preload value             预加载到控制台的JavaScript文件列表(逗号分隔)
网络选项:
--bootnodes value    用于P2P发现引导的enode urls(逗号分隔)(对于light servers用v4+v5代替)
--bootnodesv4 value  用于P2P v4发现引导的enode urls(逗号分隔) (light server, 全节点)
--bootnodesv5 value  用于P2P v5发现引导的enode urls(逗号分隔) (light server, 轻节点)
--port value         网卡监听端口(默认值:30303)
--maxpeers value     最大的网络节点数量(如果设置为0，网络将被禁用)(默认值:25)
--maxpendpeers value    最大尝试连接的数量(如果设置为0，则将使用默认值)(默认值:0)
--nat value             NAT端口映射机制 (any|none|upnp|pmp|extip:<IP>) (默认: “any”)
--nodiscover            禁用节点发现机制(手动添加节点)
--v5disc                启用实验性的RLPx V5(Topic发现)机制
--nodekey value         P2P节点密钥文件
--nodekeyhex value      十六进制的P2P节点密钥(用于测试)
矿工选项:
--mine                  打开挖矿
--minerthreads value    挖矿使用的CPU线程数量(默认值:8)
--etherbase value       挖矿奖励地址(默认=第一个创建的帐户)(默认值:“0”)
--targetgaslimit value  目标gas限制：设置最低gas限制（低于这个不会被挖？） (默认值:“4712388”)
--gasprice value        挖矿接受交易的最低gas价格
--extradata value       矿工设置的额外块数据(默认=client version)
GAS价格选项:
--gpoblocks value      用于检查gas价格的最近块的个数  (默认: 10)
--gpopercentile value  建议gas价参考最近交易的gas价的百分位数，(默认: 50)
虚拟机的选项:
--vmdebug        记录VM及合约调试信息
日志和调试选项:
--metrics            启用metrics收集和报告
--fakepow            禁用proof-of-work验证
--verbosity value    日志详细度:0=silent, 1=error, 2=warn, 3=info, 4=debug, 5=detail (default: 3)
--vmodule value      每个模块详细度:以 <pattern>=<level>的逗号分隔列表 (比如 eth/*=6,p2p=5)
--backtrace value    请求特定日志记录堆栈跟踪 (比如 “block.go:271”)
--debug                     突出显示调用位置日志(文件名及行号)
--pprof                     启用pprof HTTP服务器
--pprofaddr value           pprof HTTP服务器监听接口(默认值:127.0.0.1)
--pprofport value           pprof HTTP服务器监听端口(默认值:6060)
--memprofilerate value      按指定频率打开memory profiling    (默认:524288)
--blockprofilerate value    按指定频率打开block profiling    (默认值:0)
--cpuprofile value          将CPU profile写入指定文件
--trace value               将execution trace写入指定文件
WHISPER实验选项:
--shh                        启用Whisper
--shh.maxmessagesize value   可接受的最大的消息大小 (默认值: 1048576)
--shh.pow value              可接受的最小的POW (默认值: 0.2)
弃用选项：
--fast     开启快速同步
--light    启用轻客户端模式
其他选项:
–help, -h    显示帮助

目录
1：环境构建
2：Fabric源码及镜像文件处理
3：运行测试e2e
4：创建Fabric多节点集群
5：启动Fabric多节点集群
6：Fabric多节点集群生产部署
7：Fabric多节点集群生产启动
8：智能合约
9：CouchDB
10：CA
11：fabric-sdk-java应用
12：orderer分布式方案
13：Hyperledger Fabric问题小节


# FAQ 列表

https://github.com/ACINQ/eclair-mobile/wiki/FAQ

https://explorer.acinq.co/faq

https://medium.com/@rusty_lightning/bitcoin-lightning-things-to-know-e5ea8d84369f

https://medium.com/@The1Brand7/lightning-faq-67bd2b957d70

https://counterparty.io/docs/paymentchannels-lightning-faq/

https://www.reddit.com/r/Bitcoin/comments/7pwna9/lightning_network_megathread/

https://docs.btcpayserver.org/faq-and-common-issues/faq-lightningnetwork

https://bluewallet.io/lightning/

https://bitcointalk.org/index.php?topic=4792622.msg43243696#msg43243696

 
# 节点无法连接内网节点, 建立通道

  1. 内网节点主动连接公网节点，然后公网节点就可以向内网节点建立通道

  2. 配置NAT

     lnd 支持自动nat，会检测路由器是否支持upnp和nat-pmp, 但是不支持多级nat，就是如果节点在多个路由器后面，那就无法支持自动nat

  3. 反向代理
     frp
     ssh
     nginx
     ngork

# 没有建立通道的节点

  lncli getnodeinfo pubkey

    rpc error: code = Unknown desc = unable find to node

# node 在 1ml 搜索不到

  node 必须有通道

## lnd.conf pending channel num

  default is 5

### lnd 显示 "unable to find a path to destination"

 1. 容量不够

 2. no path

## 2个节点能不能创建多个通道

 只有lnd的节点之间可以 

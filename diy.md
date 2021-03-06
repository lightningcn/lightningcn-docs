# DIY闪电网络节点

市面上的闪电网络盒子都在1000人民币以上，而且几乎都是国外厂商，购买不方便, 见[闪电网络盒子列表](https://docs.lightningcn.com/hardware)

这些产品很多都是树莓派加个盒子, 所以其实这个很容易可以自己组装

由于闪电网络可以支持轻节点,  所以只需要保持部分最新的区块数据就可以运行闪电网络节点,
并不需要一个大硬盘, 当然有条件还是加个硬盘，运行全节点更安全, 更去中心化

## 300元左右带液晶屏的闪电节点

名称       |     价格 (¥)  |  地址
------     |   ------ | ---------
树梅派 3   |       200      |
盒子+液晶屏   |      64      | https://item.taobao.com/item.htm?spm=a1z09.2.0.0.24372e8duH2VOA&id=574620008311&_u=8b4sbm9cb0
32G tf卡   |      30      | https://item.jd.com/6577597.html

如果要长期稳定运行, 最好加个散热片

# 软件方案


## 方案一  开机即用的image

链接: https://pan.baidu.com/s/1t5OfgW7rF3qA3StIqAqRgg 提取码: ww6m 

这个image里bitcoin运行在轻节点模式，内置了到2019年3月10日共计5G左右数据，开机连接会自动同步，可以通过液晶屏或者连接RTL web界面http://ip:3000 查看节点

web的默认密码为lightningcn

ssh admin@ip 密码为123

### 查看 logs

    cd /data

- 查看 bitcoind logs

    docker-compose logs --tail 10 bitcoind

    or

    tail bitcoin_data/debug.log

- 查看 lnd logs

    docker-compose logs --tail 10 lnd_bitcoin

- 查看 rtl logs

    docker-compose logs --tail 10 rtl

## 方案二 一键搭建闪电网络节点
  
  https://github.com/lightningcn/ln-node

## raspiblitz向导方式安装

  https://github.com/lightningcn/raspiblitz

  https://github.com/lightningcn/guides/blob/lightningcn/zh_CN/raspibolt/readme.md

  https://github.com/rootzoll/raspiblitz/blob/master/shoppinglist_cn.md

  视频 https://youtu.be/77BBQWg1n8w


#  更低硬件需求的方案

## 200元左右的闪电网络节点

raspberry zero w 100左右

可以运行:

spruned + clightning + flume 

见 https://github.com/lightningcn/ln-node#%E6%A0%91%E8%8E%93%E6%B4%BEzerow-%E5%AE%89%E8%A3%85-spruned--clightning--fulmo-%E9%97%AA%E7%94%B5%E7%BD%91%E7%BB%9C%E6%9C%8D%E5%8A%A1%E5%99%A8

## 100元左右的闪电网络节点

荔枝派 zero 50元 + sd卡, 性能比树莓派zero还好一些

spruned + clightning + flume 

见 https://github.com/lightningcn/ln-node#%E6%A0%91%E8%8E%93%E6%B4%BEzerow-%E5%AE%89%E8%A3%85-spruned--clightning--fulmo-%E9%97%AA%E7%94%B5%E7%BD%91%E7%BB%9C%E6%9C%8D%E5%8A%A1%E5%99%A8

## 路由器集成

todo

## 其他选择

其他各种派，单板计算机

https://en.wikipedia.org/wiki/Comparison_of_single-board_computers

https://dietpi.com/#download

https://docs.google.com/spreadsheets/d/e/2PACX-1vSUjUlcC1I84weciiE15YePzPiTNwHLgf9VVGygZBxgB6PAjjjKTJxILCqVrbARSTGNdBhKp1upx40t/pubhtml

 https://github.com/cryptoadvance/specter-diy

 https://github.com/btcpayserver

 https://github.com/mynodebtc/mynode

 https://blog.bitcoinprivacy.net/2019/06/18/the-worlds-cheapest-full-node-is-now-a-lightning-network-hub-and-still-pretty-cheap/

 https://blog.bitcoinprivacy.net/2019/12/20/news-from-the-cheapnode-project/


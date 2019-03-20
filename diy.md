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
16G tf卡   |      30      | https://item.jd.com/1875996.html

如果要长期稳定运行, 最好加个散热片

# 软件方案


## 方案一  开机即用的image

链接: https://pan.baidu.com/s/1t5OfgW7rF3qA3StIqAqRgg 提取码: ww6m 

这个image里bitcoin运行在轻节点模式，内置了到2019年3月10日共计5G左右数据，开机连接会自动同步，可以通过液晶屏或者连接RTL web界面http://ip:3000 查看节点

## 方案二 一键搭建闪电网络节点
  
  https://github.com/lightningcn/ln-node

## raspiblitz向导方式安装

  https://github.com/rootzoll/raspiblitz
  https://github.com/rootzoll/raspiblitz/blob/master/shoppinglist_cn.md


#  更低硬件需求的方案

## 200元左右的闪电网络节点

raspberry zero w 100左右

可以运行

spruned + clightning + flume 

## 100元左右的闪电网络节点

荔枝派 zero 50元 + sd卡, 性能比树莓派zero还好一些

spruned + clightning + flume 

## 路由器集成

todo

## 其他硬件选择

其他各种派，单板计算机

https://en.wikipedia.org/wiki/Comparison_of_single-board_computers

# 其他节点方案

## https://github.com/alevchuk/minibank
minibank这个闪电网络节点项目，用2个树莓派zerow,2个256g卡iscsi， 跑了全节点+lnd+ prometheus+ grafana

## https://github.com/lncm/pi-factory



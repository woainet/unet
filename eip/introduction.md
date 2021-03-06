# 外网弹性IP

## 产品简介

UCloud外网弹性IP（EIP）是互联网标准静态IP地址。将外网弹性IP与云主机UHost、负载均衡ULB、NAT网关等服务绑定，可以为这些服务提供接入外网访问的能力。

## 计费方式简介

在UCloud云平台中，用户可以为账户中的每个EIP选择不同的带宽使用模式。目前，云平台中的所有地域均能够提供 **标准带宽**、
**流量计费** 、**共享带宽**和**带宽后付费** 等计费方式。

在各种不同的带宽模式下，弹性IP也分别具有不同的属性。

### 标准带宽

![image](/images/eip1.png)

带宽计费 购买弹性IP时，同时购买“出口”带宽上限。该计费方式不会记录流量所产生费用。

**注意:**

  - 当所购买出口带宽小于50Mbps时，入口带宽等于50Mbps。当所购买出口带宽大于等于50Mbps时，入口带宽等于出口带宽。
  - 香港回内地带宽采用专用线路，产品策略如下：


  1、 如果购买带宽值小于等于2Mbps，则回内地的带宽上限为购买值。
  
  2、 如果购买带宽值大于2Mbps，且小于等于20Mbps，则回内地带宽上限为2Mbps。
  
  3、 如果购买带宽值大于20Mbps，那么回内地带宽限制为购买值的1/10。


### 流量计费

![image](/images/eip3.png)

购买弹性IP时，可选择设置“出口”带宽上限，按照不同地域的单价，根据IP产生“出流量”进行扣费。该计费方式不会记录带宽所产生的费用。

**注意:**

  - 流量统计会在每天零点进行结算。弹性IP的详细计费规则参见FAQ
  - 香港回内地带宽采用专用线路，产品策略如下：
  
  
  1、如果该流量计费EIP带宽值小于等于2Mbps，则回内地的带宽上限为购买值。
  
  2、如果该流量计费EIP带宽值大于2Mbps，且小于等于20Mbps，则回内地带宽上限为2Mbps。
  
  3、如果该流量计费EIP带宽值大于20Mbps，那么回内地带宽限制为购买值的1/10。


### 共享带宽

共享带宽模式参见共享带宽[帮助文档](/network/unet/share_bandwidth/introduction)。

![image](/images/eip2.png)

**注意:**

  - 香港回内地带宽采用专用线路，产品策略如下：


  1、 如果EIP分配到的带宽份额小于等于2Mbps，则回内地的带宽上限为EIP分配到的份额。
  
  2、 如果EIP分配到的带宽份额大于2Mbps，且小于等于20Mbps，则回内地带宽上限为2Mbps。
  
  3、 如果EIP分配到的带宽份额大于20Mbps，那么回内地带宽限制为该EIP带宽份额的1/10。


关于香港回内地带宽的具体监控，可以在香港的EIP界面看到。可以据此进行判断，您的香港回内地带宽是否超过限制。

**注意:**

香港回内地带宽的监控信息由于采样方式和标准带宽计算有所不同，可能会有一定的偏差。此外香港回内地的带宽限制，由于算法问题，可能会短时超过限制值。

### 带宽后付费

![image](/images/accurateeip.png)

需选择保底带宽值并支付相应费用，保底带宽费用与普通带宽一致[价格列表](/network/unet/eip_price/accuratebandwidth)。EIP的实际带宽限制为峰值带宽，峰值带宽:保底带宽比例关系为5:1，超过保底带宽的用量会在次日零点进行费用结算。根据当日使用情况，每五分钟取一个点，如果该点低于保底带宽，则不计入结算;若平均带宽高于保底带宽，则减去保底带宽，对超过部分进行结算。最终结算的费用为当天所有的结算点的平均值。参见下图：
![image](/images/eippostpaid.png)
阴影部分点的平均值，即为当天需结算的后付费带宽值。

**注意:**

1、 带宽后付费调整带宽时，调整的为保底带宽值，保底带宽值调整后，对应的峰值带宽会自动调整。

2、 EIP的监控数据-带宽使用率，按照峰值带宽计算。

3、 保底带宽的可选范围为5-200Mbps。



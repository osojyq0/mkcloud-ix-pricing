# 上云互联专线购买：Mkcloud 四条IX线路价格套餐全整理，先搞懂前置机再下单不吃亏

搜“上云互联专线购买”的人，基本分两类：一类是做跨境电商或 TikTok 直播的，想给业务弄条稳定低延迟的出海线路；另一类是被各种“IXP 上云”科普文章种草后，发现这东西比 IEPL 便宜不少，但始终没搞明白为什么便宜、要满足什么条件才能买。

这篇文章把两个问题一起解决。以 Mkcloud（mkcloud.net）为例——这家从 2023 年 4 月开始做跨境专线，目前官网上云互联优化入口（IXP）覆盖深圳-香港、上海-日本、上海-香港、上海-美国四条线路，流量计费套餐 ¥158/月起——把购买前的门槛、全部套餐现价、优惠现状和下单流程一次讲清。文中所有价格均为 2026 年 9 月从官网商店页逐条核对后的现售价，过期活动码会明确标注，不让你拿着失效折扣白高兴一场。

## 先弄清楚：上云互联专线到底是个什么东西

传统跨境专线（IEPL/IPLC）有一个公网入口 IP，你从家里或办公室直接连上去。上云互联（IXP）专线不是这样：它的入口 IP 只在云厂商交换中心内宣告，换句话说，**只有阿里云、腾讯云这类大厂云内网的机器能连上入口**，三大运营商的网络根本摸不到门。

这个设计带来两件事。好处是入口不走公网，线路被攻击、被通报的风险低很多，NodeSeek 社区对这类产品的普遍评价是“抗通报能力比公网入口专线强”；坏处也很直接——你得自己准备一台云厂机器当前置，前置机的钱和折腾都算你的。NodeSeek 上一篇讨论把这件事说得很直白：IX 上云互联省下的成本，其实是以“转嫁给用户”的方式实现的。

所以购买决策的第一步不是看套餐，而是确认你有没有前置条件。

## 购买前必须确认的三件事

### 前置机：你有没有一台能用的云厂机器

这是硬门槛，不满足就不用往下看价格表了。四条线路对前置云机的要求不完全一样，直接看官网购物车页面的说明：

| 线路 | 出口 | 端内延迟 | 支持的前置云厂 |
| --- | --- | --- | --- |
| 深港 IX | 香港 BGP | 1~2ms | 阿里云国内全网（页面标注暂时不通）、腾讯云国内全网、百度云国内全网、火山云华南、华为云华南 |
| 沪日 IX | 日本 BGP | 25~28ms | 阿里云、腾讯云、百度云国内全网，火山云华东、华为云华东、UCloud 华东 |
| 沪港 IX | 香港 BGP | 21ms | 阿里云、腾讯云、百度云国内全网，火山云华东、华为云华东、UCloud 华东 |
| 沪美 IX | 美国 BGP | 124~134ms | 阿里云、腾讯云、百度云国内全网，火山云华东、华为云华东、UCloud 华东 |

两个细节值得注意。第一，深港线路的购物车提示里阿里云标注“暂时不通”，如果你的前置是阿里云，选深港之前先确认这条备注是否更新。第二，前置机到入口的物理距离影响很大：第三方实测里，用腾讯云上海机器连沪港入口延迟约 26ms，而用广东的云机连深港入口可以压到 5ms 以内。前置机放在哪座城市，比你想的重要。

### 实名与用途限制：合规是这家店的底线

Mkcloud 购物车页面有一段加粗提醒，内容不复杂但每条都会实际执行：

> 所有产品均为云服务器/独立服务器，需中国身份信息实名。仅限个人或企业正规用途，禁止机场、回国等违法违规用途，一经发现立刻清退不退款。

付款方式目前只支持支付宝。开通后不支持换地域，退款只认“质量问题”，而且要你拿出具体证据——准确的延迟数据、速度数据。这不是商家客套话，官网常见问题里写明了退款举证要求，下单前把这条读进去。

另外还有一个容易忽略的点：普通入口的专线有省级白名单限制，只允许选定省份的 IP 连入。IXP 线路没有这个限制，因为你用的是自己云机的前置 IP——这也是很多用户选 IXP 而不是普通专线的真实原因之一，VPS 测评站 vpsxb.net 在实测小结里也专门提到了这一点。

### 流量双向计费，超量停机

上云互联的流量计费套餐按上行、下行双向统计。用 2TB 档举例：你上传 1TB、下载 1TB，这个月额度就用完了。超量后机器直接暂停，不是降速。补救方式有两种：自助购买流量重置，或提交工单补差价升级套餐。升降级都要走工单，且降级到低价套餐时差价不退——买大套餐前想清楚，钱不退是真的不退。

## Mkcloud 上云互联专线怎么选线路

四条线路出口不同、延迟不同，价格差距也不小。选线逻辑其实就一句话：业务在哪个市场，就选哪个出口，再看延迟和价格要不要为它买单。

- **深港 IX（香港出口）**：端内 1~2ms，全站延迟最低，适合对操作流畅度敏感的跨境电商后台、直播间推流。前置需要华南区域的云厂机器（阿里云暂时不通，注意核对）。
- **沪港 IX（香港出口）**：端内 21ms，价格比深港便宜——2TB 档深港卖 ¥158，沪港直接给到 500M 峰值带宽只卖 ¥198。上海及周边的前置机选这条，单 TB 成本反而更低。
- **沪日 IX（日本出口）**：端内 25~28ms，做日本市场（日本电商、游戏、对日 SaaS）的对应选择。
- **沪美 IX（美国出口）**：端内 124~134ms，物理距离摆在那里，适合美国独立站、美区电商后台这类不追求低延迟的场景。

一句话概括：香港出口是通用性最强的默认答案，沪港性价比比深港更激进；深港买的是 1~2ms 的极致延迟；日本、美国按市场选。

## 全套餐价格表（2026 年 9 月官网现价）

以下数据逐条来自 Mkcloud 官网商店页当前展示，包含四条线路全部流量计费档位和深港独享带宽档位。所有套餐均含 1 个独立入口 IP + 1 个独立出口 IP，支持 Ubuntu/Debian/CentOS/Rocky/AlmaLinux 等主流系统。

**深港上云互联优化专线（流量计费，香港 BGP，端内 1~2ms）**

| 流量/月 | 峰值带宽 | CPU/内存/硬盘 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 2TB | 1Gbps | 2核/4GB/40GB | ¥158 | [ 购买深港IX 2TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 4TB | 1Gbps | 2核/4GB/40GB | ¥258 | [ 购买深港IX 4TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 6TB | 2Gbps | 4核/8GB/40GB | ¥378 | [ 购买深港IX 6TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 10TB | 2Gbps | 4核/8GB/40GB | ¥826 | [ 购买深港IX 10TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 20TB | 2Gbps | 4核/8GB/40GB | ¥1639 | [ 购买深港IX 20TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 30TB | 3Gbps | 4核/8GB/60GB | ¥2458 | [ 购买深港IX 30TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 50TB | 3Gbps | 8核/8GB/60GB | ¥3588 | [ 购买深港IX 50TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 100TB | 5Gbps | 8核/16GB/80GB | ¥7168 | [ 购买深港IX 100TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 200TB | 5Gbps | 8核/16GB/80GB | ¥12288 | [ 购买深港IX 200TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |
| 300TB | 5Gbps | 8核/16GB/80GB | ¥18428 | [ 购买深港IX 300TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-sh) |

**沪港上云互联优化专线（流量计费，香港 BGP，端内 21ms）**

| 流量/月 | 峰值带宽 | CPU/内存/硬盘 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 2TB | 500Mbps | 2核/4GB/40GB | ¥198 | [ 购买沪港IX 2TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-sh-hk-sh) |
| 3TB | 500Mbps | 2核/4GB/40GB | ¥288 | [ 购买沪港IX 3TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-sh-hk-sh) |
| 6TB | 1Gbps | 4核/8GB/40GB | ¥398 | [ 购买沪港IX 6TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-sh-hk-sh) |
| 10TB | 1Gbps | 4核/8GB/40GB | ¥666 | [ 购买沪港IX 10TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-sh-hk-sh) |
| 20TB | 1Gbps | 4核/8GB/40GB | ¥1290 | [ 购买沪港IX 20TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-sh-hk-sh) |
| 30TB | 2Gbps | 4核/8GB/60GB | ¥1900 | [ 购买沪港IX 30TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-sh-hk-sh) |
| 50TB | 2Gbps | 8核/8GB/60GB | ¥3120 | [ 购买沪港IX 50TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-sh-hk-sh) |

**沪日上云互联优化专线（流量计费，日本 BGP，端内 25~28ms）**

| 流量/月 | 峰值带宽 | CPU/内存/硬盘 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 1TB | 200Mbps | 2核/4GB/40GB | ¥166 | [ 购买沪日IX 1TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 2TB | 300Mbps | 2核/4GB/40GB | ¥268 | [ 购买沪日IX 2TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 3TB | 500Mbps | 2核/4GB/40GB | ¥358 | [ 购买沪日IX 3TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 6TB | 1Gbps | 4核/8GB/40GB | ¥688 | [ 购买沪日IX 6TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 10TB | 1Gbps | 4核/8GB/40GB | ¥1125 | [ 购买沪日IX 10TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 20TB | 1Gbps | 4核/8GB/40GB | ¥2150 | [ 购买沪日IX 20TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 30TB | 2Gbps | 4核/8GB/60GB | ¥3165 | [ 购买沪日IX 30TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |
| 50TB | 2Gbps | 8核/8GB/60GB | ¥5222 | [ 购买沪日IX 50TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-jp-sh) |

**沪美上云互联优化专线（流量计费，美国 BGP，端内 124~134ms）**

| 流量/月 | 峰值带宽 | CPU/内存/硬盘 | 月付价格 | 购买链接 |
| --- | --- | --- | --- | --- |
| 1TB | 200Mbps | 2核/4GB/40GB | ¥266 | [ 购买沪美IX 1TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |
| 2TB | 200Mbps | 2核/4GB/40GB | ¥430 | [ 购买沪美IX 2TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |
| 3TB | 500Mbps | 2核/4GB/40GB | ¥615 | [ 购买沪美IX 3TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |
| 6TB | 500Mbps | 4核/8GB/40GB | ¥1166 | [ 购买沪美IX 6TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |
| 10TB | 1Gbps | 4核/8GB/40GB | ¥1945 | [ 购买沪美IX 10TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |
| 20TB | 1Gbps | 4核/8GB/40GB | ¥3686 | [ 购买沪美IX 20TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |
| 30TB | 2Gbps | 4核/8GB/60GB | ¥5529 | [ 购买沪美IX 30TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |
| 50TB | 2Gbps | 8核/8GB/60GB | ¥9216 | [ 购买沪美IX 50TB套餐](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-us-sh) |

**深港上云互联优化专线（带宽计费/独享带宽，流量不限，香港 BGP，端内 1~2ms）**

| 独享带宽 | CPU/内存/硬盘 | 月付价格 | 购买链接 |
| --- | --- | --- | --- |
| 100M 独享 | 2核/4GB/40GB | ¥1600 | [ 购买深港IX 100M独享](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 200M 独享 | 2核/4GB/40GB | ¥3000 | [ 购买深港IX 200M独享](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 500M 独享 | 8核/8GB/60GB | ¥6000 | [ 购买深港IX 500M独享](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 1G 独享（赠独立服务器） | 28核/64GB/512GB | ¥9000 | [ 购买深港IX 1G独享](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 2G 独享（赠独立服务器） | 28核/64GB/512GB | ¥16000 | [ 购买深港IX 2G独享](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 5G 独享（赠独立服务器） | 28核/64GB/512GB | ¥35000 | [ 购买深港IX 5G独享](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |
| 定制配置 | 按需定制 | 询价 | [ 咨询深港IX定制方案](https://www.mkcloud.net/aff.php?aff=390&url=https://www.mkcloud.net/index.php/store/cloud-hk-ex) |

看表时留意两个性价比拐点。流量计费档位里，深港 4TB（¥258）比 2TB（¥158）多 100 块翻倍流量，如果月用量会超过 2TB，直接买 4TB 比超量后买流量重置划算。带宽计费的独享线路是给另一类人的：流量无限但按带宽收费，100M 起步 ¥1600，适合持续跑大流量的业务，偶尔用用的话流量计费永远是更便宜的那边。

## 优惠现状：哪些能用，哪些已经失效

目前官方动态页展示的全场优惠是：**流量计费产品 8.8 折循环，优惠码 MK-8.8**。循环折扣意味着月付订单每月续费都按折后价扣，不是只首月便宜。以深港 2TB 档为例，折后约 ¥139/月。独享带宽产品在近期活动中出现过首月 7.8 折（MK-7.8）的口径，结账时以购物车页面显示为准——官网也提示“准确优惠券信息请登录后查看”。

需要泼冷水的是那些在旧文章里流传的折扣码。核对官网公告状态后，下面这些**全部已失效**，看到就直接划走：

- CLOUD-2T-NEW（上云 2TB 档循环 8 折，新春活动，已结束）
- IXCLOUD（上云互联预售 6.9 折，预售期专用，已结束）
- ALIYUN-NEW（深港 IX 上新折扣，已结束）
- MK-NEW / US-6.9 / MK-8.9 等节日活动码（对应活动均已结束，双旦活动页明确标注“优惠码仅在活动期内有效”）

Mkcloud 的活动页写得算厚道，每篇都标注活动状态，但二手转发经常把“已结束”三个字删掉。认准一点：结账页优惠码框不接受，就是没了。

另外它家有 10% 的 AFF 邀请返佣：通过推广链接注册的新用户完成首单，邀请人拿 10% 一次性奖励。反过来说，如果你从别人的推广链接进入购买，付出的价格和官网直购是一样的，等于商家让利给推荐人，对你没有成本差。

## 购买流程：从下单到能用的六步

整个过程官网标注约 1 分钟自动开通，实际时间主要花在第三步：

1. **确认前置机已就绪**：一台在支持列表内的云厂机器（阿里云/腾讯云/百度云/火山云/华为云/UCloud，按线路对应区域），记下它的公网 IP。
2. **进入对应线路的产品页**：上表任一购买链接直达。
3. **逐层选择**：地区 → 网络（上云互联优化入口 IXP）→ 类型（流量计费/带宽计费）→ 套餐 → 系统（Ubuntu、Debian、CentOS、Rocky、AlmaLinux、Fedora 等都有）。
4. **勾选同意条款并输入优惠码**：当前可试 MK-8.8，以页面提示为准；付款方式支付宝。
5. **等待自动开通**：拿到两个 IP——一个入口 IP、一个出口 IP，都独立独享。
6. **从前置机连入入口 IP 使用**：部署你的业务环境后，所有出境流量走专线出口。记得核对入口 IP 是否只从你的前置机可访问，这是 IXP 线路的正常表现，不是故障。

## 第三方实测数据参考

自己动手测过的人怎么说，比宣传页可信。vpsxb.net 在 2026 年 2 月对深港 IX 2TB 档做过一轮实测，几个关键数字：机器为 AMD EPYC 平台，磁盘 IO 平均 366MB/s；用腾讯云上海机器做前置，到入口延迟约 26ms，iperf3 稳定跑在 210~230Mbps（受限于前置机 200Mbps 带宽，线路本身给到 1G 峰值）；换 500M 带宽测出口，香港节点跑到 499/377Mbps。出口 IP 在流媒体检测里 Netflix、Disney+、TikTok、ChatGPT（APP）均为原生解锁，TikTok 归属新加坡区域。

虎窝博客对沪港 IXP 线路的补充说明也值得一提：这类产品入口成本低，所以售价比同方向的传统 IPLC 便宜一截，优势是“入口成本比较低，售价也会便宜不少”。两家第三方结论方向一致：线路质量没有虚标，低价来自入口结构的差异，而不是缩水。

当然，共享带宽是峰值不保证持续跑满，晚高峰的波动任何商家都一样存在，这是选流量计费方案时应该有的预期。

## 几个购买前常被问到的问题

**没有云厂机器，能不能买？** 不能。入口只对云厂内网开放，三大运营商网络无法直连。要么先买一台云机（各大厂轻量云几十块一个月的就有），要么改选 Mkcloud 的普通 IPLC/IEPL 线路。

**前置机有流量限制怎么办？** 前置机的流量消耗取决于你的业务怎么部署。vpsxb 实测用的是腾讯云“不限流量@200Mbps”机型，如果你的前置机按流量计费，把它算进总成本再比较方案——这也是社区里有人能把 IXP 合租成本压到每 TB 很低的思路，但自用场景别为了省前置机钱选太小带宽的云机，它会成为整条链路的瓶颈。

**超量停机后数据丢不丢？** 官网说明是超量后暂停，可自助购买流量重置恢复，或提交工单补差价升级，机器数据保留。流量重置不影响原重置日期，到期仍正常重置。

**支持退订吗？** 仅支持质量问题退款，且要提供具体延迟、速度数据举证；服务开通后不支持更换地域。下单前按“这笔钱可能拿不回来”的心态做决定。

**月付还是年付划算？** 商店页支持月付到三年付多种周期。IXP 流量计费套餐单价已经压得比较低，年付折扣以购物车实际显示为准；拿不准的话先月付一个月跑准流量基线，再决定要不要锁定长周期，比凭感觉年付稳。

## 最后的选择建议

把决策压缩成三句话：先确认你有云厂前置机，没有就没有然后；月流量 2TB 以内、要极致低延迟选深港 2TB（¥158，折后更低），上海周边的前置机可以直接对比沪港 2TB（¥198 但带宽给到 500M）；做日本或美国市场就按出口选沪日和沪美，别为了便宜买错方向。

如果看完还是不确定流量档位，从小的买起——套餐升降级走工单就行，超量也有重置兜底，唯一不可逆的是退款政策。先月付验证一个月，再决定长期方案，这是上云互联专线这种按量计费产品最不容易后悔的买法。

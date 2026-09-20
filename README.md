# 搬瓦工下单教程：从选套餐到支付宝付款的完整流程，新手也能一次买对 BandwagonHost VPS

搬瓦工（BandwagonHost）算是在售时间很长的老牌 VPS 商家了，但它的购买流程对新手一直不太友好：官网是英文的，注册和下单绑在一起分不清先后，付款方式里哪个适合国内用户也没人明说。这篇文章按真实的下单顺序走一遍，从怎么挑套餐、填什么信息，到支付宝扫码付款、进入 KiwiVM 后台拿到 IP，一次说清楚。

## 下单之前，先想清楚三件事

搬瓦工的套餐按线路分成好几个系列，价格差距很大，直接跳过这一步去下单，大概率会买错。

**第一，看你的用户在哪。**如果你的服务主要给国内用户访问，普通国际线路的套餐晚高峰会比较拥堵，这个钱不建议省；如果只是学习 Linux、跑脚本、做纯海外业务，便宜的常规款反而更合适。

**第二，看预算档位。**搬瓦工目前在售的常规套餐大致分四档：

- **入门档：KVM 常规套餐**，年付 49.99 美元起，走普通线路，部分机房（比如 DC2、DC8）对电信有一定优化，购买后可在约 9 个机房之间切换。
- **主力档：CN2 GIA-E（CN2 GIA E-COMMERCE）**，季付 49.99 美元起，三网双向 CN2 GIA 优化，可选机房多达 15 个左右，是目前多数国内用户的首选系列。
- **企业档：SLA PLAN**，季付 65.89 美元起，主打 99.99% 在线率保障和每两周免费更换一次 IP，机房固定在洛杉矶 DC5，适合掉线就亏钱的跨境业务。
- **高端档：香港 / 东京 / 大阪 / 新加坡 CN2 GIA**，月付 49.99 美元到 89.99 美元起，延迟低但流量少、价格贵，其中大阪和新加坡的起步价比香港、东京便宜不少。

**第三，确认自己能不能付款。**搬瓦工支持支付宝、银联、PayPal 和国际信用卡，国内用户基本不存在付款障碍，这点不用担心。

## 全系列套餐与最新价格

下面这张表整理了搬瓦工官网当前展示的各系列套餐，配置和价格信息参考了 2026 年仍在对官网套餐做同步维护的第三方汇总（其数据更新至 2026 年 5 月底），实际以结账页显示为准。每个套餐的购买链接都指向对应的下单页面。

### KVM 常规套餐（入门与海外业务）

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核 | 1GB | 20GB SSD | 1TB | 1Gbps | $49.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=44) |
| 3核 | 2GB | 40GB SSD | 2TB | 1Gbps | $52.99/半年 或 $99.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=45) |
| 4核 | 4GB | 80GB SSD | 3TB | 1Gbps | $19.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=46) |
| 5核 | 8GB | 160GB SSD | 4TB | 1Gbps | $39.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=47) |
| 6核 | 16GB | 320GB SSD | 5TB | 1Gbps | $79.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=48) |
| 7核 | 24GB | 480GB SSD | 6TB | 1Gbps | $119.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=49) |

### CN2 GIA-E 套餐（国内用户主力选择）

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核 | 1GB | 20GB SSD | 1TB | 2.5Gbps | $49.99/季 或 $169.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=87) |
| 3核 | 2GB | 40GB SSD | 2TB | 2.5Gbps | $89.99/季 或 $299.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=88) |
| 4核 | 4GB | 80GB SSD | 3TB | 2.5Gbps | $56.99/月 或 $549.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=89) |
| 6核 | 8GB | 160GB SSD | 5TB | 5Gbps | $86.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=90) |
| 8核 | 16GB | 320GB SSD | 8TB | 5Gbps | $159.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=91) |
| 10核 | 32GB | 640GB SSD | 10TB | 10Gbps | $289.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=92) |
| 12核 | 64GB | 1280GB SSD | 12TB | 10Gbps | $549.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=93) |

### SLA PLAN 套餐（企业电商，99.99% 在线率保障）

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核独享 | 1GB | 20GB NVMe | 1TB | 2.5Gbps | $65.89/季 或 $239.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=164) |
| 3核独享 | 2GB | 40GB NVMe | 2TB | 2.5Gbps | $116.99/季 或 $399.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=165) |
| 4核独享 | 4GB | 80GB NVMe | 3TB | 2.5Gbps | $69.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=166) |
| 6核独享 | 8GB | 160GB NVMe | 5TB | 5Gbps | $109.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=167) |
| 8核独享 | 16GB | 320GB NVMe | 8TB | 5Gbps | $199.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=168) |
| 10核独享 | 32GB | 640GB NVMe | 10TB | 10Gbps | $369.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=169) |
| 12核独享 | 64GB | 1280GB NVMe | 12TB | 10Gbps | $699.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=170) |
| 12核独享 | 64GB | 1280GB NVMe | 15TB | 10Gbps | $879.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=171) |
| 12核独享 | 64GB | 1280GB NVMe | 20TB | 10Gbps | $1159.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=172) |

### 新加坡 CN2 GIA 套餐

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核 | 2GB | 40GB SSD | 0.5TB | 1.5Gbps | $49.99/月 或 $499.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=173) |
| 4核 | 4GB | 80GB SSD | 1TB | 1.5Gbps | $86.99/月 或 $869.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=174) |
| 6核 | 8GB | 160GB SSD | 2TB | 2.5Gbps | $165.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=175) |
| 8核 | 16GB | 320GB SSD | 4TB | 2.5Gbps | $329.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=176) |
| 10核 | 32GB | 640GB SSD | 6TB | 5Gbps | $549.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=177) |
| 12核 | 64GB | 1280GB SSD | 8TB | 5Gbps | $1059.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=178) |

### 日本大阪 CN2 GIA 套餐（JPOS_6，亚太高端平替）

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核 | 2GB | 40GB SSD | 0.5TB | 1.5Gbps | $49.99/月 或 $499.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=134) |
| 4核 | 4GB | 80GB SSD | 1TB | 1.5Gbps | $86.99/月 或 $869.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=135) |
| 6核 | 8GB | 160GB SSD | 2TB | 1.5Gbps | $165.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=136) |
| 8核 | 16GB | 320GB SSD | 4TB | 1.5Gbps | $329.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=137) |
| 10核 | 32GB | 640GB SSD | 6TB | 1.5Gbps | $549.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=138) |
| 12核 | 64GB | 1280GB SSD | 8TB | 1.5Gbps | $1059.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=139) |

### 日本东京 CN2 GIA 套餐（JPTYO_8）

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核 | 2GB | 40GB SSD | 0.5TB | 1.2Gbps | $89.99/月 或 $899.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=108) |
| 4核 | 4GB | 80GB SSD | 1TB | 1.2Gbps | $155.99/月 或 $1559.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=109) |
| 6核 | 8GB | 160GB SSD | 2TB | 1.2Gbps | $299.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=110) |
| 8核 | 16GB | 320GB SSD | 4TB | 1.2Gbps | $589.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=111) |
| 10核 | 32GB | 640GB SSD | 6TB | 1.2Gbps | $989.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=123) |
| 12核 | 64GB | 1280GB SSD | 8TB | 1.2Gbps | $1889.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=125) |

### 香港 CN2 GIA 套餐（延迟最低）

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核 | 2GB | 40GB SSD | 0.5TB | 1Gbps | $89.99/月 或 $899.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=95) |
| 4核 | 4GB | 80GB SSD | 1TB | 1Gbps | $155.99/月 或 $1559.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=96) |
| 6核 | 8GB | 160GB SSD | 2TB | 1Gbps | $299.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=97) |
| 8核 | 16GB | 320GB SSD | 4TB | 1Gbps | $589.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=98) |
| 10核 | 32GB | 640GB SSD | 6TB | 1Gbps | $989.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=122) |
| 12核 | 64GB | 1280GB SSD | 8TB | 1Gbps | $1889.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=124) |

### 阿联酋迪拜套餐（中东区域业务）

| 配置 | 内存 | 硬盘 | 流量/月 | 带宽 | 价格 | 购买链接 |
| --- | --- | --- | --- | --- | --- | --- |
| 2核 | 1GB | 20GB SSD | 0.5TB | 1Gbps | $19.99/月 或 $169.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=114) |
| 3核 | 2GB | 40GB SSD | 1TB | 1Gbps | $32.99/月 或 $299.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=115) |
| 4核 | 4GB | 80GB SSD | 2TB | 1Gbps | $56.99/月 或 $549.99/年 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=116) |
| 6核 | 8GB | 160GB SSD | 3TB | 1Gbps | $86.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=117) |
| 8核 | 16GB | 320GB SSD | 4TB | 1Gbps | $159.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=118) |
| 10核 | 32GB | 640GB SSD | 5TB | 1Gbps | $289.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=119) |
| 12核 | 64GB | 1280GB SSD | 6TB | 1Gbps | $549.99/月 | [ 前往下单](https://bandwagonhost.com/aff.php?aff=79616&pid=120) |

如果只是想快速拿主意：预算紧、纯练手选 KVM 年付；要给国内用户用，CN2 GIA-E 季付起步款是最常见的答案；做跨境电商、怕封 IP 的，再看 SLA 系列。除了这些常规款，搬瓦工偶尔还会放出 THE PLAN 之类的限量套餐，性价比很高但基本靠抢，看到补货就不用犹豫太久。

## 搬瓦工下单教程：从选套餐到付款的完整步骤

### 第一步：选套餐，加入购物车

从上面表格里点进对应套餐的下单页，确认配置和价格后点 **Add to Cart** 进入购物车页面。注意搬瓦工同一款套餐经常只显示一种计费周期的按钮，比如年付款和季付款是分开的两个入口，下单前看清楚价格旁边的周期标注。

### 第二步：选计费周期，填优惠码

购物车页面有两件事要做。一是确认计费周期（Billing Cycle），同样是 CN2 GIA-E，年付 169.99 美元比季付 49.99 美元乘四要划算，长期用建议直接年付。

二是在 **Promotional Code** 输入框里填优惠码，点 **Validate Code** 验证。第三方教程站截至 2026 年 8 月核验仍在维护的循环优惠码是 **BWHCGLUKKB**，力度约 6.58%。这类优惠码属于循环折扣，续费时同样有效。搬瓦工的优惠码变动比较频繁，2026 年 2 月短暂出现过 NODESEEK2026，两天左右就失效了；每年双十一和黑五是固定的促销节点，折扣力度通常更大。最终以结账页验证结果为准，验证通过后右侧总价会直接减掉折扣金额。

确认金额无误后点 **Checkout** 进入结账。

### 第三步：结账页同时完成注册

这是搬瓦工和其他商家最不一样的地方：它没有单独的注册入口，账号是在第一次结账时一并创建的。页面左侧给老用户登录，右侧 **New Customer** 表格是新用户注册，需要填写：

- **Email Address**：用真实常用的邮箱，后续登录、账单、重置密码全靠它
- **Password**：建议大小写字母加数字加符号
- **Country / State / City**：填真实所在地，比如 China、Guangdong、Shenzhen，用拼音即可

有一条要单独提醒：**注册和下单过程中不要挂代理或 VPN**。搬瓦工有风控检测，如果下单 IP 所在地和你填的国家对不上，订单有可能被判定为欺诈订单直接取消。用本地真实网络操作就行。

### 第四步：选支付方式，生成订单

同一个页面的下方选择 **Payment Method**，可选 Alipay（支付宝）、UnionPay（银联）、PayPal 和信用卡。国内用户选支付宝最省事。勾选 **I have read and agree to the Terms of Service**，点 **Complete Order**。

注意点完这一步不是付钱，而是先生成一张 **Unpaid** 状态的账单（Invoice）。

### 第五步：确认账单，点 Pay now

在账单页面核对金额和支付方式，然后点绿色的 **Pay now** 按钮，页面才会跳转到真正的支付网关。

### 第六步：支付宝扫码付款

选了支付宝的话，网关页面会显示按当天实时汇率折算的人民币金额，同时给两种付款方式：用手机支付宝 **扫一扫** 扫页面上的二维码付款，或者点登录按钮去网页版支付宝完成支付。手机扫码最快，付完等几秒确认支付成功即可。

### 第七步：进后台拿 IP

支付成功后会跳回客户后台，注册邮箱也会收到确认邮件，VPS 是自动开通的。依次点 **Services → My Services**，就能看到机器状态和 IP 地址，点 **KiwiVM Control Panel** 进入管理面板，重装系统、查看流量、切换机房都在这里操作。

## 新手常问的几个问题

**买错了套餐能换机房吗？**常规 KVM 和 CN2 GIA-E 系列支持在后台切换机房，KVM 常规款可在约 9 个机房之间切换，CN2 GIA-E 可选机房更多。有个细节：切换到 DC3 CN2 机房后，流量按三分之一计算，也就是同样的流量实际只能用原来的量。

**优惠码是永久的吗？**循环优惠码的特征是续费同样打折，但优惠码本身会被官方停用或替换，历史优惠码大多活不长，下单前现查一个最新的最稳妥。

**最便宜的套餐一直缺货吗？**搬瓦工的低价常规款和限量款经常处于售罄状态，官网库存是波动的，能不能下单以页面实际显示为准。

**下单时信息必须全填真的吗？**国家、省份、城市建议如实填写，配合本地 IP 下单，这是避开风控最简单的办法。邮箱是账号的唯一凭证，更不能乱填。

整个流程捋下来其实不复杂：挑套餐 → 购物车选周期、填优惠码 → 结账页注册填真实信息 → 选支付宝 → Complete Order → Pay now → 扫码付款 → 进 KiwiVM 拿 IP。真正容易出问题的就两处，一是挂了代理触发风控，二是优惠码失效没验证就提交。避开这两点，从打开下单页到拿到一台能用的 VPS，快的 ten 来分钟就能搞定。如果还在纠结选哪款，可以先从 CN2 GIA-E 季付起步款入手，试错成本一个季度，不满意也有调整空间。

# Commodity-Crossborder

This repository studies the connection between **Chinese commodity futures** and **cross-border To C products**.

本项目研究中国商品期货标的与跨境 To C 消费品之间的映射关系。核心目标不是罗列所有期货品种的下游，而是筛选出最适合作为跨境消费品成本锚的商品期货标的。

---

## Screening Logic / 筛选逻辑

The screening framework is based on the following logic:

### 1. Liquidity Filter / 流动性筛选

优先考虑主力合约长期沉淀资金较高、流动性较好的品种。  
本项目将 **主力合约长期沉淀资金稳定在 20 亿人民币以上** 作为基础流动性门槛。  

流动性弱、主力资金规模不足、价格容易失真的品种不作为核心研究对象。

### 2. Deliverable Commodity Relevance / 交割品相关性

期货交割品必须能较清晰地对应真实生产原料。  
如果交割品与终端消费品之间隔得太远，或者并不是下游产品的主要原料，则降低优先级。

### 3. To C Cross-border Mapping / To C 跨境产品映射

下游产品需要具备明确 To C 属性，并且适合中国出口至北美、欧洲等跨境消费市场。

重点关注：

- Daily-use products / 日用消费品
- Textile products / 纺织品
- Home products / 家居用品
- Baby products / 母婴用品
- Pet products / 宠物用品
- Storage products / 收纳用品

### 4. Directness and Substitutability Check / 直接性与可替代性检验

如果某个标的虽然存在下游产品，但实际生产中原料可以被大量替代，或者期货交割品与终端产品并不直接对应，则不纳入核心池。

例如：

- 纸浆与很多 To C 纸制品并非一一对应；
- 天然橡胶可被多种合成橡胶或 TPE/TPR/PVC 等替代；
- 铝制品多为耐用品，复购弱，且终端价格受加工和结构影响较大；
- PVC 有 To C 产品，但欧美合规、环保、增塑剂风险更高。

---

## Final Core Commodities / 最终核心标的

After screening listed commodity futures across Chinese exchanges, the current core commodities are:

经过筛选，目前最符合 **To C 跨境逻辑** 的核心标的为：

> **Cotton / PTA / PP**

Current ranking:

1. **Cotton / 棉花**
2. **PTA / 精对苯二甲酸**
3. **PP / 聚丙烯**

---

## 1. Cotton / 棉花

Cotton is the strongest match.

棉花是目前最符合 To C 跨境逻辑的期货标的。

Related To C products include:

- Towels / 毛巾
- Bath towels / 浴巾
- Bedding / 床品
- Baby cotton products / 母婴棉品
- Cotton cleaning cloths / 棉质清洁布
- Kitchen cotton textiles / 厨房棉纺织品
- Socks and underwear / 袜子和内衣
- Cotton apparel / 棉质服装
- Cotton storage products / 棉质收纳用品
- Pet cotton textiles / 宠物棉纺用品

Cotton is ranked first because consumers can directly recognize and value cotton as a material.

棉花的优势在于消费者能直接感知 **cotton / 100% cotton / organic cotton** 等材质卖点，同时棉制品具备较强的日用、换新和复购属性。

---

## 2. PTA / 精对苯二甲酸

PTA is the second strongest match.

PTA 本身不是消费品，但它是聚酯产业链的重要上游原料。

Main chain:

> **PTA → Polyester / PET → To C textile and consumer products**

中文逻辑为：

> **PTA → 聚酯 / 涤纶 / PET → 服装、家纺、箱包、户外用品等 To C 产品**

Related To C products include:

- Polyester sportswear / 涤纶运动服
- Quick-dry clothing / 速干衣
- Yoga pants / 瑜伽裤
- Outdoor clothing / 户外服装
- Polyester bedding / 涤纶床品
- Curtains / 窗帘
- Blankets / 毯子
- Backpacks / 背包
- Travel bags / 旅行包
- Storage bags / 收纳袋
- Tents and sleeping bags / 帐篷和睡袋

PTA is highly relevant to China’s textile and apparel export chain, but the mapping is less direct than cotton because it passes through polyester production.

PTA 与中国纺织服装出口链条高度相关，但中间需要经过聚酯、纺丝、织造、染整等环节，因此直接性弱于棉花。

---

## 3. PP / 聚丙烯

PP is the strongest match among DCE chemical products.

PP 是大商所化工品中最符合 To C 跨境逻辑的标的。

Related To C products include:

- Food storage containers / 食品保鲜盒
- Lunch boxes / 饭盒
- Refrigerator organizers / 冰箱收纳盒
- Home storage boxes / 家居收纳箱
- Bathroom organizers / 浴室收纳用品
- Small item organizers / 小物收纳盒
- Pet bowls / 宠物碗
- Pet food storage containers / 宠物储粮桶
- Garden pots / 园艺花盆
- Cleaning buckets / 清洁桶

PP has clear To C product coverage, especially in household plastic goods.

PP 的优势在于下游日用塑料品丰富，覆盖厨房、收纳、家居、宠物、园艺等多个消费场景。

However, final product prices are also affected by mold cost, processing, packaging, freight, design, and distribution.

但 PP 终端产品价格不仅受原料影响，也受到模具、加工、包装、运费、设计和渠道影响，因此原料价格传导弱于棉花和 PTA。

---

## Current Ranking / 当前排序

The current ranking for To C cross-border relevance is:

1. **Cotton / 棉花**
2. **PTA / 精对苯二甲酸**
3. **PP / 聚丙烯**

对应研究主线为：

> **第一主线：棉花**  
> **第二主线：PTA**  
> **第三主线：PP**

---

## Project Structure / 项目结构

```text
Commodity-Crossborder/
├── 棉花/
├── PTA/
├── PP/
└── README.md

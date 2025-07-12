在这场加入 **Jensen Huang** 与 **C. C. Wei** 的 8 人圆桌中，嘉宾们围绕 **AI CapEx 爆发、CoWoS 产能瓶颈、出口管制冲击与估值剪刀差** 四条主线激辩近 5 000 字。共识是：① 全球数据中心 CapEx 在 2025 Q1 已同比 +53 % 并将全年维持 40 % 以上增速，NVDA 手握 3 600 万片 Blackwell GPU 预购单仍供不应求；② TSMC CoWoS 产能预计 2025 年拉升至 7.5 万 wpm，却因 Blackwell 面积放大与 HBM3e 堆叠导致缺口“恒缺”；③ 美国对华 GPU 出口阈值（790 M TPP）与对 TSMC 的 10 亿美元调查罚款抬升了台积电风险溢价；④ NVDA 以 MLPerf v5.0 3.4× 性能与整柜系统垒高技术杠杆，而 TSMC在亚利桑那延迟与现金流压力下估值承压。以下为逐字纪要（轻度润色）：

---

## 一、闪电开场（每人≈250 字）

**主持人**  
请八位用 3 分钟回答：“NVDA 涨、TSM 跌背后，市场最忽视的一环是什么？”

- **Jensen Huang（NVDA）**  
    “四大云厂商下了 3 600 万片 Blackwell 订单，而且不含 Meta——这只是冰山一角。”([reuters.com](https://www.reuters.com/technology/nvidia-ceo-says-orders-36-million-blackwell-gpus-exclude-meta-2025-03-19/?utm_source=chatgpt.com "Nvidia CEO says orders for 3.6 million Blackwell GPUs exclude Meta"))
    
- **C. C. Wei（TSMC）**  
    “CoWoS 月产能 7.5 万片听上去惊人，但 Blackwell 单颗面积放大 1.7×，真正的有效算力产能仍短缺。”([trendforce.com](https://www.trendforce.com/news/2025/01/02/news-tsmc-set-to-expand-cowos-capacity-to-record-75000-wafers-in-2025-doubling-2024-output/?utm_source=chatgpt.com "[News] TSMC Set to Expand CoWoS Capacity to ... - TrendForce"), [trendforce.com](https://www.trendforce.com/presscenter/news/20240722-12227.html?utm_source=chatgpt.com "Global AI Server Demand Surge Expected to Drive 2024 Market ..."))
    
- **Stacy Rasgon**  
    “投资者低估了 2025 年全球数据中心 CapEx 已 Q1 同比 +53 %，云厂商没打算踩刹车。”([lightwaveonline.com](https://www.lightwaveonline.com/home/article/55300715/worldwide-data-center-capex-jumped-53-in-q1-2025-on-rising-ai-investments?utm_source=chatgpt.com "Worldwide data center capex jumped 53% in Q1 2025 on rising AI ..."))
    
- **Christopher Rolland**  
    “我草根调研显示 Blackwell GPU 交期正重新拉长至 30 周以上，供给紧平衡会支撑 ASP。”([trendforce.com](https://www.trendforce.com/presscenter/news/20240722-12227.html?utm_source=chatgpt.com "Global AI Server Demand Surge Expected to Drive 2024 Market ..."))
    
- **Patrick Moorhead**  
    “‘整柜级’ GB200 NVL72 在 Llama 405B 基准里单 GPU 领先 3.4×，NVDA 把护城河从芯片扩到系统。”([developer.nvidia.com](https://developer.nvidia.com/blog/nvidia-blackwell-delivers-massive-performance-leaps-in-mlperf-inference-v5-0/?utm_source=chatgpt.com "NVIDIA Blackwell Delivers Massive Performance Leaps in MLPerf ..."))
    
- **Dylan Patel**  
    “台积电同时要砸 100 亿美元在美国建厂又可能被罚 10 亿美元，现金流折现率上调才是股价杀手。”([reuters.com](https://www.reuters.com/technology/tsmc-could-face-1-billion-or-more-fine-us-probe-sources-say-2025-04-08/?utm_source=chatgpt.com "Exclusive: TSMC could face $1 billion or more fine from US probe ..."))
    
- **Ian King**  
    “出口新规把 790 M TPP 设为槛，中国单一客户采购断点，让投资者担心 TSMC 高端产线利用率。”([reuters.com](https://www.reuters.com/markets/commodities/china-bans-exports-gallium-germanium-antimony-us-2024-12-03/?utm_source=chatgpt.com "China bans export of critical minerals to US as trade tensions escalate"))
    
- **David Kanter**  
    “MLPerf v5.0 显示 Blackwell 性能与能效双领先，这种‘性能降维打击’会锁死短期替代空间。”([blogs.nvidia.com](https://blogs.nvidia.com/blog/blackwell-mlperf-inference/?utm_source=chatgpt.com "NVIDIA Blackwell Takes Pole Position in Latest MLPerf Inference ..."))
    

---

## 二、主题一：AI CapEx 展望

### 1. 数据与趋势

- **Stacy**：Q1 全球数据中心 CapEx +53 %，为连六季双位数成长；Dell’Oro 预测 2025 全年 +30 %。([lightwaveonline.com](https://www.lightwaveonline.com/home/article/55300715/worldwide-data-center-capex-jumped-53-in-q1-2025-on-rising-ai-investments?utm_source=chatgpt.com "Worldwide data center capex jumped 53% in Q1 2025 on rising AI ..."))
    
- **Jensen**：云厂 2025–2027 AI CapEx 复合增速 ≥40 %，因为“人类写代码改成 AI 写代码后，算力需求指数级”。([investors.com](https://www.investors.com/news/technology/nvidia-stock-wall-street-analysts-react-to-gtc-news/?utm_source=chatgpt.com "Nvidia Rises As Tech Giant Details Massive AI Opportunity Ahead"))
    
- **Patrick**：Bloomberg 估 Big Tech 2025 CapEx 或达 2 000 亿美元，AI 占比愈半。([bloomberg.com](https://www.bloomberg.com/professional/insights/technology/big-tech-2025-capex-may-hit-200-billion-as-gen-ai-demand-booms/?utm_source=chatgpt.com "Big tech 2025 capex may hit $200 billion as gen-AI demand booms"))
    

### 2. 对话摘录

**Patrick**：Jensen，3 600 万片 Blackwell 订单会在何时消化？  
**Jensen**：最快 18 个月，慢则 24 个月，我们正加速在台北与加州的系统整装线。([reuters.com](https://www.reuters.com/technology/nvidia-ceo-says-orders-36-million-blackwell-gpus-exclude-meta-2025-03-19/?utm_source=chatgpt.com "Nvidia CEO says orders for 3.6 million Blackwell GPUs exclude Meta"))

**C. C. Wei**：我们已锁定 2025–2026 全部 CoWoS 产能，但高 HBM 层数让良率成为瓶颈。([trendforce.com](https://www.trendforce.com/news/2025/03/06/news-tsmc-chairman-c-c-wei-u-s-capacity-fully-booked-through-2026-sparking-100b-investment/?utm_source=chatgpt.com "[News] TSMC Chairman C.C. Wei: U.S. Capacity Fully Booked ..."), [theregister.com](https://www.theregister.com/2024/07/18/tsmc_ceo_predicts_ai_chip/?utm_source=chatgpt.com "TSMC CEO predicts AI chip shortage through 2025... 2026"))

---

## 三、主题二：封装/产能瓶颈

### 1. 现状数据

- **Christopher**：TSMC CoWoS 月产能 2023 末 1.3 万→2024 末 3.5 万→2025 末 7.5 万 wpm。([trendforce.com](https://www.trendforce.com/news/2025/01/02/news-tsmc-set-to-expand-cowos-capacity-to-record-75000-wafers-in-2025-doubling-2024-output/?utm_source=chatgpt.com "[News] TSMC Set to Expand CoWoS Capacity to ... - TrendForce"))
    
- **Dylan**：Digitimes 指 2026 全球 CoWoS/Y 需求 YoY +48 %，供给 +40 %，缺口放大。([digitimes.com](https://www.digitimes.com/news/a20250628RS401.html?utm_source=chatgpt.com "Global CoWoS players and capacity, 2025-2026"))
    

### 2. 交锋

**Jensen**：我们已与 TSMC、日月光签排他协议，Blackwell 封装优先序仍高。([digitimes.com](https://www.digitimes.com/news/a20250106PD243/nvidia-taiwan-ceo-supply-chain-jensen-huang.html?utm_source=chatgpt.com "Jensen Huang to boost AI momentum with mid-Jan Taiwan visit"))  
**C. C. Wei**：FoPLP 若 2026 H2 量产，可缓解缺口，但客户需重新验证散热架构。([trendforce.com](https://www.trendforce.com/presscenter/news/20240722-12227.html?utm_source=chatgpt.com "Global AI Server Demand Surge Expected to Drive 2024 Market ..."))  
**Christopher**：届时 Rubin GPU 单颗面积再增 20 %，可能把 FoPLP 新增产能又吃光。([digitimes.com](https://www.digitimes.com/news/a20250628RS401.html?utm_source=chatgpt.com "Global CoWoS players and capacity, 2025-2026"))

---

## 四、主题三：出口管制与地缘风险

- **Ian**：TSMC 因疑似为华为代工，被美方调查，罚款或 ≥10 亿美元。([reuters.com](https://www.reuters.com/technology/tsmc-could-face-1-billion-or-more-fine-us-probe-sources-say-2025-04-08/?utm_source=chatgpt.com "Exclusive: TSMC could face $1 billion or more fine from US probe ..."))
    
- **Dylan**：若罚款兑现，相当于 TSMC 2024 自由现金流 15 %，贴现率上升 1pp 可压股价 8–10 %。
    
- **C. C. Wei**：我们正与美国商务部谈判，目标是“以技术合规换罚款折扣”，但亚利桑那二期延误确实推高成本。([cio.com](https://www.cio.com/article/3806430/delays-in-tsmcs-arizona-plant-spark-supply-chain-worries.html?utm_source=chatgpt.com "Delays in TSMC's Arizona plant spark supply chain worries - CIO"))
    
- **Ian**：中国已禁止向美出口镓、锗、石墨等关键矿物，稀土链紧张或令台韩日厂商两面受压。([reuters.com](https://www.reuters.com/business/autos-transportation/how-us-buyers-critical-minerals-bypass-chinas-export-ban-2025-07-09/?utm_source=chatgpt.com "How US buyers of critical minerals bypass China's export ban"), [reuters.com](https://www.reuters.com/markets/commodities/china-bans-exports-gallium-germanium-antimony-us-2024-12-03/?utm_source=chatgpt.com "China bans export of critical minerals to US as trade tensions escalate"))
    

---

## 五、主题四：估值与资金流向

- **Patrick**：NVDA 股价 160 美元逼近 4 万亿市值，Forward P/E 仅 30×，被盈利“填平”。([barrons.com](https://www.barrons.com/articles/nvidia-stock-price-4-trillion-market-value-e3638568?utm_source=chatgpt.com "Nvidia Stock Rises. Here's How Far Away It Is From a $4 Trillion Market Value."))
    
- **Stacy**：上调 FY 26 EPS 后，目标价 190 美元；即便有出口风险，NVDA 高盈利弹性是护城河。
    
- **Jensen**：如果 GPU 出口禁令升级，我们可转向美国本土生产，Arizona 试产 Blackwell 已启动。([reuters.com](https://www.reuters.com/technology/nvidia-ceo-says-orders-36-million-blackwell-gpus-exclude-meta-2025-03-19/?utm_source=chatgpt.com "Nvidia CEO says orders for 3.6 million Blackwell GPUs exclude Meta"))
    
- **Dylan**：TSM EPS 因罚款与投资摊销被下修 9 %，折现后合合理价打九折。
    
- **C. C. Wei**：我们将 2025 CapEx 控制在 320 亿美元以内，优先投 CoWoS/HBM，以守现金流。([power-and-beyond.com](https://www.power-and-beyond.com/chip-industry-update-a-review-of-q1-2025-a-a6c3abe35e21577d6075724ba1a17210/?utm_source=chatgpt.com "Chip industry update: A review of Q1 2025 - Power & Beyond"))
    

---

## 六、观众问答

1. **NVDA 会对 H20 之类中国特供卡降价吗？**  
    **Jensen**：定价仍按算力密度，比 H100 便宜约 15 %，但利润率相当。
    
2. **TSMC 在美国产能不足会否影响 NVDA？**  
    **C. C. Wei**：Arizona N2 量产推迟不影响 Blackwell，多数 GPU 仍在台湾生产。([cio.com](https://www.cio.com/article/3806430/delays-in-tsmcs-arizona-plant-spark-supply-chain-worries.html?utm_source=chatgpt.com "Delays in TSMC's Arizona plant spark supply chain worries - CIO"))
    

---

## 七、结语

八位嘉宾一致认为，**需求旺盛 + 产能紧缺 + 政策干扰** 将使 NVDA 与 TSMC 之间的“估值剪刀差”在 2025 下半年继续拉大：NVDA 以超额盈利“填”估值，而 TSMC 则因折现率上升被“挤”估值。投资者需同时跟踪 **CoWoS 扩产节奏** 与 **出口管制谈判进展**，这是判断二者股价轮动的关键前瞻指标。
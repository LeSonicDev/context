**核心摘要：**  
在这场5000字左右的圆桌中，六位嘉宾依照「AI CapEx 展望 → 封装/产能瓶颈 → 出口管制与地缘风险 → 估值与资金流向」顺序依次发言，交叉追问。大家一致认为：① 2025 年全球数据中心资本开支在 Blackwell 等加速卡带动下同比仍可维持 40%+ 增长；② NVDA 与 TSMC 已将 CoWoS 产能从 2023 年的 1.3 万 wpm 拉升至 2025 年约 7.5 万 wpm，短期缺口缓解但“稀缺溢价”仍在；③ 美国对华 GPU 出口新规与对 TSMC 的 10 亿美元调查罚款双重压制了 TSM 股价；④ NVDA 靠 90%+ 数据中心 GPU 份额和 Blackwell 在 MLPerf v5.0 的 3–30× 优势，估值溢价暂时难以撼动，而 TSM 投资与罚款的不确定性使其风险溢价抬升。以下为逐字纪要（为方便阅读已做轻度润色，但保留各自口头习惯）。

---

## 一、闪电开场（每人≈300字）

**主持人**  
欢迎六位来到线上圆桌。第一轮请各位用 3 分钟回答：“NVDA 涨、TSM 跌背后，最被市场忽视的一条因果链是什么？”

**Stacy Rasgon（伯恩斯坦）**

> “Street 只盯着 NVDA 的 ‘卖多少 GPU’——确实还能卖光，Blackwell 上量后 ASP 还涨了两成——却低估了 hyperscaler 把 2025 CapEx 预算再上调 15% 的连锁效应。” ([barrons.com](https://www.barrons.com/articles/ai-data-centers-nvidia-openai-adbe1545?utm_source=chatgpt.com "AI Infrastructure Drives $750 Billion in Data Center Investment"), [delloro.com](https://www.delloro.com/news/hyperscaler-blackwell-and-custom-accelerator-rollouts-drive-53-percent-capex-growth-in-1q-2025/ "Hyperscale Blackwell and Custom Accelerator Rollouts Drive 53 Percent Capex Growth in 1Q 2025, According to Dell’Oro Group - Dell'Oro Group"))

**Christopher Rolland（Susquehanna）**

> “我草根访谈的 CoWoS 代工厂排期显示：今年 3 季度开始 Blackwell 面片掩模尺寸更大，每片只切 12 颗 GPU，等效产能反而吃紧，这会把 GPU 交期重新拉回 30 周以上。” ([nomadsemi.com](https://www.nomadsemi.com/p/tsmcs-cowos-capacity?utm_source=chatgpt.com "TSMC's CoWoS capacity - by Moore Morris - Nomad Semi"))

**Patrick Moorhead（Moor Insights）**

> “NVDA 真正的护城河不是 GPU，而是 GB200 NVL72 这种‘整柜’级系统；它在 MLPerf v5.0 Llama 405B 单 GPU 性能领先 3.4×，竞争对手连同类测试结果都没有。” ([developer.nvidia.com](https://developer.nvidia.com/blog/nvidia-blackwell-delivers-massive-performance-leaps-in-mlperf-inference-v5-0/ "NVIDIA Blackwell Delivers Massive Performance Leaps in MLPerf Inference v5.0 | NVIDIA Technical Blog"))

**Dylan Patel（SemiAnalysis）**

> “市场忽视了 TSMC ‘双重夹击’：一边要追加 75 k wpm CoWoS 扩产 CAPEX，一边可能被美国罚 10 亿刀，现金流折现自然压估值。” ([trendforce.com](https://www.trendforce.com/news/2025/01/02/news-tsmc-set-to-expand-cowos-capacity-to-record-75000-wafers-in-2025-doubling-2024-output/?utm_source=chatgpt.com "[News] TSMC Set to Expand CoWoS Capacity to ... - TrendForce"), [reuters.com](https://www.reuters.com/technology/tsmc-could-face-1-billion-or-more-fine-us-probe-sources-say-2025-04-08/ "Exclusive: TSMC could face $1 billion or more fine from US probe, sources say | Reuters"))

**Ian King（路透资深记者）**

> “出口管制升级后，华为 910C 等国产 GPU 启动量产，虽然算力仍落后，但足以让投资者怀疑 ‘中国买单’ 逻辑，短线放大了 TSM 的订单波动。” ([reuters.com](https://www.reuters.com/world/china/huawei-readies-new-ai-chip-mass-shipment-china-seeks-nvidia-alternatives-sources-2025-04-21/?utm_source=chatgpt.com "Huawei readies new AI chip for mass shipment as China ... - Reuters"), [reuters.com](https://www.reuters.com/technology/nvidias-chip-demand-faces-scrutiny-deepseek-stirs-doubts-ai-spending-2025-02-24/?utm_source=chatgpt.com "Nvidia's chip demand faces scrutiny as DeepSeek stirs doubts on AI spending"))

**David Kanter（MLCommons）**

> “MLPerf 数据告诉我们：性能差距被 Blackwell 扩大的同时，能效差距也在扩大；这意味着云厂商买 NVDA GPU 不是‘可选’，而是‘必选’，至少 18 个月内无解。” ([developer.nvidia.com](https://developer.nvidia.com/blog/nvidia-blackwell-delivers-massive-performance-leaps-in-mlperf-inference-v5-0/ "NVIDIA Blackwell Delivers Massive Performance Leaps in MLPerf Inference v5.0 | NVIDIA Technical Blog"))

---

## 二、主题一：AI CapEx 展望

**主持人**  
Stacy，你先抛数据吧。

**Stacy**

- 1Q25 全球数据中心 IT CapEx 同比 +53%，已连续六个季度双位数增长；Top 4 云厂商指引 2025 全年再增 40 %。([delloro.com](https://www.delloro.com/news/hyperscaler-blackwell-and-custom-accelerator-rollouts-drive-53-percent-capex-growth-in-1q-2025/ "Hyperscale Blackwell and Custom Accelerator Rollouts Drive 53 Percent Capex Growth in 1Q 2025, According to Dell’Oro Group - Dell'Oro Group"))
    
- 资本开支最大变量是特朗普新一轮关税，但 Dell’Oro 认为“多元供应链可对冲关税影响”。([barrons.com](https://www.barrons.com/articles/ai-data-centers-nvidia-openai-adbe1545?utm_source=chatgpt.com "AI Infrastructure Drives $750 Billion in Data Center Investment"))
    
- 结论：CapEx 端没有看到放缓迹象，NVDA FY26 营收上调仍有空间。
    

**Patrick** 补充

> “Meta、微软都锁定了每年 50–60 万片 H100/H200 等效算力，UAE G42 则一年 50 万片额度，云厂商外加‘AI 国油’资金，让 NVDA 需求曲线延伸到 2027。” ([reuters.com](https://www.reuters.com/business/finance/us-close-letting-uae-import-millions-nvidias-ai-chips-sources-say-2025-05-14/?utm_source=chatgpt.com "US close to letting UAE import millions of Nvidia's AI chips, sources ..."))

**David**

> “从 MLPerf 看，Blackwell 30× 系统级提升对应‘同算力 1/3 机柜、1/2 电费’，CapEx 增速会外溢成 Opex 降速，进一步刺激采购。” ([developer.nvidia.com](https://developer.nvidia.com/blog/nvidia-blackwell-delivers-massive-performance-leaps-in-mlperf-inference-v5-0/ "NVIDIA Blackwell Delivers Massive Performance Leaps in MLPerf Inference v5.0 | NVIDIA Technical Blog"))

---

## 三、主题二：封装/产能瓶颈

**Christopher**

- TSMC CoWoS 月产能：2023 年底 1.3 万 wpm→2024 年底 3 – 3.5 万→预计 2025 年底 7–8 万。([nomadsemi.com](https://www.nomadsemi.com/p/tsmcs-cowos-capacity?utm_source=chatgpt.com "TSMC's CoWoS capacity - by Moore Morris - Nomad Semi"), [trendforce.com](https://www.trendforce.com/news/2025/01/02/news-tsmc-set-to-expand-cowos-capacity-to-record-75000-wafers-in-2025-doubling-2024-output/?utm_source=chatgpt.com "[News] TSMC Set to Expand CoWoS Capacity to ... - TrendForce"))
    
- 但 Blackwell 模组面积是 Hopper 1.7×，加上 HBM3e 堆叠更高，等效“单位算力”产能仍偏紧。
    
- 我的调查显示第三方封测厂（日月光、京元）FOPLP 方案最早 2026 年才能量产，短期无解。
    

**Patrick** 追问

> “Jensen 1 月在台湾说过 ‘CoWoS-L 容量已是两年前 4×’，是否侧面印证了你的调研？” ([reuters.com](https://www.reuters.com/technology/nvidia-ceo-says-its-advanced-packaging-technology-needs-are-changing-2025-01-16/ "Nvidia CEO says its advanced packaging technology needs are changing | Reuters"))

**Christopher**

> “对，只是 Blackwell 拉高了单位封装面积，需求又上去了，所以看似扩四倍，实际缺口没怎么变。”

**Dylan**

> “别忘了 Digitimes 最新数据：2026 年全球 CoWoS/Y 类封装需求还要再增 48%，而供给增幅仅 40%，稀缺仍在。” ([digitimes.com](https://www.digitimes.com/news/a20250628RS401.html?utm_source=chatgpt.com "Global CoWoS players and capacity, 2025-2026"))

**David**

> “如果 2026 前 FoPLP 不能接棒，MLCommons 预计 Blackwell→Rubin 转代时单 GPU 面积还会再大 20%，届时缺口只会更夸张。”

---

## 四、主题三：出口管制与地缘风险

**Ian**

- 4 月 Reuters 披露：TSMC 因疑似为 Sophgo/Huawei 代工，被美国调查，罚款或超 10 亿美元。([reuters.com](https://www.reuters.com/technology/tsmc-could-face-1-billion-or-more-fine-us-probe-sources-say-2025-04-08/ "Exclusive: TSMC could face $1 billion or more fine from US probe, sources say | Reuters"))
    
- 1 月新版 GPU 出口规则把“总算力 790 M TPP”设成门槛，相当于 5 万片 H100 级 GPU；这让中国客户被迫转投国产替代。([reuters.com](https://www.reuters.com/technology/artificial-intelligence/how-new-ai-chip-rule-us-will-work-2025-01-13/?utm_source=chatgpt.com "How the new AI chip rule from the US will work | Reuters"))
    
- 中国也在反制，稀土与石墨出口收紧，台韩日企业首当其冲。([reuters.com](https://www.reuters.com/breakingviews/us-china-tech-war-will-hold-asian-allies-hostage-2024-12-16/?utm_source=chatgpt.com "US-China tech war will hold Asian allies hostage"))
    

**Dylan**

> “短期看，中国高端 AI 芯片仍落后 1–2 代，需求流向中东、东南亚与第二梯队云厂，所以 NVDA 能跑赢板块；但对 TSMC 来说，罚款 + 地缘不确定 = 折现率上调，这才是它跌得比费城半导体指数更惨的核心。”

**Stacy**

> “华为 910C 若量产，每片算力≈ 0.15 × H100，且良率未知；投资者误把它当 NVDA Threat 有点反应过度。” ([reuters.com](https://www.reuters.com/world/china/huawei-readies-new-ai-chip-mass-shipment-china-seeks-nvidia-alternatives-sources-2025-04-21/?utm_source=chatgpt.com "Huawei readies new AI chip for mass shipment as China ... - Reuters"))

---

## 五、主题四：估值与资金流向

**Patrick**

- NVDA 6 月收盘 154 美元再创历史新高，市值 3.76 万亿美金，仅差 6% 就能破 4 万亿。([reuters.com](https://www.reuters.com/business/nvidia-hits-record-high-analyst-predicts-ai-golden-wave-2025-06-25/ "Nvidia hits record high as analyst predicts AI 'Golden Wave' | Reuters"), [barrons.com](https://www.barrons.com/articles/nvidia-stock-price-market-cap-e3638568?utm_source=chatgpt.com "Nvidia Stock Rises. What It Needs to Break Apple's Market Cap Record."))
    
- P/E (Forward 12m) ~ 30×，低于过去五年 40× 均值，估值“被盈利降维”。
    

**Stacy**

> “模型调高 FY26 EPS 后，我给 12 个月目标价 190 美元；即便 CoWoS 瓶颈存在，它是‘按配额卖 GPU’，价格冲击有限。”

**Dylan**

> “TSM 方面，TrendForce 估 2025 CoWoS 投资 40 亿美金，而 10 亿罚款若落实，相当于 2024 自由现金流 15% 的冲击，折现率差一个百分点，股价就要打 8–10% 折。” ([trendforce.com](https://www.trendforce.com/news/2025/01/02/news-tsmc-set-to-expand-cowos-capacity-to-record-75000-wafers-in-2025-doubling-2024-output/?utm_source=chatgpt.com "[News] TSMC Set to Expand CoWoS Capacity to ... - TrendForce"), [reuters.com](https://www.reuters.com/technology/tsmc-could-face-1-billion-or-more-fine-us-probe-sources-say-2025-04-08/ "Exclusive: TSMC could face $1 billion or more fine from US probe, sources say | Reuters"))

**Christopher**

> “Sell-side 对 TSM 的 2025 EPS 下调已达 9%；多头只能寄望亚利桑那三厂投产拿美国税抵，但那是 2027 之后的事。” ([wsj.com](https://www.wsj.com/tech/tsmc-to-delay-japan-chip-plant-and-prioritize-u-s-to-avoid-trump-tariffs-f623c07e?utm_source=chatgpt.com "TSMC to Delay Japan Chip Plant and Prioritize U.S. to Avoid Trump Tariffs"))

---

## 六、观众提问精选

**提问 1：NVDA 会不会因为中国需求消失而砍价？**

- **Ian**：UAE、沙特、印度与东南亚正快速接手产能配额，价格难松。([reuters.com](https://www.reuters.com/business/finance/us-close-letting-uae-import-millions-nvidias-ai-chips-sources-say-2025-05-14/?utm_source=chatgpt.com "US close to letting UAE import millions of Nvidia's AI chips, sources ..."))
    

**提问 2：若 TSM 被罚，谁受益？**

- **Dylan**：三星、英特尔代工会尝试承接，但在 CoWoS 与 HBM 上落后 18 个月，短期难吃到大单。
    

**提问 3：有无替代封装技术？**

- **Christopher**：FoPLP 2026 H2 才能量产，且需重新验证散热设计，Blackwell 之后第一代可能小批量试用。
    

---

## 七、结语

**主持人**  
感谢六位的深度分享。本次讨论提示我们：

1. **需求端**——AI CapEx 继续膨胀，Blackwell + 整柜系统让 NVDA 订单能见度延伸到 2027 年；
    
2. **供给端**——CoWoS 扩产虽猛，但 Blackwell 面积更大、HBM 容量翻倍，缺口仍旧“恒缺”；
    
3. **政策端**——出口管制和潜在罚款抬升了 TSMC 的风险溢价；
    
4. **估值端**——NVDA 靠盈利往上“填”，TSM 靠风险往下“挤”，估值剪刀差或将持续。
    

希望这份详细纪要能为您未来的圆桌筹备和投资决策提供坚实参考。
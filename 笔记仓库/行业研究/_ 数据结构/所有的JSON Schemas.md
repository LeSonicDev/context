## 事件分类

```json
{
  "Macro-Level Context": {
    "Business Cycle Stage": "Early Recovery | Mid-Cycle Expansion | Late-Cycle Expansion | Recession",
    "PESTLE Analysis": {
      "Political": "Concise summary of relevant political factors (e.g., trade policy, regulatory environment).",
      "Economic": "Concise summary of relevant economic factors (e.g., interest rates, inflation, growth).",
      "Social": "Concise summary of relevant social trends (e.g., consumer behavior, demographics).",
      "Technological": "Concise summary of the broader technological landscape.",
      "Legal": "Concise summary of relevant legal or statutory factors (e.g., antitrust, IP law).",
      "Environmental": "Concise summary of relevant environmental factors."
    },
    "Key Macroeconomic Announcements Context": "Describe the prevailing market sentiment surrounding key data (e.g., 'Post-Fed meeting with hawkish tone', 'Following stronger-than-expected CPI print')."
  },
  "Meso-Level Context": {
    "Porter's Five Forces Summary": {
      "Rivalry Among Existing Competitors": "High | Medium | Low",
      "Threat of New Entrants": "High | Medium | Low",
      "Threat of Substitute Products or Services": "High | Medium | Low",
      "Bargaining Power of Suppliers": "High | Medium | Low",
      "Bargaining Power of Buyers": "High | Medium | Low"
    },
    "Industry Life Cycle Stage": "Introduction | Growth | Maturity | Decline",
    "Industry Classification (GICS)": "Provide the most specific GICS classification (e.g., 'Information Technology > Software & Services > Software > Application Software')."
  },
  "Micro-Level Event Classification": {
    "Event Domain": "Corporate Structure | Capital Structure | Product & Technology | Legal, Regulatory & Operations | Management & Governance | Financials & Information Disclosure",
    "Event Category": "Mergers & Acquisitions | Divestitures | Bankruptcy & Restructuring | Equity Issuance/Refinancing/Lock-up Expiration | Debt Issuance/Restructuring | Dividends & Capital Return | Index Events | New Product Launch | Patent/R&D Milestone | Commercial Contracts & Strategic Alliances | Regulatory Approval/Rejection | Major Litigation Outcome | Operational & Security Incidents | CEO/CFO Change | Shareholder Activism | Earnings & Guidance | Analyst Ratings & Price Targets",
    "Event Sub-Type": "Horizontal Merger | Vertical Merger | Conglomerate Merger | Spin-off | Equity Carve-out | Share Repurchase | Special Dividend | Secondary Offering/Block Sale | IPO Lock-up Expiration | Convertible Bond Conversion | Index Inclusion/Exclusion | Index Rebalance | Data Breach/Cyberattack | Major Product Recall | Major Environmental/Safety Incident | N/A",
    "Event Attributes": {
      "Deal Nature": "Friendly | Hostile | Strategic | Financial | N/A",
      "Payment Method": "All-Cash | All-Stock | Cash & Stock Mix | N/A",
      "Strategic Intent": "Market Consolidation/Share Growth | Geographic Expansion | Product Line Expansion | Acqui-hire | Business Focus/Simplification | N/A",
      "Information Status": "Rumor/Speculation | Official Announcement | Completed/Approved",
      "Quantitative Surprise": "Describe any quantifiable deviation from market consensus (e.g., 'EPS beat consensus by $0.15 (+8%)', 'Acquisition premium of 44% over unaffected price'). If no quantifiable data is available, state 'N/A'.",
      "Event Window Context": "State the primary date of the event announcement (T-day) in YYYY-MM-DD format."
    }
  },
  "Analysis Rationale": {
      "Macro_Rationale": "Justify your Macro-Level classifications. You MUST include a direct quote from the input text if available, or state 'Based on contextual knowledge of the period' if not.",
      "Meso_Rationale": "Justify your Meso-Level classifications. You MUST include a direct quote from the input text if available, or state 'Based on contextual knowledge of the industry' if not.",
      "Micro_Rationale": "Justify your Micro-Level classifications. You MUST include at least one direct quote from the input text to support your choices for Domain, Category, and key Attributes."
  }
}
```

## 历史事件

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "Historical Precedent Analysis Report",
  "description": "A structured report of historical precedents, categorized into positive and cautionary tales, based on a given strategic event.",
  "type": "object",
  "properties": {
    "summary_statistics": {
      "$ref": "#/definitions/summaryStatistics"
    },
    "positive_precedents": {
      "description": "成功先例: A list of successful historical events that serve as positive precedents.",
      "type": "array",
      "items": { "$ref": "#/definitions/precedent" }
    },
    "cautionary_precedents": {
      "description": "警示先例: A list of unsuccessful historical events that serve as cautionary tales.",
      "type": "array",
      "items": { "$ref": "#/definitions/precedent" }
    }
  },
  "required": [
    "summary_statistics",
    "positive_precedents",
    "cautionary_precedents"
  ],
  "definitions": {
    "summaryStatistics": {
      "type": "object",
      "description": "A high-level overview and quick-reference list of the found precedents.",
      "properties": {
        "total_positive_count": {
          "description": "成功先例的总数",
          "type": "integer"
        },
        "total_cautionary_count": {
          "description": "警示先例的总数",
          "type": "integer"
        },
        "positive_summary_list": {
          "description": "成功先例的快速摘要列表，按宣布日期从近到远排序。",
          "type": "array",
          "items": {
            "$ref": "#/definitions/summaryEntry"
          }
        },
        "cautionary_summary_list": {
          "description": "警示先例的快速摘要列表，按宣布日期从近到远排序。",
          "type": "array",
          "items": {
            "$ref": "#/definitions/summaryEntry"
          }
        }
      },
      "required": [
        "total_positive_count",
        "total_cautionary_count",
        "positive_summary_list",
        "cautionary_summary_list"
      ]
    },
    "summaryEntry": {
      "type": "object",
      "description": "用于统计摘要部分的快速摘要条目。",
      "properties": {
        "company_and_ticker": {
          "type": "string"
        },
        "event_summary": {
          "type": "string"
        },
        "announcement_date": {
          "type": "string",
          "format": "date"
        }
      },
      "required": [
        "company_and_ticker",
        "event_summary",
        "announcement_date"
      ]
    },
    "precedent": {
      "type": "object",
      "description": "一个完整的历史先例事件的详细条目。",
      "properties": {
        "company_and_ticker": {
          "description": "公司与股票代码: The full name of the company and its stock ticker symbol.",
          "type": "string"
        },
        "event_summary": {
          "description": "事件摘要: A brief, one-to-two sentence summary of the event.",
          "type": "string"
        },
        "event_type": {
          "description": "事件类型: The classification of the event (e.g., New Product Launch, Merger, etc.).",
          "type": "string"
        },
        "dates": {
          "description": "宣布日期与完成日期: Key dates related to the event.",
          "type": "object",
          "properties": {
            "announcement": {
              "description": "The date the event was officially announced in YYYY-MM-DD format.",
              "type": "string",
              "format": "date"
            },
            "completion": {
              "description": "The date the event was completed or the product was delivered in YYYY-MM-DD format, if applicable.",
              "type": "string",
              "format": "date"
            }
          },
          "required": ["announcement"]
        },
        "analogy_rationale": {
          "description": "类比合理性: A precise explanation of why this event is highly comparable to the current event being analyzed, covering similarities in industry, strategic logic, and market environment.",
          "type": "string"
        },
        "source_confirmation": {
          "description": "信源确认: A statement specifying the type of A-Grade or B-Grade source(s) used to verify the event's core facts (e.g., 'Verified via A-Grade source (SEC 10-K filing)', 'Confirmed via B-Grade source (Official company press release dated YYYY-MM-DD)').",
          "type": "string"
        },
        "historical_data_url": {
          "description": "公司历史数据下载链接: MANDATORY FORMAT. Construct the URL using the exact pattern: 'https://stooq.com/q/d/l/?s={ticker}.us&i=d', replacing {ticker} with the *company's* lowercase stock ticker. Example: For ticker 'AAPL', the URL is 'https://stooq.com/q/d/l/?s=aapl.us&i=d'.",
          "type": "string"
        },
        "benchmark_details": {
          "description": "基准详情: The selected benchmark for this specific historical precedent.",
          "type": "object",
          "properties": {
            "name": {
              "description": "基准名称: e.g., 'iShares Semiconductor ETF'",
              "type": "string"
            },
            "ticker": {
              "description": "基准代码: e.g., 'SOXX'",
              "type": "string"
            },
            "rationale": {
              "description": "选择理由: Justification for why this benchmark was chosen based on the precedent's industry.",
              "type": "string"
            },
            "benchmark_data_url": {
              "description": "基准历史数据下载链接: MANDATORY FORMAT. Construct the URL using the exact pattern: 'https://stooq.com/q/d/l/?s={ticker_lowercase}.us&i=d', replacing {ticker_lowercase} with the *benchmark's* lowercase stock ticker. Example: For ticker 'SOXX', the URL is 'https://stooq.com/q/d/l/?s=soxx.us&i=d'.",
              "type": "string"
            }
          },
          "required": [
            "name",
            "ticker",
            "rationale",
            "benchmark_data_url"
          ]
        }
      },
      "required": [
        "company_and_ticker",
        "event_summary",
        "event_type",
        "dates",
        "analogy_rationale",
        "source_confirmation",
        "historical_data_url",
        "benchmark_details"
      ]
    }
  }
}
```

## 历史事件BRL
```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "BRL Calculation Result",
  "description": "Schema for the output of a Base Rate Library (BRL) calculation for a single historical event.",
  "type": "object",
  "properties": {
    "event_details": {
      "type": "object",
      "description": "Echoes the input event details for reference.",
      "properties": {
        "company_and_ticker": { "type": "string" },
        "event_summary": { "type": "string" },
        "announcement_date": { "type": "string", "format": "date" }
      },
      "required": ["company_and_ticker", "event_summary", "announcement_date"]
    },
    "benchmark_details": {
      "type": "object",
      "description": "回显从输入事件中获取的基准详情。",
      "properties": {
        "name": { "type": "string" },
        "ticker": { "type": "string" },
        "rationale": { "type": "string", "description": "回显的选择理由，说明为何此基准被（在上一阶段）选中。" }
      },
      "required": ["name", "ticker", "rationale"]
    },
    "calculation_results": {
      "type": "object",
      "properties": {
        "t_plus_90_days": {
          "type": "object",
          "properties": {
            "start_date": { "type": "string", "format": "date" },
            "end_date": { "type": "string", "format": "date" },
            "stock_price_start": { "type": "number" },
            "stock_price_end": { "type": "number" },
            "benchmark_price_start": { "type": "number" },
            "benchmark_price_end": { "type": "number" },
            "stock_return_percent": { "type": "number" },
            "benchmark_return_percent": { "type": "number" },
            "excess_return_alpha_percent": { "type": "number" },
            "is_win": { "type": "boolean" }
          },
          "required": ["start_date", "end_date", "stock_price_start", "stock_price_end", "benchmark_price_start", "benchmark_price_end", "stock_return_percent", "benchmark_return_percent", "excess_return_alpha_percent", "is_win"]
        },
        "t_plus_360_days": {
          "type": "object",
          "properties": {
            "start_date": { "type": "string", "format": "date" },
            "end_date": { "type": "string", "format": "date" },
            "stock_price_start": { "type": "number" },
            "stock_price_end": { "type": "number" },
            "benchmark_price_start": { "type": "number" },
            "benchmark_price_end": { "type": "number" },
            "stock_return_percent": { "type": "number" },
            "benchmark_return_percent": { "type": "number" },
            "excess_return_alpha_percent": { "type": "number" },
            "is_win": { "type": "boolean" }
          },
          "required": ["start_date", "end_date", "stock_price_start", "stock_price_end", "benchmark_price_start", "benchmark_price_end", "stock_return_percent", "benchmark_return_percent", "excess_return_alpha_percent", "is_win"]
        }
      },
      "required": ["t_plus_90_days", "t_plus_360_days"]
    },
    "data_sourcing_notes": {
      "type": "string",
      "description": "Any notes regarding data retrieval, such as adjustments made for non-trading days or any data availability issues encountered."
    }
  },
  "required": ["event_details", "benchmark_details", "calculation_results", "data_sourcing_notes"]
}
```
## 锚点方面

```json
{
  "event_class": "<The input event_class_description>",
  "framework_rationale": "<A brief 1-2 sentence explanation of why this framework is appropriate, linking it to the base rate drivers.>",
  "analytical_domains": [
    {
      "domain_name": "<The specific name of the first analytical domain (e.g., 'Target's Vulnerability & Defense Profile')>",
      "domain_description": "<A brief explanation of what this domain covers and why it's a key driver of the outcome.>",
      "key_research_questions": [
        "<The first critical question to guide research in this domain (e.g., 'Does the target have a poison pill or staggered board?')>",
        "<The second critical question (e.g., 'What is the target's current debt/EBITDA vs. peers?')>",
        "...etc."
      ]
    },
    {
      "domain_name": "<The specific name of the second analytical domain (e.g., 'Bidder's Financial & Strategic Capacity')>",
      "domain_description": "<...>",
      "key_research_questions": [
        "<e.g., 'Is the bidder's offer all-cash or stock-based?'>",
        "<e.g., 'What is the stated strategic rationale (e.g., cost synergy, market expansion)?'>"
      ]
    }
    // ... potentially 3-5 domains total
  ]
}
```
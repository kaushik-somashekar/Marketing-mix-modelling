# Marketing Attribution Model

## Project Overview

This project analyzes multi-touch customer journeys and compares multiple marketing attribution models to understand how different channels contribute to conversions and revenue.

It is designed as a realistic **Digital Analytics / Marketing Analytics / Customer Journey Analytics** portfolio project.

## Business Problem

Customers rarely purchase after only one marketing interaction. A typical journey may include:

```text
Paid Social → Organic Search → Paid Search → Email → Purchase
```

The key business question is:

> Which marketing channels should receive credit for conversions and revenue?

Relying only on last-click attribution can over-credit closing channels like Direct, Email, or Paid Search and under-credit upper-funnel channels like Paid Social, Display, Organic Search, or Referral.

## Dataset

The dataset is synthetic but designed to reflect realistic ecommerce customer journey data.

### Files

```text
data/customer_journey_touchpoints.csv
data/conversions.csv
data/data_dictionary.csv
```

### Dataset Size

- 7,000 users
- Multi-touch customer journeys
- Paid and organic marketing channels
- Ecommerce conversions
- Revenue and media cost fields

## Attribution Models Used

1. **First-Touch Attribution**: 100% credit to the first channel.
2. **Last-Touch Attribution**: 100% credit to the final channel.
3. **Linear Attribution**: Equal credit across all touchpoints.
4. **Position-Based Attribution**: 40% first, 40% last, 20% middle.
5. **Time-Decay Attribution**: More credit to touchpoints closer to conversion.

## Folder Structure

```text
marketing_attribution_model/
│
├── data/
│   ├── customer_journey_touchpoints.csv
│   ├── conversions.csv
│   └── data_dictionary.csv
│
├── notebooks/
│   └── marketing_attribution_model.ipynb
│
├── reports/
│   ├── attribution_model_summary.csv
│   ├── channel_performance_summary.csv
│   ├── touchpoint_attribution_output.csv
│   └── figures/
│       ├── attributed_revenue_by_model.png
│       ├── conversion_path_length.png
│       ├── time_decay_roas_by_channel.png
│       └── touchpoints_by_channel.png
│
├── docs/
│   └── project_summary.md
│
├── requirements.txt
├── .gitignore
└── README.md
```

## Key Outputs

| Output | Description |
|---|---|
| `attribution_model_summary.csv` | Revenue, conversions, cost, and ROAS by channel and attribution model |
| `channel_performance_summary.csv` | Touchpoint and conversion summary by channel |
| `touchpoint_attribution_output.csv` | Touchpoint-level attribution credits and revenue allocation |
| `attributed_revenue_by_model.png` | Comparison of attributed revenue across models |
| `time_decay_roas_by_channel.png` | ROAS by channel using time-decay attribution |
| `conversion_path_length.png` | Distribution of number of touchpoints before conversion |
| `touchpoints_by_channel.png` | Channel-level touchpoint volume |

## Business Recommendations

### Paid Search
Strong lower-funnel channel. Prioritize high-intent non-brand and shopping campaigns while monitoring CPA and ROAS.

### Organic Search
Supports discovery and consideration. Invest in SEO category pages, product content, and comparison content.

### Paid Social
Useful for awareness and demand creation. It should be assessed using assisted conversions, not only last-click revenue.

### Email
Strong retention and conversion support channel. Expand basket recovery, loyalty, and lifecycle campaigns.

### Display
May look weak under last-click attribution but supports awareness and retargeting. Reduce broad prospecting waste.

### Affiliate
Audit voucher and cashback partners for incrementality and margin impact.

### Direct
Often captures demand created by earlier marketing activity. Do not over-credit Direct without journey context.

## Tools Used

Python, Pandas, NumPy, Matplotlib, Marketing Attribution, Customer Journey Analytics, ROAS Analysis

## Author

Kaushik Somashekar  
Digital Analyst | Product Analyst | Data Analyst | Aspiring Data Scientist

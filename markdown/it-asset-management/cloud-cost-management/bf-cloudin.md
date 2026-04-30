---
title: Cloud budgets
description: To manage your cloud spend, you can define and monitor custom budget plans. The system compares the plans with billing data to calculate and report on how well budgets are being met. Understanding budget compliance by groups and service accounts can significantly improve oversight and reduce cloud spend.
locale: en-US
release: yokohama
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Cloud budgets

To manage your cloud spend, you can define and monitor custom budget plans. The system compares the plans with billing data to calculate and report on how well budgets are being met. Understanding budget compliance by groups and service accounts can significantly improve oversight and reduce cloud spend.

## How budget analysis works

Each successful Billing download triggers budget refresh automatically. Budget refresh is also triggered manually when a new Budget policy is created.

Budget Forecast jobs use the cost forecast data from the providers and follow this process:

1.  Apply each budget plan to billing data. For more information about plans, see are described in [Create or update a budget policy](manage-cloud-budgets.md#).
2.  Update all Budget Forecast reports.
3.  Repeat the process whenever billing data is updated or a user requests budget reanalysis.

**Note:** If there’s a large number of users, the users may not load correctly or may fail to load to the [Budget view](budget-view-ws.md). See the Knowledge article for more information [KB0866547](https://support.servicenow.com/kb_view.do?sysparm_article=KB0866547).


---
title: Control Tower Home
description: Explore the Home page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-control-tower/ai-control-tower-home-page.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Control Tower dashboard, Explore, Control Tower \(legacy\), Enable AI experiences]
---

# Control Tower Home

Explore the Home page.

The Home page view on the dashboard features recommendations for actions at the top displaying task statuses, pending asset reviews, and newly added AI systems.

The home page displays the [Overview tab in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/overview-tab-in-ai-control-tower.md), [AI strategy tab in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/ai-strategy-ai-control-tower.md), [AI asset inventory tab in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/ai-asset-inventory.md), [Value tab in Super Intelligence Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/aict-value-tab.md), [Risk and compliance tab in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/risk-compliance-tab-aict.md), [AI cases tab in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/ai-cases-tab-aict.md), and [Security &amp; privacy tab in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/security-privacy-tab.md).

**Important:** The [AI strategy tab in Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/ai-strategy-ai-control-tower.md) is available only with Strategic Portfolio Management \(SPM\) Professional license.

Each of these tabs includes widgets, and you can explore the data within each widget in more detail. For instance, the AI system trend widget displays trends based on historical data about AI system deployments. Similarly, the AI risk classification widget shows data according to the default risk classification settings for your skills.

The data appearing on these widgets consists entirely of transactional data. Data is populated once assessments are completed. When Control Tower is first installed, there’s no data available.

**Note:** AI system trend's data is dependent on two types of scheduled job.

-   Control Tower Core Monthly Data Collection
-   Control Tower Core Historical Data Collection job

The Control Tower Core Monthly Data Collection is a job that runs each month to collect data. In Control Tower, this data is displayed on a quarterly basis through aggregation. So, if you configure Control Tower for the first time you don’t see any data.

The Control Tower Core Historical Data Collection job, which is used to gather historical data. If there was any relevant data from previous months, it can be collected using this job. You can run this job manually, as the monthly job only collects data going forward, not from the past.


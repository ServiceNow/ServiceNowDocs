---
title: ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) monitor engagement health agentic workflow
description: Monitor engagement health scores and metric trends. The workflow generates risk signals when a decline is detected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/now-assist-tmt-monitor-health.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Dashboards, Customer success, Use, Customer Success Management]
---

# ServiceNow Otto for Telecommunications, Media, and Technology \(TMT\) monitor engagement health agentic workflow

Monitor engagement health scores and metric trends. The workflow generates risk signals when a decline is detected.

## Monitor engagement health agentic workflow overview

Customer success managers can monitor the health score of up to 10 active engagements and summarize the health trend for the past 6 weeks. Each metric used to calculate the health score is monitored. If a declining pattern is detected, a risk signal or a risk occurrence is generated. A summary indicating the number of risk signals created and the health score range is generated. The Monitor engagement health agentic workflow is triggered weekly based on a predefined schedule and the results are displayed in the [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md).

You can view the risk signals and occurrences that have been created by navigating to the [Risk signals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-create-risk-signal.md) page. For risks created using the agentic workflow, the following field values are displayed:

-   Category: Health declined
-   Creation method: AI generated

The agentic workflow only monitors engagements for which the **AI Health Monitor** flag has been enabled. To configure this workflow, see [Configure agentic workflows for Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-otto-workflows-config.md).

**Parent Topic:**[Dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-dashboards.md)


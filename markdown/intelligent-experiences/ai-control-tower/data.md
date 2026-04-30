---
title: Explore Data
description: Explore the Data section in the Configuration page.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configurations, AI Control Tower dashboard, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Explore Data

Explore the Data section in the Configuration page.

## Data sharing

By default, Data sharing is active. You can opt out to deactivate AI Control Tower and share your data with ServiceNow to improve AI accuracy, enhance user experiences, and gain a better understanding of business needs.

![Data sharing on Configurations screen.](../image/aict-data-sharing.png)

Data sharing helps enhance ServiceNow products, but if you choose to opt out of the ServiceNow data sharing program, you’ll no longer be able to contribute data to improve ServiceNow AI products.

For information on data sharing opt-out, see [Opt out of data sharing](https://www.servicenow.com/docs/bundle/zurich-intelligent-experiences/page/administer/now-assist-admin/task/opt-out-of-data-sharing-for-now-assist.html).

## Data overflow processing

By default, all Now Assist traffic is managed within ServiceNow datacenters. If there are traffic spikes, the system automatically redirects to Microsoft Azure datacenters to maintain performance. You can opt out of this feature to keep all Now Assist traffic exclusively within ServiceNow datacenters. By default, data overflow processing is inactive.

**Note:** The Data sharing and Data overflow processing features are available for a sub-prod instance in read-only mode, when Multi-instance setup is configured and active.

## Data privacy

The Data privacy section displays a read-only view of the data patterns that are enabled to detect and anonymize sensitive information in prompts. Use this view as a quick reference when troubleshooting sensitive data charts. This feature requires the Data privacy plugin to be installed.

The data leak detection anonymization displays a list of data patterns to monitor. You can enable each anonymization by setting it to true.

For more information on how the data is sent and stored, see [User data usage policy for Now Assist](https://www.servicenow.com/docs/bundle/zurich-intelligent-experiences/page/administer/now-assist-admin/concept/user-data-usage-policy-now-assist.html).


---
title: Activate the Self-Service Platform Analytics Solution
description: Activate the content pack plugins or ServiceNow Store application for the Platform Analytics Solution.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Performance Analytics, Extend capabilities, Configure, Customer Service Management]
---

# Activate the Self-Service Platform Analytics Solution

Activate the content pack plugins or ServiceNow Store application for the Platform Analytics Solution.

## Before you begin

Activate the full, subscription version of Performance Analytics on the instance where you are activating this Platform Analytics Solution. You can activate Performance Analytics on a sub-production instance without purchasing a subscription. For more information, see [Activate your Performance Analytics subscription](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_PremiumPerformanceAnalytics.md).

**Note:** The data for the Communities and Virtual Agent tabs on the Self-Service Analytics dashboard are generated when the Communities plugin \(com.sn\_communities\) and Glide Virtual Agent plugin \(com.glide.cs.chatbot\) are activated respectively.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for Self-Service Analytics for Customer Service plugin \(com.snc.pa.self\_service\_analytics\_csm\).

3.  Install the application.

    When you install this application, you also activate the following plugins:

    -   Customer Service \(com.sn\_customerservice\)
    -   Self-Service Analytics PA \(com.snc.pa.self\_service\_analytics\)
    -   Self-Service Analytics Core \(com.snc.self-service\_analytics\_core\)

**Related topics**  


[List of plugins \(Paris\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/list-of-plugins.md)


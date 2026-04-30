---
title: Activate the Platform Analytics Solution for Self-Service Analytics for Customer Service
description: Activate the content pack plugins or ServiceNow Store application for the Platform Analytics Solution.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Platform Analytics Solution for Self-Service Analytics for Customer Service, Extend capabilities, Configuring Customer Service Management, Customer Service Management]
---

# Activate the Platform Analytics Solution for Self-Service Analytics for Customer Service

Activate the content pack plugins or ServiceNow Store application for the Platform Analytics Solution.

## Before you begin

Activate the full, subscription version of Performance Analytics on the instance where you are activating this Platform Analytics Solution. You can activate Performance Analytics on a sub-production instance without purchasing a subscription. For more information, see [Activate your Performance Analytics subscription](https://www.servicenow.com/docs/access?context=c_PremiumPerformanceAnalytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

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


[List of plugins \(Paris\)](https://www.servicenow.com/docs/access?context=list-of-plugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)


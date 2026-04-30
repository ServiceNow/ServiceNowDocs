---
title: Set up RSS feed sources
description: Set up RSS feed sources to efficiently aggregate and monitor updates from multiple websites or content providers in one centralized location. This saves time, ensures you stay informed, and enables automated data retrieval.
locale: en-US
release: zurich
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the RSS feeds infrastructure, Configure, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Set up RSS feed sources

Set up RSS feed sources to efficiently aggregate and monitor updates from multiple websites or content providers in one centralized location. This saves time, ensures you stay informed, and enables automated data retrieval.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **RSS Feeds** &gt; **Feed Sources**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the website that generates and provides the RSS feed. For example, `Consumer Financial Protection Bureau Alerts`.|
    |Connection|Connection that has the details from which the feed would be obtained. For more information, refer to [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).|
    |Active|Option to denote if the source is active. Only active sources are able to fetch the feeds.|
    |Provider|Service or platform that generates and distributes RSS feeds for websites or content creators. For more information, refer to, [Create a connection Alias for third-party provider](https://www.servicenow.com/docs/access?context=create-cnctn-alias&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).|

4.  Select **Submit**.


## Result

The feed source is set up and ready to provide the feed to your instance.


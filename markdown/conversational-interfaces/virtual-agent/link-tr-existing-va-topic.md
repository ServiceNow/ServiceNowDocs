---
title: Link a topic recommendation to an existing Virtual Agent topic
description: Instead of creating a new topic from a topic recommendation, you can link it to an existing topic. This lets Virtual Agent know that you have a topic that addresses the recommendation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/link-tr-existing-va-topic.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Virtual Agent, topic recommendation, link, conversational interfaces]
breadcrumb: [Using Virtual Agent Topic Recommendations, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Link a topic recommendation to an existing Virtual Agent topic

Instead of creating a new topic from a topic recommendation, you can link it to an existing topic. This lets Virtual Agent know that you have a topic that addresses the recommendation.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

If you continue to get recommendations for an active topic after linking it, the topic probably needs improvement.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Topic Recommendations**.

2.  Select the info icon \[Omitted image "icon-info-blue.png"\] Alt text: Info icon. to open the overlay card for a topic that has a **New** status.

3.  At the bottom of the overlay card, select **Here's how to link to an existing topic**.

    Select the link as shown in the following example.

    \[Omitted image "link-new-tr-existing-topic.png"\] Alt text: Select the link at the bottom of the overlay card.

4.  In the dialog box, select a topic in the **Find topic to link** list.

5.  Select **Link topic**.


## Result

The overlay card shows that the recommendation is linked, as well as the date this occurred.

\[Omitted image "tr-linked-topic-overlay-card.png"\] Alt text: The overlay card displays link information at the bottom. It reads, "Linked topic - ITSM - Request - Software - Install," as well as the date it was linked.

If a topic recommendation continues to appear in your analysis results after you linked it to a topic, you may want to revisit the topic to improve its effectiveness.

You can also [unlink a topic recommendation from a Virtual Agent topic.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/unlink-tr-va-topic.md)


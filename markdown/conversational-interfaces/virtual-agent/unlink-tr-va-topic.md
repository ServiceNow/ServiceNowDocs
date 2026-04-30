---
title: Unlink a topic recommendation from a Virtual Agent topic
description: You can unlink a topic recommendation from a topic. This lets you link it to a new or alternate topic.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Unlink, Virtual Agent, topic, recommendation]
breadcrumb: [Using Virtual Agent Topic Recommendations, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Unlink a topic recommendation from a Virtual Agent topic

You can unlink a topic recommendation from a topic. This lets you link it to a new or alternate topic.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

You can either add a recommendation as a new topic or link it to an existing topic. If you link it to an existing topic, you can always unlink it later if you need to. Added topic recommendations create an empty topic that you provide with a workflow, so you can't unlink them using this method.

The following example shows the difference between a linked recommendation and an added recommendation.

![A linked card reads, "Linked to topic on May 5, 2021. An added card reads, "Added on Mar 13, 2021."](../images/tr-linked-topic-card-example.png "Example of linked and added cards in the Topic Recommendations page")

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Topic Recommendations**.

2.  Select the info icon ![Info icon.](../images/icon-info-blue.png) to open the overlay card for a linked topic.

    ![Key details from ITSM Issue - Software - Files - PDF.](../images/tr-unlink-topic.png)

3.  Select **Unlink**.


## Result

Unlinked recommendations are set to **New** status. You can link it to another topic, or add it to Virtual Agent as a new topic.

**Note:** If you added a topic to Virtual Agent for a recommendation, it is not shown as linked, so you can't unlink it. To reset an added recommendation as **New**, delete the topic that was added in Virtual Agent Designer.


---
title: Unlink a topic recommendation from a Virtual Agent topic
description: You can unlink a topic recommendation from a topic. This lets you link it to a new or alternate topic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/unlink-tr-va-topic.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Unlink, Virtual Agent, topic, recommendation]
breadcrumb: [Using Virtual Agent Topic Recommendations, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Unlink a topic recommendation from a Virtual Agent topic

You can unlink a topic recommendation from a topic. This lets you link it to a new or alternate topic.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

You can either add a recommendation as a new topic or link it to an existing topic. If you link it to an existing topic, you can always unlink it later if you need to. Added topic recommendations create an empty topic that you provide with a workflow, so you can't unlink them using this method.

The following example shows the difference between a linked recommendation and an added recommendation.

\[Omitted image "tr-linked-topic-card-example.png"\] Alt text: A linked card reads, "Linked to topic on May 5, 2021. An added card reads, "Added on Mar 13, 2021."

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Topic Recommendations**.

2.  Select the info icon \[Omitted image "icon-info-blue.png"\] Alt text: Info icon. to open the overlay card for a linked topic.

    \[Omitted image "tr-unlink-topic.png"\] Alt text: Key details from ITSM Issue - Software - Files - PDF.

3.  Select **Unlink**.


## Result

Unlinked recommendations are set to **New** status. You can link it to another topic, or add it to Virtual Agent as a new topic.

**Note:** If you added a topic to Virtual Agent for a recommendation, it is not shown as linked, so you can't unlink it. To reset an added recommendation as **New**, delete the topic that was added in Assistant Designer.


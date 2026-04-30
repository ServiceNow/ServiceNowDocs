---
title: Add consumer variables to a remote record producer
description: As a consumer, you can add your own variables to a provider's remote record producer \(RRP\) in your consumer instance using a variable set. Consumer variables help you add extra details to the tasks that you run before syncing a provider task.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Service Exchange for Consumers, Service Exchange for Consumers, Service Exchange]
---

# Add consumer variables to a remote record producer

As a consumer, you can add your own variables to a provider's remote record producer \(RRP\) in your consumer instance using a variable set. Consumer variables help you add extra details to the tasks that you run before syncing a provider task.

## Before you begin

Note the following requirements:

-   You must be using Service Exchange version 2.1.x+.
-   The variables you want to add to the RRP must be included in a variable set. For more details, see [Using variable sets with Remote Record Producers](../concept/service-bridge-v2-variable-sets.md).

Role required: admin, itil, sn\_sb.admin

## About this task

-   You can add only one variable set to a provider's RRP in your consumer instance.
-   The variable set you add in your consumer instance doesn’t automatically synchronize with the provider instance.
-   You cannot edit any provider variables.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Provider Connections**.

2.  On the Provider connection page, open your provider connection by selecting its number link.

3.  In the Remote record producers related list, select the remote record producer.

    You can select only record producers with a Compatibility field value of 2.1.x+.

4.  In the Remote record producers form, in the Consumer variables field, select the variable set you want to add.

5.  Select **Update**.



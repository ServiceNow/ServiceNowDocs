---
title: Add consumer variables to a remote record producer
description: As a consumer, you can add your own variables to a provider's remote record producer \(RRP\) in your consumer instance using a variable set. Consumer variables are useful in a Consumer Pre-Flow for adding additional information to complete a flow.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install and configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Add consumer variables to a remote record producer

As a consumer, you can add your own variables to a provider's remote record producer \(RRP\) in your consumer instance using a variable set. Consumer variables are useful in a Consumer Pre-Flow for adding additional information to complete a flow.

## Before you begin

Note the following requirements:

-   You must be using Service Exchange version 2.1.x+.
-   You have added the necessary variables to a variable set. For more details, see [Using variable sets with Remote Record Producers](../concept/service-bridge-v2-variable-sets.md).

Role required: admin, itil, sn\_sb.admin

## About this task

-   You can add only one variable set to a provider's RRP in your consumer instance.
-   The variable set you add in your consumer instance doesn’t automatically synchronize with the provider instance.
-   You cannot edit any provider variables.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Provider Connections**.

2.  On the Provider connection page, open your provider connection by selecting the relevant number link.

3.  Select the Remote record producers related list.

4.  Select the remote record producer.

    You can select only record producers with a Compatibility field value of 2.1.x+.

5.  In the Remote record producers form, in the Consumer variables field, select the variable set you want to add.

6.  Select **Update**.



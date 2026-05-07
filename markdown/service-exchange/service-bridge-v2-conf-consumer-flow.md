---
title: Service Exchange consumer pre-flows
description: As a consumer, you can control when data should be synced between the provider tasks on the consumer and provider instances.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Service Exchange consumer pre-flows

As a consumer, you can control when data should be synced between the provider tasks on the consumer and provider instances.

## Before you begin

-   Role required: admin
-   A subflow with the sync condition should have been created

Role required: admin

## About this task

You can attach a subflow with a Service Exchange remote record producer and run processes such as approvals, before syncing a task with the provider. When a new provider task is created, the attached subflow is executed before the data is synced between the consumer and provider instances. The subflow must set a field called **Sync** on the Provider task to **true** for the record to sync to the provider. If the remote record producer doesn’t have an attached subflow, provider tasks are immediately synced to the provider instance.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Provider Connections**.

2.  Select a remote record producer for which you want to attach a subflow.

3.  In the Flow field, select the subflow that is to be applied to the provider task.

    Data is synced to the provider instance only if the attached subflow sets the **Sync** flag to **true** on the provider task.

4.  Select **Update**.

    Depending on the conditions defined in the subflow, the provider task is synced to the provider instance.



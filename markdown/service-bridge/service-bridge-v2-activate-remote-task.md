---
title: Activate the remote task definitions record in Service Exchange
description: As a consumer, activate the remote task definitions in your instance so that you can create remote tasks.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Activate entitlements in Service Exchange, Installing and configuring Service Exchange for Consumers, Service Exchange for Consumers, Service Exchange]
---

# Activate the remote task definitions record in Service Exchange

As a consumer, activate the remote task definitions in your instance so that you can create remote tasks.

## Before you begin

Before you \(the consumer\) can activate a remote task definition in your ServiceNow instance, your provider must create it first in their ServiceNow instance. For more information, see [Create remote task definitions in Service Exchange for Providers](service-bridge-v2-create-remote-tasks-defs.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Remote Tasks**.

2.  Click the remote task definition record that you want to activate.

3.  On the remote task definition form, review the Simple Trigger section on the form.

    If you set a simple trigger that matches a task record update, a remote task is automatically created for the task record.

4.  On the **Inbound fields** related tab, review the variables data.

    The provider defines these inbound fields. When you create a remote task, your provider receives the remote task data through these inbound fields. You can modify the **Field label**, **Sync when**, and **Target field** fields.

5.  On the **Outbound fields** related tab, review the variables data.

    Your provider defines these outbound fields. When the provider responds to your remote task, you receive the remote task data through these outbound fields. You can only modify the **Source field** field on these records.

6.  On the **Remote task variables** related tab, review the variables data.

    The remote task variables are created from your inbound fields to be displayed on the remote tasks form.

7.  Click **Activate**.

8.  Verify the mappings of the inbound and outbound variables and click **OK**.

    The pop-up window enables you to verify the inbound and outbound mappings.



---
title: Activate a remote task definition record in Service Exchange
description: As a consumer, activate the remote task definitions in your instance so that you can create remote tasks.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install and configure for consumers, Service Exchange for Consumers, Service Exchange]
---

# Activate a remote task definition record in Service Exchange

As a consumer, activate the remote task definitions in your instance so that you can create remote tasks.

## Before you begin

Before you can activate a remote task definition \(RTD\) in your ServiceNow instance, your provider must create an RTD first in their ServiceNow instance. For more information, see [Create a remote task definition in Service Exchange for Providers](service-bridge-v2-create-remote-tasks-defs.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Provider Connections**.

2.  Select the Number column to navigate to the Provider connection record.

3.  Select the Remote task definition related list, and select an RTD to you want to activate.

4.  On the remote task definition form, review the Simple Trigger section on the form.

    If you set a simple trigger that matches a task record update, a remote task is automatically created for the task record.

5.  On the **Inbound fields** related tab, review the variables data.

    The provider defines these inbound fields. When you create a remote task, your provider receives the remote task data through these inbound fields. You can modify the **Field label**, **Sync when**, and **Target field** fields.

6.  On the **Outbound fields** related tab, perform the following actions.

    1.  Review the variables data.

        Your provider defines these outbound fields. When the provider responds to your remote task, you receive the remote task data through these outbound fields. You can only modify the **Source field** on these records.

    2.  Select the **Sync pre-existing entries** option to enable synchronization of all existing comments to the target task when a connection is established.

        If enabled, any comments made prior to the connection gets included in the sync process when a remote task is created.

        **Note:** This feature is only available for Service Exchange version 2.2.x.

7.  On the **Remote task variables** related tab, review the variables data.

    The remote task variables are created from your inbound fields to be displayed on the remote tasks form.

8.  Select **Activate**.

9.  Verify the mappings of the inbound and outbound variables and select **OK**.

    The pop-up window enables you to verify the inbound and outbound mappings.



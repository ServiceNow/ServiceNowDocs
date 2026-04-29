---
title: Activate the remote task definitions
description: Activate the remote task definitions published by the provider on your instance so that your provider can fulfill your Zero Touch Refresh requests.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Exchange configuration for Zero Touch Refresh, Manage refresh of assets using Zero Touch Refresh, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Activate the remote task definitions

Activate the remote task definitions published by the provider on your instance so that your provider can fulfill your Zero Touch Refresh requests.

## Before you begin

The Service Exchange application must be installed on your instance. For more information, see [Install Service Bridge for customers](https://www.servicenow.com/docs/access?context=install-service-bridge-v2-customer&version=australia&pubname=australia-service-bridge&ft:locale=en-US).

Before you can activate a remote task definition on your ServiceNow instance, your provider must create and publish it. For more information, see [Trigger the assignment of a remote task](create-rtd-for-providers.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Bridge** &gt; **Customer** &gt; **Remote Task Definitions**.

2.  Select the remote task definition record.

3.  On the Remote Task Definition form, in the Simple Trigger section, set the trigger condition as **Model is not empty**.

    Remote tasks are automatically created when records with values in the **Model** field are added to the Zero Touch Refresh Fulfillment Request \[sn\_itam\_ztr\_fulfillment\_req\] table.

4.  Select **Save**.

5.  Verify the data on the **Inbound fields** tab, the **Outbound fields** tab, and the **Remote task variables** tab.

    The provider defines these values. When you create a remote task, the provider receives the remote task data through the inbound fields and responds with the remote task data through the outbound fields.

6.  Select **Activate**.

7.  In the pop-up window, verify the mappings of the inbound and outbound variables and select **OK**.



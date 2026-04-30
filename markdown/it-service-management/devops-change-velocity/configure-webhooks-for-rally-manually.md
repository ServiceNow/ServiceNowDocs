---
title: Configure webhooks for Rally manually
description: Configure webhooks for Rally to send sync notifications to the DevOps Change Velocity application.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Rally, Integrate, DevOps Change Velocity, IT Service Management]
---

# Configure webhooks for Rally manually

Configure webhooks for Rally to send sync notifications to the DevOps Change Velocity application.

## Before you begin

Role required: sn\_devops.admin or sn\_devops.tool\_owner in DevOps Change Velocity.

## About this task

To send inbound events to a ServiceNow instance for Rally, you must use the following API endpoint structure: `<instance_url>/api/sn_devops/v2/devops/tool/plan?toolId=<toolId>&&ni.nolog.token=<token>`

## Procedure

1.  In DevOps Change Velocity, in the Configure to send data playbook activity, select **Configure manually** when configuring the tool instance to send data.

    ![Configure webhooks for Rally](../image/configure-webhook-rally.png)

    **Note:** You can also access manual configuration from the Jira tool record in DevOps Change Velocity. From the tool record, select **Configure** &gt; **Configure manually**.

2.  Select **Copy** in the appropriate field to copy the value to your clipboard.

    The field label changes to **Copied**, but you can copy multiple times.

3.  Use the following API endpoint structure to send inbound events to your ServiceNow instance. `<instance_url>/api/sn_devops/v2/devops/tool/plan?toolId=<toolId>&&ni.nolog.token=<token>`.

    For more information, see [Creation of webhooks to send inbound events to DevOps Change Velocity using token](create-webhooks-to-send-inbound-events-to-devops-change-velocity-using-token.md).


**Parent Topic:**[Rally integration with DevOps Change Velocity](../concept/rally-devops-integration.md)


---
title: Configure webhooks for Rally manually
description: Configure webhooks for Rally to send sync notifications to the DevOps Change Velocity application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-change-velocity/configure-webhooks-for-rally-manually.html
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "configure-webhook-rally.png"\] Alt text: Configure webhooks for Rally

    **Note:** You can also access manual configuration from the Jira tool record in DevOps Change Velocity. From the tool record, select **Configure** &gt; **Configure manually**.

2.  Select **Copy** in the appropriate field to copy the value to your clipboard.

    The field label changes to **Copied**, but you can copy multiple times.

3.  Use the following API endpoint structure to send inbound events to your ServiceNow instance. `<instance_url>/api/sn_devops/v2/devops/tool/plan?toolId=<toolId>&&ni.nolog.token=<token>`.

    For more information, see [Creation of webhooks to send inbound events to DevOps Change Velocity using token](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/create-webhooks-to-send-inbound-events-to-devops-change-velocity-using-token.md).


**Parent Topic:**[Rally integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/rally-devops-integration.md)


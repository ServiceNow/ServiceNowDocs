---
title: Add a service to SRM
description: Create or add an existing service to your instance so that alerts and incidents on that service are available to your teams within SRM.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Working with SRM services, Using Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Add a service to SRM

Create or add an existing service to your instance so that alerts and incidents on that service are available to your teams within SRM.

## Before you begin

Role required: Responder, Manager, or Administrator

## About this task

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You are taken to your SRM homepage.

    **Note:** If you have other SOW applications, and depending on your assigned roles, that homepage may not be the SRM homepage. It is the SOW homepage instead, with SRM alerts and incidents included in your metrics. In that case, to view SRM specific areas, select SRM modules from the left navigation pane.

2.  Use one of the following methods to open the Tell us about the service form and select or fill in the fields.

    -   On your **Home** page, in the Getting started section, under Setup up your service, select **Add a service**.
    -   On the Services page \(![services](../image/icon-sr-services.png)\), select **Add a service**.
3.  Add a new service or register an existing one.

<table id="choicetable_m3m_brg_n1c"><thead><tr><th align="left" id="d96567e113">

Option

</th><th align="left" id="d96567e116">

Steps

</th></tr></thead><tbody><tr><td id="d96567e122">

**Add a new service**

</td><td>

1.  In the **New or existing** field, select **Create a new service in Service Reliability Management**.
2.  On the form, fill in the fields.

For more information on the field descriptions, see [Add service form](../reference/sr-add-service-form.md).

3.  Select **Next**.


</td></tr><tr><td id="d96567e164">

**Register an existing service**

</td><td>

1.  In the **New or existing** field, select **Associate existing CMDB services to Service Reliability Management**.
2.  Select one or more services.
3.  Select **Next**.


</td></tr></tbody>
</table>4.  In the Assign a team step, fill in the fields.

    -   In the **Service owner** field, select the user who will own the services.
    -   In the **Support Group** field, select a team that will monitor services.

        To assign the services to a new team, select **Create a new team**.

        For more information, see [Add an SRM team](sr-create-team.md).

5.  Select **Add service\(s\)**.


## Result

If approvals aren’t enabled, finish setting up the service by going to its service record page or do it later.

If approvals are enabled, your service request is sent for approval. After its approved, the service will appear in the Services list.

## What to do next

You can set up your service to start tracking its reliability.

-   **[Working with SRM integrations](../concept/sr-work-integrations.md)**  
Integrations within SRM provide the ability to use monitoring and collaborating tools to manage alerts and incidents efficiently by the users. SRM integrations are added or created within Services only.

**Parent Topic:**[Working with SRM services](../concept/sr-work-services.md)


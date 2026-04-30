---
title: Customize team approval settings in SRM
description: Add an approval process to your Service Reliability Management teams for governance.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Customize team approval settings in SRM

Add an approval process to your Service Reliability Management teams for governance.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  Under **Governance and autonomy**, select **Team governance**.

3.  Depending on your organization's preference, you can choose to add an approval process when SRM admins, managers, or responders request to create a team in SRM.

4.  Select the **Update value with sys\_id** link.

5.  In the new window, select the link to edit the record.

    ![Select the link to edit the record and set the approving team sys ID in the property.](../image/sr-team-approval-sys-prop.png)

6.  Replace the system property **Value** with the `sys_id` of the assignment team.

    1.  Navigate to the Group record for the team you want.

    2.  Open the record

    3.  Right-click in the header \(or use the keyboard shortcut\) and select **Copy sys\_id**.

        ![Add the appropriate flow to the fulfillment of the item.](../image/sr-team-copy-sys-id.png)

    4.  Return to the System Property record and paste the **sys\_id** in the Value field.

    5.  Add the appropriate flow to the fulfilment of the item, which is SRM - create team approval required.

    6.  Select **Update.**

        This action initiates the approval process and assigns approval to the team responsible for approving new teams.

        **Note:** Approvals take two steps. First the request is approved, which shows up in the request record in the **Stage** field, then the request remains **Pending** until the request item is approved in the **Request** record.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Customize service approval settings in SRM](sr-add-approval-services.md)

**Next topic:**[Import teams to Service Reliability Management](sr-import-teams.md)


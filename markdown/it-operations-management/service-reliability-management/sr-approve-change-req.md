---
title: Approve a change request for SRM
description: Approve a service change request in Service Reliability Management \(SRM\) to allow the requested action to proceed.REVISE FOR SRM
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Approve a change request for SRM

Approve a service change request in Service Reliability Management \(SRM\) to allow the requested action to proceed.

## Before you begin

Only open change requests are available on the **Reliability tasks** page.

Role required: SRM approval team or admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

    You're taken to your SRM Home page.

    **Note:** If you use other Service Operations Workspace \(SOW\) applications, you may see the SOW Home page instead of the SRM Home page. The SOW Home page includes SRM alerts and incidents in its metrics.

2.  From the primary navigation, select **Reliability tasks** \(![Reliability tasks icon](../image/icon-sr-reliability-tasks.png)\).

3.  Select the **Changes** tab.

4.  Select a change request and then select the **Details** tab.

5.  On the **State** field, select the list and select **Approved**.

6.  Select **Save**.

    The change request state updates from `Assess` to `Approved`.

    On approval, the new service is created and added to the SRM team. The owner is set to the person shown in the Assigned to field. And the Managed by group is set to the SRM team associated with the assignee.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Related topics**  


[Install Service Reliability Management from Admin Center or ServiceNow Store](sr-install-sr-store-app.md)

[Assign an administrator to Service Reliability Management](sr-assign-admins.md)

[Activate teams and services in SRM](sr-activate-teams-and-services-in-srm.md)

[Customize service approval settings in SRM](sr-add-approval-services.md)

[Customize team approval settings in SRM](sr-add-approval-teams.md)

[Configure error budget actions for breached SRM SLOs](sr-configure-error-budget.md)

[Configure fields for escalation triggers](srm-configure-trigger-fields.md)

[Configure Twilio to send notifications in SRM](sr-add-twilio-key.md)

[Install the Alert Automation application](sr-install-aa-store-app.md)


---
title: Customize service approval settings in SRM
description: Add an approval process to your services for governance.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Customize service approval settings in SRM

Add an approval process to your services for governance.

## Before you begin

Role required: srm\_admin or admin

## About this task

Require approval when Service Reliability Management \(SRM\) admins, managers, or responders request to create or add a service in SRM.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Configurations**.

2.  Select **Service Reliability Management** &gt; **Governance and autonomy** &gt; **Service governance**.

3.  Choose one or both processes by selecting the relevant check box.

    Approval requirement types:

    -   Approval required when creating a new service:

        Requires approval when creating a service in SRM, and assigns it to the team responsible for new services.

    -   Approval required when associating an existing Configuration Management Database \(CMDB\) service:

        Requires approval to add an existing service to SRM, and assigns it to the team responsible for existing services.

4.  Enter or select the team responsible for approvals.

5.  Select **Save**.

    This action initiates the approval process and assigns approval to the team responsible for approving the new service.

    **Note:** Approvals take two steps. First, the request is approved, which appears in the **Stage** field of the request record. Next, the request remains **Pending** until the request item is approved in the **Request** record.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Related topics**  


[Install Service Reliability Management from Admin Center or ServiceNow Store](sr-install-sr-store-app.md)

[Assign an administrator to Service Reliability Management](sr-assign-admins.md)

[Activate teams and services in SRM](sr-activate-teams-and-services-in-srm.md)

[Customize team approval settings in SRM](sr-add-approval-teams.md)

[Configure error budget actions for breached SRM SLOs](sr-configure-error-budget.md)

[Approve a change request for SRM](sr-approve-change-req.md)

[Configure fields for escalation triggers](srm-configure-trigger-fields.md)

[Configure Twilio to send notifications in SRM](sr-add-twilio-key.md)

[Install the Alert Automation application](sr-install-aa-store-app.md)


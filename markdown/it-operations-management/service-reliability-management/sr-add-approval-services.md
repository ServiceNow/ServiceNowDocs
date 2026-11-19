---
title: Customize service approval settings
description: Add an approval process to your services for governance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-reliability-management/sr-add-approval-services.html
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Customize service approval settings

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


**Parent Topic:**[Configuring Service Reliability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-reliability-management/configuring-service-reliability-management.md)

**Related topics**  


[Install Service Reliability Management from Admin Center or ServiceNow Store]()

[Assign an administrator to Service Reliability Management]()

[Activate teams and services in SRM]()

[Customize team approval settings]()

[Configure error budget actions for breached SRM SLOs]()

[Approve a change request for SRM]()

[Configure fields for escalation triggers]()

[Configure Twilio to send notifications in SRM]()

[Install the Alert Automation application]()


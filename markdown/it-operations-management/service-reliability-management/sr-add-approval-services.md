---
title: Customize service approval settings in SRM
description: Add an approval process to your services for governance.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Customize service approval settings in SRM

Add an approval process to your services for governance.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  Under **Governance and autonomy**, select **Service governance**.

3.  Depending on your organization's preference, you can choose to add an approval process when SRM admins, managers or responders request to create a service in SRM or associate an existing service with SRM.

4.  Select one or both processes by selecting the appropriate check box.

    Approval requirement types:

    -   Approval is required when creating a new service in SRM:

        Requires approval when creating a new service for SRM, and assigns it to the team responsible for new services.

    -   Approval required when associating an existing CMDB service within SRM:

        Requires approval to add an existing service to SRM, and assigns it to the team responsible for existing services.

5.  Enter or select the team responsible for approvals.

6.  Select **Save**.

    This action initiates the approval process and assigns approval to the team responsible for approving the new service.

    **Note:** Approvals take two steps. First the request is approved, which shows up in the request record in the **Stage** field, then the request remains **Pending** until the request item is approved in the **Request** record.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Activate teams and services in SRM](sr-activate-teams-and-services-in-srm.md)

**Next topic:**[Customize team approval settings in SRM](sr-add-approval-teams.md)


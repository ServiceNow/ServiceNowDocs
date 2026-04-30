---
title: Remove a service from SRM
description: Remove a service from Service Reliability Management \(SRM\) when you no longer need to track or monitor its reliability.
locale: en-US
release: zurich
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2025-10-22"
reading_time_minutes: 2
breadcrumb: [Working with SRM services, Using Service Reliability Management, Service Reliability Management, ITOM AIOps, IT Operations Management]
---

# Remove a service from SRM

Remove a service from Service Reliability Management \(SRM\) when you no longer need to track or monitor its reliability.

## Before you begin

SRM administrators can remove any service from SRM. SRM managers can remove only the services assigned to their teams.

**Note:** Administrators and SRM administrators have a delete option on service pages. That option deletes the service from both SRM and the Configuration Management Database \(CMDB\). The remove option, described below, only removes the service from SRM.

Role required: srm\_manager or srm\_admin

## About this task

Remove one or more services from SRM when you no longer need to track their reliability. Removing a service from SRM does the following:

-   Removes the service from SRM views, including the Service page and Service reliability dashboard.
-   Deletes all draft service level objectives \(SLOs\) associated with the service. Those SLOs aren't recoverable.
-   Retires all active SLOs associated with the service. Those SLOs are no longer active but remain visible in SRM.

Removing a service from SRM doesn't affect the service reliability tasks, such as alerts, change tasks, or incidents. The service also remains in the CMDB, and you can add it back to SRM at any time.

**Note:** The following procedure shows how to remove services from SRM using the Services page. You can also remove services using the Teams page by selecting a team and then the **Services managed** tab.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation, select **Services**.

3.  Point to a service you want to remove, and then select its check box.

    You can select one or more services.

4.  Select **Remove**.

5.  In the dialog, review the details about the affected SLOs and then select **Remove service**.

    The page displays `<service-name> removed from SRM`. The service no longer appears in the SRM application, but it remains in the CMDB. You can add it back to SRM at any time.

    **Note:** If you receive an error when removing a service, see [Troubleshoot SRM](../reference/srm-troubleshoot.md).


## What to do next

To learn how to monitor and manage services that remain in SRM, see [Working with SRM services](../concept/sr-work-services.md). To add a service that you want to monitor or that was removed by mistake, see [Add a service to SRM](sr-add-service.md).

**Parent Topic:**[Working with SRM services](../concept/sr-work-services.md)


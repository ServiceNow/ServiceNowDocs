---
title: Activate teams and services
description: Follow this step only if you are on version 1.5.0 of Service Observability. Assign existing teams to Service Observability so they can view the data returned by the Configuration Management Database \(CMDB\) on those pages. Activate the services in the CMDB for use in Service Observability.
locale: en-US
release: australia
product: Service Observability
classification: service-observability
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Service Observability, Service Observability, ITOM AIOps, IT Operations Management]
---

# Activate teams and services

Follow this step only if you are on version 1.5.0 of Service Observability. Assign existing teams to Service Observability so they can view the data returned by the Configuration Management Database \(CMDB\) on those pages. Activate the services in the CMDB for use in Service Observability.

## Before you begin

-   Users assigned to a group that manage the activated services.
-   Services that you want to monitor in Service Observability should be configured in the CMDB.

Role required: system admin

## About this task

**Note:** Follow this step only if you are on version 1.5.0 of Service Observability.

Teams are used in both Service Reliability Management and Service Observability to give existing roles and groups the ability to view CMDB data on the **Overview** and **Observability** tabs.

The services that you want to monitor in Service Observability must be activated. Activation enables you to map data from an observability monitoring instance to that service and then view that service's related data on the **Overview** and **Observability** tabs.

**Note:** Teams and services activated for Service Observability are also activated for Service Reliability Management \(SRM\). Service Observability admins can create a single service. For more information, see [Add a service to SRM](../../service-reliability/task/sr-add-service.md). When Service Observability admins create a single service, it's automatically activated for Service Observability and SRM. For more information, see [Service Reliability Management](../../service-reliability/reference/sr-landing-page.md).

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations** and choose the **Service Operations Management** card.

2.  Navigate to **Service Operations Management** &gt; **Assign and activate** &gt; **Activate teams and services**.

3.  Choose **Activate teams and services**.

4.  Select the assignment groups that you want as teams in Service Observability and then select **Activate**.

    Only teams that haven't already been assigned are displayed.

5.  In the modal, select **Confirm**.

6.  In the Service class drop-down menu, select a CMDB service type.

7.  From the list of services, select which services to activate for Service Observability and select **Activate**.

8.  In the modal, select a support team for the services and choose **Confirm**.

    You now have services that can be monitored in Service Observability


## What to do next

1.  [Connect a Service Observability data source](../task/connect-an-observability-data-source.md)
2.  [Create and manage data mappings](../task/create-and-manage-observability-data-mappings.md)

**Parent Topic:**[Configuring Service Observability](configuring-service-observability.md)


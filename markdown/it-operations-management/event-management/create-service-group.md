---
title: Create a service group
description: Create service groups to combine similar services. Organize services by groups to perform actions simultaneously on multiple services and to control user access to services.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create a service group

Create service groups to combine similar services. Organize services by groups to perform actions simultaneously on multiple services and to control user access to services.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

Service groups are a way to organize and group services based on the application services or technical services they impact. Instead of looking at individual service from different infrastructure components \(like servers, databases, or applications\), Service groups help consolidate them under the umbrella of a service group. Application service groups enable faster identification of alert impact. Service groups appear in the **Group by** option on the Service Operations Workspace dashboard.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Services** &gt; **Service Groups**.

2.  Click **New**.

3.  In the **Name** field, enter the name of the new service group.

4.  In the **Parent Group** field, enter the name of another group in which to embed the new group.

    Users with access to a parent service group automatically have access to all its child groups.

5.  Click **Submit**.


**Parent Topic:**[Application services in Event Management](../concept/application-service-event-management.md)

**Related topics**  


[Assign a role to a service group](t_EMAssignRoleSvcGroup.md)

[Group application services](../../service-mapping/task/organizing_services-into-groups.md)


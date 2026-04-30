---
title: Manually create an application service in Event Management
description: You can manually create an application services. Event Management can use application services to monitor service performance and identify health issues.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Application services in Event Management, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Manually create an application service in Event Management

You can manually create an application services. Event Management can use application services to monitor service performance and identify health issues.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

An application services is a set of interconnected applications and hosts which are configured to offer a service to the organization. Application services can be internal, like an organization email system or customer-facing, like an organization website. Use application services to organize, maintain, and monitor services in your organization.

Application services do not support these CI types:

-   cmdb\_ci\_endpoint
-   cmdb\_ci\_translation\_rule
-   cmdb\_ci\_config\_file
-   cmdb\_ci\_qualifier
-   cmdb\_ci\_application\_cluster

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Services** &gt; **Application Services**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Enter a unique application service name.|
    |Owned by|Specify an owner who is responsible for this application service in the organization|
    |Add entry points:| |
    |CI Type|Select the CI type \(CI class\) for the CI you are adding. Every CI belongs to a CI type which contains a set of attributes configured for this kind of CI, for example, cmdb\_ci\_appl for applications.|
    |CI Name|Select the CI from the list of CIs of the selected CI type.|

    The CI type list includes only allowed CI types. For example, you cannot add an application cluster.

4.  Click **Submit**.


## What to do next

For details on grouping application services, see [Group application services](../../service-mapping/task/organizing_services-into-groups.md).

For details on controlling user access to application services, see [Control user access to application services](../../service-mapping/task/control-user-access-to-business-services.md).

**Parent Topic:**[Application services in Event Management](../concept/application-service-event-management.md)


---
title: Apply scope to a service in Service Portfolio Management
description: Define the limits of a service with scope details to grant or deny specific service views. Out of Scope items define what a service cannot provide and In Scope items define what a service provides. For example, nightly backups may be In Scope for the Desktop Support service, but Out of Scope for the Disaster Recovery service.
locale: en-US
release: xanadu
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Apply scope to a service in Service Portfolio Management

Define the limits of a service with scope details to grant or deny specific service views. Out of Scope items define what a service cannot provide and In Scope items define what a service provides. For example, nightly backups may be In Scope for the Desktop Support service, but Out of Scope for the Disaster Recovery service.

## Before you begin

Role required: portfolio\_admin or service\_editor

## About this task

The In Scope and Out of Scope definitions appear in the service catalog page that users see when they access the service catalog.

To view the list of scope entries in your system, enter `service_scope.list` in the navigator and press the Enter key.

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Services**.

2.  Select the name of a service for which you want to define scope.

    Only a parent service can have scope.

3.  In the In Scope or Out of Scope related list, select **New** to create a new definition or select **Edit** to add the scope to the In Scope or Out of Scope list for the service.

    Configure scope with anything that is pertinent to the service and helps define the limits of the service.

4.  Give the scope item a descriptive name and provide details in the **Description** field.

5.  Select **Submit**.


**Parent Topic:**[Using Service Portfolio Management](../concept/SPM2-using.md)


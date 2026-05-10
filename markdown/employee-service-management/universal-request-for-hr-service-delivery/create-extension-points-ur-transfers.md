---
title: Create an extension point for post-processing of transfers
description: Create a scripted extension point to perform additional actions after the cross-department transfer of a primary ticket in the Universal Request application. You can change the sample extension point to copy any additional information from the previous primary ticket's child entities.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Create an extension point for post-processing of transfers

Create a scripted extension point to perform additional actions after the cross-department transfer of a primary ticket in the Universal Request application. You can change the sample extension point to copy any additional information from the previous primary ticket's child entities.

## Before you begin

Role required: admin

## About this task

When a primary ticket of a Universal Request is transferred, the current mapping configuration only copies the information from the primary ticket to the destination ticket. However, if you want additional actions to be performed after the cross-department transfer of the primary ticket, you can create a scripted extension point implementation for the **DepartmentTransferPostProcessor** extension point. A sample **DepartmentTransferPostProcessor** extension point, which is based on your business requirements, is provided for you to modify and use.

## Procedure

1.  Navigate to **All** **&gt;System Extension Points** **&gt;Scripted Extension Points**.

2.  In the search bar, search for **sn\_uni\_req.DepartmentTransferPostProcessor**.

3.  Create your department-specific extension point by selecting **Create implementation**.

    For more information about using extension points, see [Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md).


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)


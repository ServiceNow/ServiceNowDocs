---
title: Create extension points for departments
description: Create a scripted extension point to create your department specific primary ticket during cross-department ticket transfers. Using extension point enables you to create a primary ticket type as per the extension point definition.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure service to use Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Create extension points for departments

Create a scripted extension point to create your department specific primary ticket during cross-department ticket transfers. Using extension point enables you to create a primary ticket type as per the extension point definition.

## Before you begin

Role required: admin

## About this task

When configuring your department for Universal Request, to use transfer to other department capability, create scripted extension points and add them to the script includes of the application code. A sample **CreateDepartmentTicket** extension point is provided for you to modify and use.

**Note:** For a better user experience, you can choose to use the Mapping configuration to define and configure fields that must be copied to the end-points for ticket transfers and creation. For more information, see [Configure mappings](ur-transfer-map-config.md).

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for `sn_uni_req.CreateDepartmentTicket`.

3.  On the form banner, click the link **here** to edit the record.

4.  Click **Create Implementation** in the related list to create your department specific extension point script.

    For more information, see Using extension points to extend application functionality.


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)


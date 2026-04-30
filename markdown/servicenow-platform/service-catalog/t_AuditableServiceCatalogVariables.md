---
title: Audit service catalog variables
description: Audit the variables so that the audit history records all changes to the named variables.
locale: en-US
release: yokohama
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service catalog variables, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Audit service catalog variables

Audit the variables so that the audit history records all changes to the named variables.

## Before you begin

Role required: admin

## About this task

Auditing is enabled by default for service catalog variables.

These changes are displayed in:

-   The requested item history for all variables associated with the item.
-   The catalog task history for all variables that are used by the task.

This auditing allows service catalog administrators to view a full history of changes to variables that can affect the parent record, including their creation.

**Note:** Unnamed variables are not audited.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **Service Catalog**.

2.  Locate the line **Audit changes to Service Catalog Variables**.

3.  Select the **Yes** check box to enable auditing.


**Parent Topic:**[Service catalog variables](../concept/c_ServiceCatalogVariables.md)


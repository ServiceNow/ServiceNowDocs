---
title: View work order details from a change request using the CSM Configurable Workspace
description: View or track the progress of a work order in the associated change request from CSM Configurable Workspace.
locale: en-US
release: australia
product: Field Service Integrations
classification: field-service-integrations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration with Change Management, Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# View work order details from a change request using the CSM Configurable Workspace

View or track the progress of a work order in the associated change request from CSM Configurable Workspace.

## Before you begin

Enable the activity function using the ChangeWorkOrderIntegration extension point. For more information, see [Using an extension point to synchronize work orders with change requests](../reference/using-extention-point-for-chnge-mngmnt.md).

Role required: itil, wm\_admin, and sn\_change\_read

## About this task

ITIL agents can view the progress of a work order directly from a related change request. The change request tracking is updated whenever the following updates are made to the work order or related work order tasks:

-   Work notes added to the task
-   State of the task is updated

## Procedure

1.  Log in to CSM Configurable Workspace.

2.  Click the **List** icon \(![List icon.](../../../administer/workspace/image/list-icon-black.png)\).

3.  In the Lists panel, navigate to **Change** &gt; **All**

4.  Open the change request for which you want to track the progress.

5.  Click the Details related list.

6.  View the work order progress in the **Activity** section.



---
title: Set the group for a CI or an entire class of CIs
description: Synchronize group assignment attributes on entire CI classes and individual CIs using the CI Class Manager.
locale: en-US
release: xanadu
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using dynamic CI groups, Navigate, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set the group for a CI or an entire class of CIs

Synchronize group assignment attributes on entire CI classes and individual CIs using the CI Class Manager.

## Before you begin

Role required: itil and itil\_admin

## About this task

Set the **Managed by group** attribute for a specific class in the CI Class Manager. All CIs within the class will have their **Managed by group** field populated based on the value specified in the CI Class Manager. With this method, the **Managed by group** setting is applied only to the CIs that aren’t associated with a technology management offering. For CIs that are managed by a technology management offering, the **Managed by group** field is first synchronized with its dynamic CI group. The field is then synchronized with the CIs in the dynamic CI group, overwriting the entry from the CI Class Manager.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to expand the CI Classes list, select a class to display details for, and then select **Basic Info**.

3.  Specify the value in the **Managed by Group** attribute and select **Save**.

4.  To verify the change, select **CI List**.

    The change should be applied to the **Managed by Group** attribute of all CIs of this class unless they are associated with a technical service offering. The change is applied only to the CIs in the class and not to the sub classes under a CI.


## Example

As an itil\_admin, you can define a user group that can manage all CIs belonging to a specific class by following these steps:

1.  Navigate to the CI Class Manager and select the **Linux Server** class in the list.
2.  Select **Basic Info** and, in the Managed By Group attribute, select **sys\_user\_group** and then select **Save**.
3.  To verify that the attribute was updated, select **CI List** and navigate to the Linux Server class. You will see that the **Managed By Group** attribute has been updated to **sys\_user\_group**.

**Parent Topic:**[Synchronizing group assignment attributes](../concept/csdm-data-synchronize.md)


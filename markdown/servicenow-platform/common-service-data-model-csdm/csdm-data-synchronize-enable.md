---
title: Set the group for a CI or an entire class of CIs
description: Synchronize group assignment attributes on entire CI classes and individual CIs using the CI Class Manager.
locale: en-US
release: australia
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Dynamic CI group and service type, Implement, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set the group for a CI or an entire class of CIs

Synchronize group assignment attributes on entire CI classes and individual CIs using the CI Class Manager.

## Before you begin

Role required: itil and itil\_admin

## About this task

**Note:** The **Managed by Group** setting identifies the group that manages a CI class \(ensuring that it is complete and correct\). It might or might not be the same group as repairs an individual CI.

You can streamline approval of CMDB Data Manager policies by populating the **Manage by Group** attribute of CIs that you plan to target in policies. Use the CI Class Manager to populate the attribute for an entire class in a single synchronization operation. If the **Managed by Group** attribute isn't populated for a CI, then the approval process is directed to the administrator.

Set the **Managed by group** attribute for a specific class in the CI Class Manager. All CIs within the class will have their **Managed by group** field populated based on the value specified in the CI Class Manager. With this method, the **Managed by group** setting is applied only to the CIs that aren’t associated with a Technology management offering. For CIs that are managed by a Technology management offering, the **Managed by group** field is first synchronized with its dynamic CI group. The field is then synchronized with the CIs in the dynamic CI group, overwriting the entry from the CI Class Manager.

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

2.  Select **Hierarchy** to expand the CI Classes list, select a class to display details for, and then select **Basic Info**.

3.  Specify the value in the **Managed by Group** attribute and select **Save**.

4.  To verify the change, select **CI List**.

    The change should be applied to the **Managed by Group** attribute of all CIs of the class unless they are associated with a Technology management offering. The change is applied only to the CIs in the class and not to the sub classes under a CI.


## Example

In this example, you define a user group that can manage all CIs belonging to the **Linux Server** class:

1.  Navigate to the CI Class Manager and select the **Linux Server** class in the list.
2.  Select **Basic Info** and, in the **Managed By Group** attribute, select **sys\_user\_group** and then select **Save**.
3.  To verify that the attribute was updated, select **CI List** and navigate to the Linux Server class. You will see that the **Managed By Group** attribute has been updated to **sys\_user\_group**.

**Parent Topic:**[Matching the usage of dynamic CI groups to service type](../concept/csdm-dynamic-ci-groups-by-service.md)

**Related topics**  


[Synchronizing group assignment attributes](../concept/csdm-data-synchronize.md)

[Synchronize user groups for a technology management offering](csdm-enable-tso.md)


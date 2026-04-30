---
title: Create business capability and relate the capability with an application - Legacy
description: Business capabilities are the abilities of an organization to do an activity to fulfill its business goals. Align your organization goals with business capabilities by creating capabilities.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create business capability and relate the capability with an application - Legacy

Business capabilities are the abilities of an organization to do an activity to fulfill its business goals. Align your organization goals with business capabilities by creating capabilities.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy business capability module is moved to the Enterprise Architecture Workspace. To learn more, see [Exploring business capabilities](../concept/eaw-concept/eaw-business-capabilities.md).

Role required: sn\_apm.apm\_admin

## About this task

Use the Business Capability form to create and update a business capability. If you add a new capability, update an existing capability, delete a capability at a leaf node level, then the levels of all the capabilities and the leaf node in that hierarchy must be updated accordingly. Select the **Update Capability Level and HierarchyID** related link to update the levels in the hierarchy so that the capability map reflects the updates. The **Leaf Node** and the **Level** fields are rendered uneditable to you, yet you can view the level of the capability if it is at the leaf node and its position in the hierarchy.

Following are the conditions to update or delete a capability:

-   When you add a capability, the level of the new capability in the hierarchy is automatically assigned based on the level of the parent capability that is attached.
-   If a parent capability is updated in the hierarchy, then the levels of all its child capabilities are recalculated. Otherwise, a capability can only be updated of its name, description, or parent.
-   While adding or updating a capability the total number of levels can’t exceed more than six in the hierarchy. For example, the levels can be from 0 to 5, where 0 is the root level.
-   You can delete capabilities that are at the leaf node level only. Or, a capability that does not have a child capability of its own.
-   Don’t create circular relationships. In creating a parent capability, a child capability can’t be its parent.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Business Capabilities**.

    You can also navigate to **Organization** &gt; **Business Capabilities**.

2.  Select **New**.

3.  Fill in the form fields.

    For field information, see [Business capability form](../reference/business-capability-form.md).

4.  Select **Submit**.

    If a root or a level-0 capability is created or if the parent field of a capability is rendered null, then a message prompts you to run the business capability update levels job to recalculate the hierarchy IDs.

5.  To make the **Hierarchy ID** field editable, navigate to **System Properties** &gt; **All Properties**.

    1.  Select the **use\_business\_capability\_custom\_hierarchy\_id** system property in the sys\_properties.list.

    2.  Enter true in the **Value** field.

    3.  Select **Update**.

        **Note:** Since the hierarchy ID is customized, the system doesn’t check for any conflicts in the number or value that you set.

6.  To create child capabilities for the capability that you created, open the record and select **New** button in the **Capabilities** related list of the Business Capability form.

7.  In the related links, select **Update Capability Level and HierarchyID** to update the levels in the hierarchy.

    Selecting the **Update Capability Level and HierarchyID** link executes the **Update Capability Level and HierarchyID** scheduled script. You can [view the updated hierarchy in the capability map](view-capability-based-planning.md).

    If you had navigated to the Capability Hierarchy Map after updating the parent, order, or hierarchy ID but without running the update capability levels job, then a message prompts you to run the Update Capability Levels job and relaunch the page to render the capability hierarchy map with the latest change.

8.  To relate the capability with an application, select open the business capability.

9.  In the Related Items section of the business capability form, select the Add CI relationship \(\) icon to launch the relationship editor and create the [CI relationship](https://www.servicenow.com/docs/access?context=t_CreateCIRelationship&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

10. Select the **Provided by \(Parent\)** from the Suggested relationship types section.

    The filter is automatically applied on the business application.

11. In the Configuration Items section, select the relevant business application.

12. In the Relationships section, select the CI relationship icon to create a new relationship with selected configuration items.

    The Provided by::Provides relationship is added in the Relationships section.

13. Select **Save and Exit**.


## What to do next

View [capability based planning](../concept/overview-business-capability-planning.md) to understand the hierarchy of capabilities mapped with its related applications and [plan investments](view-capability-based-planning.md) in applications if the technology of the applications is at a risk.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)


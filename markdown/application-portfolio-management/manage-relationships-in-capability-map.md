---
title: Manage capability hierarchy in the capability map
description: Create a root-level capability, add a child capability to a parent, edit a capability, and delete a leaf capability, and manage the relationships between the capabilities in the capability map.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Use capability map for planning, Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Manage capability hierarchy in the capability map

Create a root-level capability, add a child capability to a parent, edit a capability, and delete a leaf capability, and manage the relationships between the capabilities in the capability map.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy capability ratings module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing a business portfolio](../concept/manage-business-portfolio.md).

Role required: sn\_apm.apm\_user

## About this task

When you add a child capability or update its order in the hierarchy, you can view the effect of your changes immediately in the hierarchical tree view of the capability map by refreshing or reloading the page. Whereas, when you add or edit a level-0 capability the **Update Business Capability Levels** scheduled job that updates the business capability levels is automatically executed to update the order and hierarchy of the capabilities in the map. Updating your business capabilities in the capability map saves your time and gives quick access to the updated data in the map.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Capability Ratings** &gt; **Capability Map**.

2.  Click **Manage Capability Hierarchy** button.

    The capability map opens up in the edit mode.

3.  To create a level-0 capability, click **New Capability** button.

4.  On the form, fill in the fields.

    For field information, see [Business capability new record form](../reference/business-capability-new-record-form.md).

5.  Click **Submit**.

6.  To add a child to a root capability, click the ellipses \(![Ellipses Icon](../image/EllipsesIcon.png)\) icon adjacent to the root-level business capability for which you intend to add a child capability.

7.  Click the **Add Capability** button and fill in the Business Capability New Record form fields.

    **Note:** The **Parent** field is auto-filled with the name of the selected root capability.

8.  Click **Submit**.

9.  To edit a capability, click the ![Ellipses Icon](../image/EllipsesIcon.png) icon adjacent to the root-level business capability.

10. Click the **Edit Capability** button and fill in the Edit Business Capability form fields.

    **Note:** The **Name** field is auto-filled with the name of the root capability. You can do the following with the edit option:

    -   Edit the name and description of a capability.
    -   Move a root-level capability as child capability in a different hierarchy.
    -   Edit a child capability to make it as a new root-level capability.
    -   Move a child capability from one root to another root.
    You can either enter a new name or keep the same name to the capability and add a parent to move the root-level capability from the existing hierarchy to a different hierarchy as a child capability. In a business scenario, this functionality is especially useful when you have to move a business capability from one business unit to another. For example, if your organization decides to move the Reward and Retain employees business capability from Finance to HR, then the business capability \(along with its child capabilities\) can be moved from Finance and appended in the HR business capability hierarchy.

11. Click **Submit**.

12. To delete a leaf capability, go to the leaf capability click the ![Ellipses Icon](../image/EllipsesIcon.png) icon adjacent to the leaf capability.

13. Click the **Delete Capability** button.

    **Note:** The **Delete Capability** button is available only for a leaf-level capability. A leaf-level capability is the one that does not have a child of its own.

14. Click **Delete**.

    **Note:** Delete action removes the capability from the business capability \[cmdb\_ci\_business\_capability\] table. It also removes the relationship that the capability has with the other configuration items in the CI relationship table.

15. Refresh or reload the page, for the map to reflect the changes that you made.


**Parent Topic:**[Use capability map for planning](view-capability-based-planning.md)


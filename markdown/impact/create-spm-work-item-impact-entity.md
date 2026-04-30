---
title: Manage work items from an initiative in the Impact Store Application
description: Use the SPM work item record link within the Impact entity to view its details, after Impact entity is successfully converted to an SPM work item.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Work items, Using Impact, Impact]
---

# Manage work items from an initiative in the Impact Store Application

Use the SPM work item record link within the Impact entity to view its details, after Impact entity is successfully converted to an SPM work item.

## Before you begin

Role required: Impact App Admin, Impact Platform Owner, Impact Portfolio Owner

If you do not have the Create and Write access to at least one of the SPM tables, then you can’t view the list of SPM work items. As a result, you can't select and convert an Impact entity to an SPM work item.

**Note:** Impact entities can either be converted into an SPM and Collaborative Work Management \(CWM\) work item, or, into an SPM or CWM work item.

## About this task

Out of the different accelerator and initiative types, only the free form initiatives can be converted into an SPM entity. The free form initiatives are created in Impact Delivery Instance, which then sync with the customer instance through service bridge.

After the conversion, whenever you access the Impact entity, you can select the link to the SPM work item and view the record details in the Strategic Planning Workspace in SPM.

Impact entities that can be converted to SPM entities are:

-   Free form initiatives that are not in **Closed** or **Cancelled** states can be created or converted into an SPM entity.
-   The status of a free form initiative moving to **On hold**, **Cancelled**, or **Closed** state will not have any effect on an already created SPM entity, creation of a new SPM entity, or deletion of an existing SPM entity.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Accelerator and Initiatives**.

    ![Free form initiative as an SPM work item.](../image/impact-free-form-init.png)

2.  Select a free form initiative that you want to convert to an SPM work item from **Your list** that is in **Not started** state.

    When you select the free form initiative, a message banner on top conveys the message that the initiative can be tracked in SPM and Collaborative Work Management applications.

3.  Select the my work item \(![my work item icon.](../image/impact-my-work-item-icon.png)\) icon from the right sidebar.

    ![Convert a free form initiative to an SPM work item.](../image/impact-convert-work-item.png)

    Since the free form initiative is not associated with the SPM entity yet, the icon is enabled for the association. If there are existing SPM work items associated with it, then they are listed in the **My work items** pane.

4.  Select **Convert to work item** to track the Impact entity as an actionable SPM and Collaborative Work Management work item.

5.  Select a work item from the list.

    In the Convert Free form initiative into a work item page, you can play the **intro video** to understand the SPM feature.

6.  Select any of the available options.

    1.  Demand
    2.  Product idea
    3.  Project
    4.  CWM Board
    5.  Epic
    6.  Strategic program
    7.  Initiative
    For example, you can select a project to convert it to an SPM work item.

    **Note:** If you do not have the Create and Write access to any of the SPM tables, you may not be able to view any of the SPM work items. As a result you can't select and convert an Impact entity to an SPM work item.

7.  Select **Next**.

    The work item opens in a Strategic Planning Workspace. The record details are mapped and the free from initiative's **Name** field is mapped with the Project's name field, and hence the field is pre-populated. You can enter details in the mandatory fields, and other details if needed.

    ![Convert Free form initiative to an SPM work item.](../image/impact-select-work-item.png)

8.  Select **Convert**.

    After you convert, an SPM work item is created, and the free form initiative is associated with the SPM entity in the Impact SPM Entity Association \[sn\_impact\_cust\_impact\_spm\_entity\_association\] table. You will see a message after the operation is successful, and the link to the SPM work item is available in the Impact entity.

9.  Select the free form initiative link in the message to view the SPM work item details.

    You can also select the ![my work item icon.](../image/impact-my-work-item-icon.png) icon to view the details.

    ![SPM work item is linked in Impact entity.](../image/impact-free-form-link.png)



---
title: Align work with a goal or target
description: Create a goal or target relationship with a planning item or any other item to identify and associate your current or future work and achieve your goals and targets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/associate-work-with-goals-strategy.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage enterprise goals, Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Align work with a goal or target

Create a goal or target relationship with a planning item or any other item to identify and associate your current or future work and achieve your goals and targets.

## Before you begin

Role required: sn\_apw\_advanced.spw\_goal\_user

## About this task

You can associate a goal or target with planning items as well as with any ServiceNow AI Platform table record.

From the Align work window, you can associate a goal or target with multiple planning items at a time. From the Planning items tab of the goal or target, you can associate a goal or target with only one planning item at a time.

You can create goal or target relationships with a custom planning item from the Align work window only if the planning item table is added to the **planning\_item\_types\_allow\_list** property. For more information, see [Enable custom item types in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/enable-custom-item-types-strategic-planning-workspace.md).

**Note:** When a goal or target relationship is created with a planning item \(Project, Demand, or Epic\) or any other ServiceNow AI Platform table record, the record appears on the Aligned work tab on the goal record.

\[Omitted image "align-work-goal-strategy.gif"\] Alt text: Align work with goals in Strategy and Goals.

## Procedure

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Strategy and Goals**.

2.  On the Strategy and Goals page, select the goal-based board for which your goal or target belongs to.

3.  Select the Row context menu icon \(\[Omitted image "more-actions.png"\] Alt text: Row context menu icon.\) of the goal or target that you want to align work and then select **Align work**.

4.  On the Align work window, select items that you want to align.

    1.  Select **Planning item** to align planning items or select **Other item** to align any ServiceNow AI Platform table records other than planning items.

    2.  From the list of items, select the items that you want to associate with the selected goal or target.

        **Tip:** You can search for the required items by applying a filter on the Name or any other required column.

    3.  Select **Confirm**.

    For a description of the field values, see [Goal/Target Relationship form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/goal-relationship-form-egm.md).


**Related topics**  


[Create a goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/create-goal-strategy.md)

[Add a target for goal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/set-target-for-goal-strategy.md)

[Duplicate a goal or target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/duplicate-goal-target-strategy.md)

[Send a reminder for target actuals check in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/send-reminder-target-checkin-strategy.md)


---
title: Customize a Work Scheduler card using the Next Experience UI Builder
description: Customize the Work Scheduler card components, such as adding an extra field, or changing the color or order of a field, to display them in the Work scheduler queue.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up, Work scheduler, Workforce Optimization for ITSM, IT Service Management]
---

# Customize a Work Scheduler card using the Next Experience UI Builder

Customize the Work Scheduler card components, such as adding an extra field, or changing the color or order of a field, to display them in the Work scheduler queue.

## Before you begin

Role required: workspace\_admin, or ui\_builder\_admin​

## About this task

You can duplicate an existing work item variant such as an Incident, Problem, Change Request and customize it based on your needs.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the **My experiences** list, select **Manager Workspace**.

3.  Select the Pages icon.

4.  In the **Page** menu, select **Work scheduler**.

5.  In the left pane, go to the **Content** section and navigate to **Body \(Flex\)** &gt; **Work queue \(Flex\)** &gt; **Sidebar**.

6.  In the right pane, select the icon \(![Edit card icon](../image/edit-card-icon.png)\) in the **Work item cards default** sub-page.

7.  In the left pane, select **Body \(Flex\)** &gt; **Viewport1**.

8.  In the right pane, select the icon \(![Edit card icon](../image/edit-card-icon.png)\) next to a card, for example, **Incident default**, that you want to configure.

9.  To duplicate the selected variant, in the left pane, in the **Variants** section, hover over the variant you want to duplicate, select the \(![Menu variant icon](../image/menu-variant-icon.png)\) icon and select **Duplicate**.

10. Hover over the variant you have duplicated, select the \(![Menu variant icon](../image/menu-variant-icon.png)\) icon and select **Edit conditions**.

11. In the **Order** field, set the order to be the lowest value so that this variant will display in manager workspace.

    **Tip:** You can only display one variant for a work item type.

12. Click **Save**.

13. Customize the variant you've created using any of the tasks or steps listed in [Create a Work scheduler card using the Next Experience UI Builder](create-workscheduler-card-wfo-itsm.md).


## Example

|If you'd like to configure this in the Work Scheduler card|Refer to|
|----------------------------------------------------------|--------|
|Add fields|[Create page scripts for Work scheduler](work-sched-create-page-scripts.md) and refer to the Create the **Transform workItem to cardProps** page script steps.|
|Add an avatar|[Configure an avatar component for Work scheduler](work-sched-avatar-component.md)|

**Parent Topic:**[Setting up Work scheduler in Workforce Optimization for ITSM](../concept/setting-up-work-scheduler.md)

**Related topics**  


[Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md)


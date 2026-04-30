---
title: Landing page configuration example
description: Learn how to configure a landing page through an example configuration process.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a landing page variant, UI Builder for Agent Workspace for HR Case Management, Configure, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Landing page configuration example

Learn how to configure a landing page through an example configuration process.

## Before you begin

Create a variant of your landing page. For more information, see [Create a landing page variant](configure-report-aws.md).

Role required: sn\_hr\_agent\_ws.admin and sn\_hr\_core.basic

## About this task

The configuration example shows how you would configure an **HR Cases closed in the last week** report beside the **Cases closed over the last 6 months** report on a landing page.

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **UI Builder for Agent Workspace for HR Case Management**.

2.  Select your variant.

3.  Select the **Editor** tab if it is not already selected.

4.  In the Page content panel, select **Container 7**.![Container 7 in the Page content panel](../image/uib-container-seven.png)

5.  In the Configuration panel, create three columns by entering `3` in the **Columns** field.![Column entry in the Configuration panel](../image/uib-container-seven-config.png)

6.  Select the more icon \(![More icon](../../legal-simple-contracts/image/menu-icon.png)\) beside **Column 2**.

7.  Select **Add after**.

8.  Select the **Components** tab and select **Container**.

    A container is an area of the page where you add information, images, or functionality \(your components\). You can have several containers on a page, nest containers within containers, and include several components in the containers.

9.  Add a component by selecting **+Add component** under the container.![Add component](../image/add-component.png)

    This example uses **Container 23**.

10. Select the **Data visualization** component.

11. Add a data source.

    1.  In the Configuration panel, select **+ Add data source**.![Adding a data source](../image/add-data-source.png)

    2.  In the **Select a source** field, enter `HR Case`.

    3.  Select the **sn\_hr\_core\_case** table.

    4.  Select **+Add custom conditions**.

    5.  Add a condition with the following values:

        -   Select field: `Assignment group`
        -   Select operator: `is(dynamic)`
        -   Enter value: `One of my groups`
    6.  Refine the condition by selecting **AND**.

        You can create dependent conditions by selecting **AND** or **OR**.

    7.  Add a condition with the following values:

        -   Select field: `Closed`
        -   Select operator: `at or after`
        -   Enter value: `Last week`
    8.  Select **Add this source**.

12. In the Configurations panel, expand **Additional settings**.![Additional settings in the Configuration panel](../image/additional-settings.png)

13. Add additional data to display by enabling **Show metric label** and **Show score update time**.

14. Select **Save**.

15. Make the variant the default landing page by changing the order of the original landing page.

    1.  Select **Landing page default** from the drop- down list.

    2.  Select the **Settings** tab.

    3.  Enter a number greater than 0 in the **Order** field.

    4.  Select **Save**.


**Parent Topic:**[Create a landing page variant](configure-report-aws.md)


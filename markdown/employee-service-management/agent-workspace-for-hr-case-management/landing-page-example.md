---
title: Landing page configuration example
description: Learn how to configure a landing page through an example configuration process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/agent-workspace-for-hr-case-management/landing-page-example.html
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

Create a variant of your landing page. For more information, see [Create a landing page variant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/agent-workspace-for-hr-case-management/configure-report-aws.md).

Role required: sn\_hr\_agent\_ws.admin and sn\_hr\_core.basic

## About this task

The configuration example shows how you would configure an **HR Cases closed in the last week** report beside the **Cases closed over the last 6 months** report on a landing page.

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **UI Builder for Agent Workspace for HR Case Management**.

2.  Select your variant.

3.  Select the **Editor** tab if it is not already selected.

4.  In the Page content panel, select **Container 7**.\[Omitted image "uib-container-seven.png"\] Alt text: Container 7 in the Page content panel

5.  In the Configuration panel, create three columns by entering `3` in the **Columns** field.\[Omitted image "uib-container-seven-config.png"\] Alt text: Column entry in the Configuration panel

6.  Select the more icon \(\[Omitted image "menu-icon.png"\] Alt text: More icon\) beside **Column 2**.

7.  Select **Add after**.

8.  Select the **Components** tab and select **Container**.

    A container is an area of the page where you add information, images, or functionality \(your components\). You can have several containers on a page, nest containers within containers, and include several components in the containers.

9.  Add a component by selecting **+Add component** under the container.\[Omitted image "add-component.png"\] Alt text: Add component

    This example uses **Container 23**.

10. Select the **Data visualization** component.

11. Add a data source.

    1.  In the Configuration panel, select **+ Add data source**.\[Omitted image "add-data-source.png"\] Alt text: Adding a data source

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

12. In the Configurations panel, expand **Additional settings**.\[Omitted image "additional-settings.png"\] Alt text: Additional settings in the Configuration panel

13. Add additional data to display by enabling **Show metric label** and **Show score update time**.

14. Select **Save**.

15. Make the variant the default landing page by changing the order of the original landing page.

    1.  Select **Landing page default** from the drop- down list.

    2.  Select the **Settings** tab.

    3.  Enter a number greater than 0 in the **Order** field.

    4.  Select **Save**.


**Parent Topic:**[Create a landing page variant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/agent-workspace-for-hr-case-management/configure-report-aws.md)


---
title: Diagnose and resolve a domain order
description: As a customer service agent, review, diagnose, and resolve, and close a domain order for the service-related issue experienced by the customer.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Order Management diagnostics capability, Integrate, Sales Customer Relationship Management]
---

# Diagnose and resolve a domain order

As a customer service agent, review, diagnose, and resolve, and close a domain order for the service-related issue experienced by the customer.

## Before you begin

Role required: admin

To enable the display of the **Diagnose** tab and **Run diagnostics** in the conceptual panel, the **Test and Turn up** must be selected in the **Stage**.

The decision table enables the Test and turn up to configure the trigger for any request definition. This out-of-the-box feature is shipped only for Test and turn up task.

## About this task

The domain order progresses through several stages from start to closure. It begins with a customer service agent reviewing and verifying the problem. Next is the diagnosis stage, where system-specified tests are executed to identify the root cause. After the tests, the agent moves to the repair, creating a task to fix the identified issue. The agent follows the instructions in the repair task to address the problem areas. Once the repair is complete, the task is retested to confirm that the issue is resolved. Finally, the order is moved to the next step toward delivery based on the customer's feedback.

This task is applicable for product order, services, and resources.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the List icon.

3.  Navigate to **Customer Orders** &gt; **All**.

4.  In the **Product Orders** tab, open the product order record.

    ![product order.](../image/diagnose-product-order.png)

5.  Review and verify the domain order.

    1.  In the **Details** tab, expand the Product Order task and then review and verify the general details for the domain order.

    2.  If necessary, in the Notes section, add **Additional comments** and **Work notes**.

6.  Diagnose the domain order to identify the root-cause of the problem.

    The decision table can be configured to control the visibility of the Diagnose and Run Diagnostics contextual panel tabs. For more information about decision tables, see [Decision Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/decision-tables/decision-table.md).

    1.  To generate the test results, select **Run diagnostics** from the contextual panel.

    2.  In the run diagnostics panel, select **CI/Service** from the drop-down list.

        The drop-down list shows the current product inventory and all the child inventories.

    3.  Expand the cards in the **Available test suite**.

    4.  In the manual test, select single/multiple tests.

        In the automated test, selection of test isn’t available. The subflow that is configured for the test group would be invoked.

    5.  Select **Configure**.

    6.  In the Configure tests dialog box, fill the test-required characteristics form to activate the **Run test** button.

    7.  In the test dialog box, select an option either to **Run test** now or to **Schedule test** for later.

    8.  Select **Run test**.

    9.  In the diagnose tab **Test results** section, select **Refresh list** ![](../image/refresh-order-line-item-orchestration-plan-ui.png) icon.

    10. In the diagnose tab, expand the **Test results** and review the results of the tests conducted in the previous step, checking whether each test is passed or failed.

        The failed tests indicate that the issues causing the order task to be identified and need repair.

        The maximum number of rows to the group is limited to 20 rows. To configure the maximum number of rows more than 20 rows to the group, see [Presentational List Usage](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-list/usage).

    11. Select the **View Details** ![](../../../reuse/icons/product-icons/open-link-right-fill-24.svg) icon for a specific test result to review its details.

    12. Select the **Rerun test** ![](../../../reuse/icons/product-icons/arrow-clockwise-outline-24.svg) icon for a specific test result to run it again.

    13. Select **Continue**.

7.  Repair the order task by creating a new or automated repair task.

    -   Select **Generate automated task** to automatically create a repair task.
    -   Select **Create repair task** to manually create a customize repair task.
    A Repair task is created for all failed test cases related to the diagnosed order task.

    1.  Select the repair task that you want to work on.

    2.  In the Resolution task form, review the task details to identify the failed test and then work on those tests to fix the order task.

    3.  In the **Select** field, select an appropriate state from the list to update or close the repair task, such as Closed complete.

    4.  Select **Save** and close the resolution task.

    5.  Select **Continue**.

8.  To view the Orchestration of the domain order, select the **Order Orchestration** tab.

9.  To view the tasks of the domain order, select the **Order Tasks** tab.

10. To view the characteristics values of the domain order, select the **Product Order Characteristics Values** tab.

11. To view the details of the service order, select the **Service Orders** tab.

12. To view the details of the domain order related items, select the **Domain Order Related Items** tab.

13. To view the composed of items, select the **Composed of items** tab.



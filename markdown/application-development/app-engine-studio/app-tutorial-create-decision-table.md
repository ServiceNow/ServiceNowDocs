---
title: Build a decision table
description: Build a decision table for the employee travel request application that determines which regional head to route travel requests to.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Adding logic and automation, App creation tutorial, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Build a decision table

Build a decision table for the employee travel request application that determines which regional head to route travel requests to.

## Before you begin

Role required: admin, decision\_table\_admin, or delegated developer permissions

## About this task

The first phase in adding logic and automation to the employee travel request application is to build a decision table. Our decision table evaluates where an employee is located and uses that information to determine which regional head to route their travel request to.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Phase 1

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Build a decision table](app-tutorial-create-decision-table.md)

</td></tr><tr><td>

Phase 2

</td><td align="justify">

![Not started icon](../image/app-tutorial-progress-not-started.png)

</td><td>

[Create a flow](app-tutorial-create-a-flow.md#)

</td></tr></tbody>
</table>For more information about using decision tables, see [Create decision tables in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/create-decision-table-in-decision-designer.md).

Follow along with the tutorial to build a decision table for the employee travel request application.

Video 6 

|Timestamp|Section|
|---------|-------|
|0:05|Create a decision table.|
|0:12|Create a new decision table.|
|0:13|Enter a unique name and choose the scope for the decision table.|
|0:28|Add an input.|
|0:36|Add a condition column.|
|0:52|Add conditions.|
|0:59|Add a result column.|
|1:09|Add results.|
|1:16|Add more conditions.|
|1:34|Save your changes.|
|1:36|Verify that the decision table has been added to your application.|

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  Select the travel request application.

3.  On the application dashboard, select **+ Add** next to **Logic and automation**.

4.  Select **Decision**, then select **Begin**.

5.  Select **Create a new decision table**.

6.  Define the properties of the decision table.

    1.  Enter `Regional head approvals` in the **Name** field.

    2.  In the **Accessible from** field, select **This application scope only** to have the logic in the decision table apply to only the selected application.

        If you want the logic in your decision table to apply to all applications, select **All application scopes**.

    3.  Select **Continue**.

7.  Select **Edit decision table** to continue setting up your decision table.

8.  Add an input to the decision table.

    **Note:** Inputs define the data that is evaluated in the decision table.

    In our tutorial, we set the input as the travel request table so that the decision table can evaluate employee information associate with each travel request.

    1.  Select **+ Add an input**.

    2.  In the **Type** field, select **Reference**, then select the travel request table from the list.

    3.  In the **Label** field, enter `Employee travel requests`.

    4.  Repeat this procedure to create as many inputs as you need for your decision table.

        In our tutorial, we don’t create additional inputs.

9.  Add a condition column to the decision table.

    **Note:** Condition columns act as filters that refine the input data by specifying which values should be evaluated by the decision table.

    In our tutorial, the condition column refines the input data to evaluate only the employees' country codes. Employees' country codes determine which regional head their travel requests should route to.

    1.  Select **+ Add condition column**.

    2.  In the **Condition column label**, enter `Employee regions`.

    3.  In the **Input** field, select the travel request table input.

    4.  For **Data to evaluate**, select **Field**.

    5.  In the **Field** field, select **Opened by** &gt; **Country code**.

    6.  In the **Default operator** field, select **is one of**.

    7.  Select **Done**.

    8.  Repeat this procedure to create as many condition columns as you need for your decision table.

        In our tutorial, we don’t create additional condition columns.

10. Define individual conditions for the condition column.

    **Note:** Conditions represent the individual values that the decision table evaluates to return results.

    In our tutorial, the conditions that we define represent each country that corresponds to a different regional head. We define individual conditions for the countries that make up the Americas \(AMS\) region, the Asia Pacific \(APAC\) region, and the Europe, Middle East, and Africa \(EMEA\) region.

    1.  Select in the empty box in the condition column.

        ![You can select in the empty box in the condition column to create conditions.](../image/app-tutorial-condition-column-value.png)

    2.  Select **is**, then select **is one of** from the list.

    3.  In the empty space beneath **is one of**, select **Brazil** and **United States**.

    4.  Select **OK**.

    5.  Select **+ Add a new decision row** to add additional conditions to the condition column.

    6.  Repeat the process in steps a-e to define additional conditions.

        In our tutorial, we define two additional conditions for the countries that make up the APAC and EMEA regions. The following table outlines the condition column values that we set:

<table id="table_jg3_5yy_fdc"><thead><tr><th>

Operator

</th><th>

Value

</th></tr></thead><tbody><tr><td>

**is one of**

</td><td>

-   **China**
-   **Japan**


</td></tr><tr><td>

**is one of**

</td><td>

-   **France**
-   **Germany**
-   **Italy**
-   **Spain**
-   **United Kingdom**


</td></tr></tbody>
</table>11. Add a result column to the decision table.

    **Note:** Result columns determine the type of data to return after evaluating the input and condition values.

    In our tutorial, the result column determines which regional head to route travel requests to. As the regional heads are individual users in the system, the result column references the User \[sys\_user\] table.

    1.  Select **+ Add result column**.

    2.  In the **Result column label** field, enter `Regional heads`.

    3.  In the **Description** field, enter a description for the result column.

    4.  In the **Type** field, enter `Reference`, then select **Reference** from the list.

    5.  In the **Reference table** field, enter `User`, then select **User \[sys\_user\]** from the list.

    6.  Select **Done**.

    7.  If you want to define additional results for your decision table, repeat this procedure to create as many result columns as needed.

        In our tutorial, we don’t create additional result columns.

12. Define the results for the result column.

    **Note:** Results are the individual values, or decisions, that are generated based on inputs, conditions, and results defined in the decision table.

    In our tutorial, the results represent the regional heads for each region.

    1.  Select in the empty box in the result column.

        ![Select in the empty box in the result column to define results.](../image/app-tutorial-result-column-value.png)

    2.  In the empty field, enter the name of the regional head.

        For the Americas \(AMS\) region, enter `Lucius Bagnoli`.

    3.  Select the regional head from the list, then select the Enter key.

    4.  Repeat the process in steps a-c to create as many results as needed for the decision table.

        In our tutorial, we create two additional results for the APAC and EMEA regional heads. The following table outlines the regional head user information for each region:

        |Region|User|
        |------|----|
        |Asia Pacific \(APAC\)|`Rob Phil`|
        |Europe, Middle East, and Africa \(EMEA\)|`Abel Tuter`|

13. Select **Save**.

14. Verify that your decision table has been added to your application.

    1.  Navigate to your application home page.

    2.  Confirm that your decision table appears in the **Logic and automation** section.


## Result

You have built a decision table for your application.

## What to do next

Proceed to the next phase in adding logic and automation to the employee travel request application: [Create a flow](app-tutorial-create-a-flow.md#).


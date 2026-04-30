---
title: Build your first flow in Workflow Studio
description: Step through an example of how to build, test, and activate a sample flow in Workflow Studio.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Getting started with flows, Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Build your first flow in Workflow Studio

Step through an example of how to build, test, and activate a sample flow in Workflow Studio.

## Before you begin

-   Role required: admin, flow\_designer, or delegated\_developer
-   Make sure to familiarize yourself with any features that your business uses to automate operations on the ServiceNow AI Platform, such as [flows](../../workflow-studio/concept/exploring-flows.md), [subflows](../../workflow-studio/reference/exploring-subflows.md), and [actions](../../workflow-studio/concept/exploring-actions.md).

## About this task

To help you get started with building your first flow in Workflow Studio, follow along with the steps below. The example flow will start, or trigger, every time a user on the instance creates a request for a Service Catalog item. When a request is created, our flow will automatically run the following actions:

-   Check if the catalog item's price is greater than $1,000.
-   If the price is greater than $1,000, notify the requester's manager to approve the request.
-   Otherwise, if the price is less than or equal to $1,000, automatically approve and close the request.

## Procedure

1.  Use the filter navigator to go to **All** &gt; **Self-Service** &gt; **Service Catalog**.

2.  From the Top requests box, select **Standard Laptop** and complete the record producer.

    The system produces a Requested Item record that has a price of $1100 or more \(RITM0010001\).

3.  Use the filter navigator to go to **All** &gt; **Process Automation** &gt; **Flow Designer**.

4.  On the Workflow Studio landing page's main header, select **New** &gt; **Flow**.

5.  In the Flow properties window, fill in the following fields:

    |Field|Action|
    |-----|------|
    |Flow name|Enter `Approval flow for requested items`|

    Then select **Submit** to open your flow in the Workflow Studio design environment.

6.  Under the TRIGGER section, select **Add a trigger**.

7.  In the trigger picker, either enter `Service Catalog` in the search field, or locate the **Service Catalog** trigger under the APPLICATION category.

    Then, select the **Service Catalog** trigger to add this trigger to your flow. Later, when we test this flow, we can simulate firing this trigger by creating a new Service Catalog Item Request record.

8.  Click **Done** to finish adding the **Service Catalog** trigger to your flow.

9.  Under the ACTIONS section, select **Add an Action, Flow Logic, or Subflow**.

    Then, select **Flow Logic** to open the flow logic picker.

10. In the flow logic picker, select **If**

11. Next to the Condition 1 input, click the pill picker icon \(![Pill picker icon](../images/data_pill_picker.png)\) to open the dot-walker.

    The dot-walker lets you access data from the trigger in your flow. Later, when you add actions to your flow, you can also use the dot-walker to access data from those actions. You can use the dot-walker to drill down into data that references other records in order to get the proper field placeholder value that you want to drop as a data pill in an action's input.

12. Navigate, or dot-walk, to **Trigger - Service Catalog** &gt; **Requested Item Record** &gt; **Price** and select **Price** to add this data pill to the Condition 1 input.

13. In the condition builder's next field, choose **greater than**, and then enter `1000` in the final field.

    Now, you've successfully set up a condition that will check if the price of the catalog item that a user requests is greater than $1,000.

14. Click **Done** to finish adding the **If** flow logic to your flow.

15. Under your **If** flow logic condition, select **Action**.

16. In the action picker, either enter `Ask For Approval` in the search field, or locate the **Ask For Approval** action by selecting **ServiceNow Core** &gt; **Ask For Approval** under the Default subcategory.

17. Add the following values for the Ask For Approval action's inputs:

    |Input|Action|
    |-----|------|
    |Record|Click the pill picker icon \(![Pill picker icon](../images/data_pill_picker.png)\) to open the dot-walker. Then, navigate, or dot-walk, to **Trigger - Service Catalog** &gt; **Requested Item Record** and select **Requested Item Record** to add this data pill to the input.|
    |Table|Leave as `Requested Item [sc_req_item]`.|
    |Approval Field|Leave as `Approval`.|
    |Journal Field|Leave as `Approval history`.|
    |Rules|Leave the first field as `Approve`. Under When, select **Anyone approves** from the list. Then, click the pill picker icon \(![Pill picker icon](../images/data_pill_picker.png)\) to open to dot-walker. Navigate, or dot-walk, to **Trigger - Service Catalog** &gt; **Requested Item Record** &gt; **Opened by** &gt; **Manager** and select **Manager** to add this data pill to the field.|
    |Due Date|Leave as `None`.|

    Now, you've successfully set up a conditional action that will automatically ask for approval from the requester's manager for any catalog item they request that has a price greater than $1,000.

18. Click **Done** to finish adding the conditional **Ask for Approval** action within the **If** flow logic of your flow.

19. Select **Add an Action, Flow Logic, or Subflow**.

    Then, select **Flow Logic** and choose **Else** from the flow logic picker.

20. Under your **Else** flow logic, select the plus icon \(![Plus icon.](../images/add-action-icon.png)\) and then select **Action**.

    From the action picker, select the **Update Record** action.

21. Add the following values for the Update Record action's inputs:

    |Input|Action|
    |-----|------|
    |Record|Click the pill picker icon \(![Pill picker icon.](../images/data_pill_picker.png)\) to open the dot-walker. Then, navigate, or dot-walk, to **Trigger - Service Catalog** &gt; **Requested Item Record** and select **Requested Item Record** to add this data pill to the input.|
    |Table|Leave as `Requested Item [sc_req_item]`.|
    |Fields|Select **+ Add field value**. Then, select the **Approval** field and choose **Approved** as the field's value. Next, select the **State** field and choose **Closed Complete** as the field's value. Finally, select the **Close notes** field and enter `Request automatically approved, as requested item's value is less than $1,000` for the field's value.|

    Now, you've successfully set up a conditional action that automatically approves and closes the catalog item request if the requested item's price is less than or equal to $1,000.

22. To finish adding the conditional **Update Record** action within the **Else** flow logic of your flow, click **Done**.

23. In the main header, click **Save** to save the changes you've made to your flow.

    Your flow should look similar to the following example:

    ![An example flow that asks for a manager's approval for requested items whose price is greater than $1,000.](../images/build-your-first-flow-example.png)

24. To test your flow and see if it triggers and runs properly without any errors, go to the main header and click **Test**.

25. In the Test Flow window, select a Requested Item record that has a price greater than $1000, then select **Run Test**.

    For example, select the requested item record that you previously created from the service catalog \(RITM0010001\).

    You can select the Create new record icon \(![Create new record icon.](../images/add-record-button.png)\) to create a new requested item.

26. Select **Your test has finished running. View the flow execution details.**

27. On the Execution Details page, see the values that populated for the trigger and each automated action in your flow.

    For more information, see [Flow execution details](../concept/flow-execution-details.md).

28. Navigate back to your flow.

29. In the main header, click **Activate** so that your flow's trigger fires whenever a user on your instance creates a new Service Catalog Item Request record.


## What to do next

Your flow is now active and will run whenever it's triggered. Next, you can manage your flow every time it runs by viewing your flow's execution history. To view this history, open your flow in the Workflow Studio design environment and click **Executions** in the main header. The resulting page shows you the state of completion for each flow execution as well as how long it took for each flow execution to run, or its runtime. To troubleshoot a flow execution for errors, select an execution from this list to open the [Flow execution details](../concept/flow-execution-details.md).

**Parent Topic:**[Getting started with flows](getting-started-flow.md)


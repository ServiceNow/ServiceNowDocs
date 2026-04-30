---
title: Build a flow from a template in App Engine Studio
description: Step through an example of how to build, test, and activate a flow using a flow template in App Engine Studio.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Getting started with flows, Exploring flows, Exploring Workflow Studio, Workflow Studio, Build workflows]
---

# Build a flow from a template in App Engine Studio

Step through an example of how to build, test, and activate a flow using a flow template in App Engine Studio.

## Before you begin

Create an application in App Engine Studio. Once your application is built, you can use flow templates to create flows. For more information, see [Building applications in App Engine Studio](https://www.servicenow.com/docs/access?context=aes-app-creation&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin, flow\_designer, or delegated\_developer

## About this task

To help you get started with building a flow from a flow template, follow along with the steps below. The example flow will start, or trigger, every time a user on the instance creates a request for a Service Catalog item. When a request is created, our flow will automatically run the following actions:

-   Check if the catalog item's price is greater than $1,000.
-   If the price is greater than $1,000, notify the requester's manager to approve the request.
-   Otherwise, if the price is less than or equal to $1,000, automatically approve and close the request.

## Procedure

1.  Navigate to **All** &gt; **App Engine Studio** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  In your application, next to Automation, click the add icon \(![Add icon](../images/plus-icon-gray-small.png)\).

4.  From the gallery of automation templates, select **Create an approval for a requested catalog item**, then click **Begin**.

5.  From the **Template catalog item** list, select the **Standard Laptop**.

6.  In the **Ask for approval if the catalog item's price is greater than** field, enter `1000`, then click **Done**.

7.  In the **Name** field, enter `Approval flow for requested items`.

8.  In the **Description** field, enter `Approval flow for requested items`, then click **Continue**.

9.  Once your flow is created, click **Edit this flow**.

10. On the flow page, click the **If not approved** step, then click **Delete** to remove the step.

11. At the bottom of the flow, click the **Log** step, then click **Delete** to remove the step.

12. In the same way, delete the last two log actions at the bottom of the flow.

13. Select **Add an Action, Flow Logic, or Subflow**.

    Then, select **Flow Logic** and choose **Else** from the flow logic picker.

14. Under your **Else** flow logic, select the plus icon \(![Plus icon.](../images/add-action-icon.png)\) and then select **Action**.

    From the action picker, select the **Update Record** action.

15. Add the following values for the Update Record action's inputs:

    |Input|Action|
    |-----|------|
    |Record|Click the pill picker icon \(![Pill picker icon.](../images/data_pill_picker.png)\) to open the dot-walker. Then, navigate, or dot-walk, to **Trigger - Service Catalog** &gt; **Requested Item Record** and select **Requested Item Record** to add this data pill to the input.|
    |Table|Leave as `Requested Item [sc_req_item]`.|
    |Fields|Select **+ Add field value**. Then, select the **Approval** field and choose **Approved** as the field's value. Next, select the **State** field and choose **Closed Complete** as the field's value. Finally, select the **Close notes** field and enter `Request automatically approved, as requested item's value is less than $1,000` for the field's value.|

    Now, you've successfully set up a conditional action that automatically approves and closes the catalog item request if the requested item's price is less than or equal to $1,000.

16. To finish adding the conditional **Update Record** action within the **Else** flow logic of your flow, click **Done**.

17. In the main header, click **Save** to save the changes you've made to your flow.

    Your flow should look similar to the following example:

    ![An example approval flow requiring manager approval for requested items whose price is greater than $1,000](../images/build-flow-from-template-example.png)

18. To test your flow and see if it triggers and runs properly without any errors, go to the main header and click **Test**.

19. In the Test Flow window, select a Requested Item record that has a price greater than $1000, then select **Run Test**.

    For example, select the requested item record that you previously created from the service catalog \(RITM0010001\).

    You can select the Create new record icon \(![Create new record icon.](../images/add-record-button.png)\) to create a new requested item.

20. Select **Your test has finished running. View the flow execution details.**

21. On the Execution Details page, see the values that populated for the trigger and each automated action in your flow.

    For more information, see [Flow execution details](../concept/flow-execution-details.md).

22. Navigate back to your flow.

23. In the main header, click **Activate** so that your flow's trigger fires whenever a user on your instance creates a new Service Catalog Item Request record.


## What to do next

Your flow is now active and will run whenever it's triggered. Next, you can manage your flow every time it runs by viewing your flow's execution history. To view this history, click **Executions** in the main header. The resulting page shows you the state of completion for each flow execution as well as how long it took for each flow execution to run, or its runtime. To troubleshoot a flow execution for errors, select an execution from this list to open the [Flow execution details](../concept/flow-execution-details.md).

**Parent Topic:**[Getting started with flows](getting-started-flow.md)


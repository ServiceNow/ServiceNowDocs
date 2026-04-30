---
title: Test your application
description: Verify that your application works as intended before publishing by testing the application experience and flow.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [App creation tutorial, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Test your application

Verify that your application works as intended before publishing by testing the application experience and flow.

## Before you begin

Role required: admin or flow\_designer

## About this task

The final step in building an application is testing. There are several ways to test an application, including simulating the user experience and running flow executions to verify that everything works as expected.

This is the last step in the app creation tutorial. In this step, we create a test record in the record producer to verify that it triggers the flow to run. We also verify that approvals route to the correct users and that the flow performs the actions that we defined, such as updating records.

<table id="table_odl_xfd_fdc"><tbody><tr><td>

Step 1

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Planning your application](../concept/app-tutorial-introduction.md)

</td></tr><tr><td>

Step 2

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Create an app](app-tutorial-create-an-app.md)

</td></tr><tr><td>

Step 3

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Building a data model](../concept/app-tutorial-data-model.md)

</td></tr><tr><td>

Step 4

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Creating user experiences](../concept/app-tutorial-experience-layer.md)

</td></tr><tr><td>

Step 5

</td><td align="justify">

![Completed icon](../image/app-tutorial-progress-complete2.png)

</td><td>

[Adding logic and automation](../concept/app-tutorial-logic-automation-layer.md)

</td></tr><tr><td>

Step 6

</td><td align="justify">

![In progress icon](../image/app-tutorial-progress-wip.png)

</td><td>

[Test your application](app-tutorial-test-app.md)

</td></tr></tbody>
</table>For more information about testing your application, see [Testing and debugging applications](../../custom-application/concept/testing-and-debugging-applications.md).

Follow along with the tutorial to test the employee travel request application.

Test your application before deploying it. 

|Timestamp|Section|
|---------|-------|
|0:07|Activate your flow.|
|0:10|Navigate to your instance home page.|
|0:15|Impersonate a user to test your user experience.|
|0:20|Find and open your record producer.|
|0:26|Create a test record.|
|0:42|End the impersonation.|
|0:45|Navigate back to your flow.|
|0:48|Test your flow using the test record that you created.|
|0:56|Review the flow execution details.|
|1:00|Perform additional tests to verify that branching actions and flow logic run correctly.|

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  Open your application's flow.

    -   If your application isn’t already open, navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**. Then open your application and select the flow under the **Logic and automation** heading.
    -   If your flow is already open, verify that your changes are saved.
3.  Select **Activate**, then select **Activate** again to make your flow available to run.

    **Note:** You can also test your flow without activating it by creating a test record within Workflow Studio. For more information about testing before activating your flow, see [Test a flow](https://www.servicenow.com/docs/access?context=flow-test&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

    ![Select Activate within the Activate dialog to make your flow available to run.](../image/app-tutorial-activate-flow.png)

4.  Navigate to your ServiceNow AI Platform instance home page.

5.  Impersonate a user to test that your record producer functions as intended.

    1.  Open the user menu.

        ![You can impersonate a user by selecting Impersonate user within the user menu.](../image/app-tutorial-user-menu.png)

    2.  Select **Impersonate user**.

    3.  Select a user from the **Recent Impersonations** list or enter a different user's name in the user selection field.

        When testing your application, you should impersonate users who have the permissions required to access the features that you're testing.

        In our tutorial, we select a user with regular user permissions, as the record producer that we're testing is accessible to all users.

    4.  Select **Impersonate user**.

        The system updates the user menu and dashboard to reflect the correct information for the user that you’re impersonating.

6.  On the home page, navigate to **All** &gt; **Self Service** &gt; **Service Catalog**.

7.  Select **Services**.

8.  Select your record producer from the list.

    In our tutorial, we select our record producer called `Raise a travel request`.

9.  Complete the record producer fields to generate a test record.

10. Select **Submit**.

11. End the impersonation.

    1.  Open the user menu.

    2.  Select **End impersonation**.

12. Reopen your application's flow.

    1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

    2.  Open your application.

    3.  Select your flow under the **Logic and automation** heading.

13. Select **Test**.

14. In the **Test Flow** dialog, select the record field, then select the record that you created during the impersonation.

15. Select **Run Test**.

    The system runs the flow based on the test record that you selected.

16. Select **Your test has finished running. View the flow execution details**.

17. Review the flow execution details to verify that your flow runs as intended.

    The flow execution details page enables you to view detailed information about an action or flow, such as the run-time, current state, items run, and values produced. For more information about flow execution details, see [Flow execution details](https://www.servicenow.com/docs/access?context=flow-execution-details&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

18. Perform additional tests to verify that the flow completes all desired branches of actions and flow logic.

    For example, if your flow performs an action only after certain conditions are met, you can create those conditions to verify that the branching actions and logic run correctly.

    In our tutorial, we simulate the manager's approval to test the branching actions and flow logic.

    1.  Select the action that is in the **Waiting** state to view the action details.

        ![You can view and change the state of actions within your flow.](../image/app-tutorial-test-action-waiting-state.png)

    2.  In the action details, select the test record.

        ![You can open, view, and edit test records within your flow by selecting the record number, then selecting Open Record.](../image/app-tutorial-test-open-record.png)

    3.  Select **Open Record**.

    4.  Open the approval record by selecting the list item in the **Approvers** list.

        **Tip:** If your test record page doesn’t display the **Approvers** list, you can adjust the page configurations to display any lists that you want to appear. Complete the following steps to configure the lists that appear on your record page.

        1.  On the record page, select the Additional actions icon \(![Additional actions icon](../../../administer/form-builder/image/additional-actions-tables.png)\).
        2.  Select **Configure** &gt; **Related lists**.
        3.  Select the **Approvers** list item or any other lists that you want to appear on the record page and move them from the **Available** list to the **Selected** list.
        4.  Select **Save**.
    5.  On the approval record page, select **Approve** to simulate the manager's approval.

    6.  Navigate back to your flow.

    7.  Select the refresh icon \(![Refresh icon](../image/app-tutorial-refresh-icon.png)\) to update your flow.

    8.  Verify that your flow has run branching actions or flow logic based on the additional test that you performed.

19. Complete this procedure to perform as many additional tests as needed to verify that all branches of your flow run correctly.


## Result

Your have tested the employee travel request application and verified that it functions as expected.

## What to do next

Congratulations! You have completed the app creation tutorial by planning, building, and testing an application.You are ready to start building your own applications in App Engine Studio.

To see what tasks you could perform after building an application, such as publishing or managing app deployments, see [Publish your app](../concept/publish-your-app.md).


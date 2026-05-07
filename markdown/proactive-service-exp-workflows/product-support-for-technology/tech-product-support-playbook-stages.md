---
title: Technology Product Support Case playbook stages and activities
description: The Technology Product Support Case playbook includes stages and activities that assist agents in researching and resolving technology cases.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Playbook, Technology Product Support Case, Explore, Product Support for Technology]
---

# Technology Product Support Case playbook stages and activities

The Technology Product Support Case playbook includes stages and activities that assist agents in researching and resolving technology cases.

When an agent creates a technology product support case, the system opens a service selector modal and displays the services defined for the Technology Product Support case type.

The agent selects a service and then selects **Create** to create a case. The system creates the case and launches the Technology Product Support Case playbook. This playbook includes the stages and activities described in the following sections.

## Intake stage

During the intake stage, an agent gathers information about the customer, the issue, and the impacted instances.![Intake stage.](../image/tech-product-support-case-intake.png)

<table id="table_d4y_ypz_y1c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Gather details

</td><td>

The agent gathers information about the account and contact and the product and adds a short description.Select **Continue** to save the information and move to the next activity.

</td></tr><tr><td>

Describe the problem

</td><td>

The agent describes the issue type and the details and adds a case description and steps to reproduce. The agent can also add users to the watch list and add attachments.Select **Continue** to save the information and move to the next activity.

</td></tr><tr><td>

Identify impacted instances

</td><td>

The agent adds the impacted instances from a list of instances that belong to the account.Select **Continue** to save the information and move to the first activity in the Triage stage.

</td></tr></tbody>
</table>## Triage stage

During the triage stage, the agent reviews the case information, makes changes as needed, and sends an initial response to the customer.tech-product-case-resolve![Triage stage.](../image/tech-product-case-triage.png)

<table id="table_b42_gqz_y1c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Review the problem

</td><td>

The agent can review information about the customer issue, including the affected instances selected in the Intake stage and the sold product or product component.In addition to reviewing information, the agent can update the list of affected instances and the attachments.

The following actions are available:

-   **Assign to me**: The agent can select this action to self-assign the case.
-   **Accept**: The agent can select this action to accept the assigned case.

Once the case is assigned, the agent can select **Continue** to save the information and move to the next activity.

</td></tr><tr><td>

Send initial response

</td><td>

The agent can send a response to the customer by entering text in the **Initial response** field. If desired, the agent can use a template from the Response Templates tab in the contextual side panel.The agent can also enter text in the **Work notes** field to capture internal information.

After entering text in these fields, the agent can:

-   Select **Save** to save the information in the fields without sending it to the customer.
-   Select **Send and Continue** to send the initial response to the customer, post the work notes, and move to the Troubleshoot stage.

</td></tr></tbody>
</table>## Troubleshoot stage

During the troubleshoot stage, the agent investigates the customer's issue and updates their findings in the action plan. The agent can leverage tools such as search or recommended actions as part of the investigation. If the agent needs assistance, they can create case tasks or other types of records or initiate a Sidebar discussion.![Troubleshoot stage.](../image/tech-product-support-case-troubleshoot.png)

<table id="table_v3c_jqz_y1c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Diagnose

</td><td>

The decision table is provided with the Technology Product Support Case application. You can modify the conditions that have been defined, and the results to suit your requirements.

 To enable the diagnostic activity in the troubleshoot stage, select the case category in the decision table as Issue, the diagnostic activity field is field is updated to True.

 The status can be changed to False by the agent. For more details on updating decision tables, see [Decision Tables](https://www.servicenow.com/docs/access?context=decision-table&version=australia&pubname=australia-application-development&ft:locale=en-US).

 The agent can view and do the following actions in these tabs:

-   1.  To generate the test results, select **Run diagnostics** from the contextual panel.

**Note:** To avoid conflicts, the system allows only one test to run at a given time. This is true even if you have multiple client test runner windows open.

2.  In the run diagnostics panel, select **CI/Service** from the drop-down list.
3.  Expand the **Available Test Suite**.
4.  Select single/multiple test definitions.
5.  Select **Configure**.
6.  In the Configure tests dialog box, select test characteristics.
7.  In the test dialog box, select an option either to run the test now or to schedule it for later.
8.  Select **Run test**.
-   **Test results**
    1.  Select the **Test results** tab and review the results of the tests conducted in the previous step, checking whether each test is passed or failed.

The failed tests indicate that issues causing the service problem are identified and needing repair.

A Repair task is created for all failed test cases related to the diagnosed service problem. For each unique service and test specification, only one repair task is created. The agent can then work on it and close this repair task.

    2.  Select the **View Details** icon for a specific test result to review its details.
    3.  Select the **Rerun test** icon for a specific test result to run it again.
-   **Diagnostic tasks** If needed, the agent can create the diagnostic tasks manually and view the diagnostic tasks.

</td></tr><tr><td>

Update action plan

</td><td>

The agent investigates the issue and adds information to the following fields:-   Issue summary
-   Actions taken
-   Next steps

Selecting the **Update and continue** action:

-   Saves the information in the action plan.
-   Posts the information to the activity stream.
-   Moves the agent to the Related work activity.

</td></tr><tr><td>

Related work

</td><td>

The agent can see the action status of the case, if available, and can update the **Needs attention** field.

 The Related work activity includes a Recommended Actions card, **Talk to an expert**, that agents can use if they need assistance.

-   Select **Start discussion** to initiate a Sidebar conversation.
-   Select **Dismiss** to close the card.

 The Related work activity shows lists of related case records. The agent can expand these related record lists and view the record cards or create records.

 -   **Update action plan**: returns the agent to the Update action plan activity so they can update information.
-   **Continue**: completes the Troubleshoot stage and moves the agent to the Resolve stage.
-   **Create repair tasks**: Create a repair task and assign to the agent.

 The Related work activity includes **Resolution Tasks**, that agents can use If the test fails and manually create the resolution task to solve the issue. The agent can expand these **Resolution Tasks** lists and view the list of resolution tasks or create one.

</td></tr></tbody>
</table>## Resolve stage

In the Resolve stage, the agent proposes a solution to the customer.![Resolve stage.](../image/tech-product-case-resolve.png)

<table id="table_bv5_mqz_y1c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Propose resolution

</td><td>

The agent updates the following fields:

-   **Root cause code**
-   **Resolution code**
-   **Cause**
-   **Resolution notes**

 The agent can also enable the **Add resolution notes to comments** check box to add the resolution information to the case activity stream.

**Note:** If the Now Assist for Customer Service Management \(CSM\) application is installed and the resolution notes generation skill has been configured, the **Resolution notes** field is automatically populated. For more information, see [Using Now Assist for CSM to generate resolution notes for a case](tech-product-support-playbook.md#section_nsx_b4n_3bc).

 -   **Propose resolution**: Completes the activity and moves to the Close stage. The case state changes to Solution Proposed.
-   **Save**: Saves the information in the activity.

</td></tr></tbody>
</table>## Close stage

A case can be closed in the following ways:

-   The customer accepts the proposed solution.
-   The agent accepts the proposed solution on behalf of the customer.
-   The agent closes the case.
-   The system auto closes the case after it remains in the Solution Proposed state for a certain number of days.

In the Close stage, the agent updates the case with a summary of the issue and provides any additional comments or work notes.

The case record is read-only when the state is Closed.![Close stage.](../image/tech-product-case-close.png)

<table id="table_grq_4qz_y1c"><thead><tr><th>

Activity

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Close case

</td><td>

The agent updates the following fields:

-   Issue summary
-   Root cause code
-   Resolution notes
-   Add resolution notes to comments
-   Additional comments
-   Work notes

 -   **Accept Solution**: Saves the changes and posts the content in the **Additional comments** and **Work notes** fields to the activity stream. The case state changes from Solution Proposed to Closed.
-   **Reject Solution**: Saves the changes and posts the content in the **Additional comments** and **Work notes** fields to the activity stream. The case state changes from Solution Proposed to Work in progress.
-   **Save**: Saves the changes to the activity.

 After the case is closed, the agent can select **Create Post Case Review** to open a post case review record in a sub-tab.

</td></tr></tbody>
</table>## Save and Continue actions

When a stage is in progress, the **Continue** action saves the information in the stage and moves the agent to the next activity in the flow. This can be the next activity within a stage or the first activity in the next stage.

When a stage is complete, the **Save** action is also available. This action saves the information in the stage but does not move the agent to the next stage. The **Save** action enables agents to update information in completed stages.

## Displaying Recommended Actions in playbook activities

Recommended actions can be configured to appear inside playbook activities. By default, the **Talk to an expert** recommendation appears in the conceptual side panel.

The Technology Product Case Troubleshoot recommended actions rule:

-   Provides the recommendation for an agent to discuss a case issue with an expert. This recommendation.
-   Includes the following actions:
    -   **Start discussion**: starts a Sidebar discussion.
    -   **Dismiss**: dismisses the recommendation card.

For more information, see [Recommended Actions](https://www.servicenow.com/docs/access?context=configure-nba&version=australia&pubname=australia-customer-service-management&ft:locale=en-US).

**Parent Topic:**[Technology Product Support Case playbook](tech-product-support-playbook.md)


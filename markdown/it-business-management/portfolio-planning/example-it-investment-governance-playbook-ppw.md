---
title: Creation example for a demand playbook for IT governance
description: Build a demand playbook that guides technology investment requests through intake, architecture review, and a steering committee decision, and moves the demand state automatically at each step.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/portfolio-planning/example-it-investment-governance-playbook-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-11-03"
reading_time_minutes: 9
breadcrumb: [Playbooks in Next Experience for Demand Management, Manage demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Creation example for a demand playbook for IT governance

Build a demand playbook that guides technology investment requests through intake, architecture review, and a steering committee decision, and moves the demand state automatically at each step.

## Before you begin

Role required: admin, playbook.admin, or pd\_author

Build and test the playbook in a non-production instance first.

## About this task

This example shows one way to model a demand governance process in a playbook. Use it as a starting point and adapt the stages, activities, and assignments to your organization.

In this example, business teams request new technology, such as a self-service employee onboarding app. Before IT commits budget and people, every request goes through three stages:

-   Intake: The demand manager captures the business case, records the expected benefit, and requests the people that the demand needs.
-   Architecture review: The enterprise architect, and only the enterprise architect, checks that the request fits the technology standards.
-   Steering Committee decision: The CIO approves or rejects the investment.

As each stage finishes, the playbook moves the demand from Draft to Screening, then to Qualified, and then to Approved.

|Activity|Activity type|Assigned to|Starts|Result|
|--------|-------------|-----------|------|------|
|1.1 Capture business case|Record Form|The demand manager of the demand|When the stage starts|Business case, financial benefit, and planned dates are added to the demand.|
|1.2 Add a benefit plan|New Record Form|Playbook user|After 1.1|A benefit plan is created and linked to the demand.|
|1.3 Request resources|Instruction|Playbook user|After 1.2|Resource assignments are created on the **Resources** tab of the demand.|
|1.4 Submit for architecture review|Update Record|Automatic|After 1.3|The demand moves to Screening.|
|2.1 Technical fit assessment|Record Form|The enterprise architect \(a named user\)|When the stage starts|Impacted applications, size, risk, and assumptions are added to the demand.|
|2.2 Mark as qualified|Update Record|Automatic|After 2.1|The demand moves to Qualified.|
|3.1 Investment approval|Ask For Ad Hoc Approval|The CIO \(a named approver\)|When the stage starts|The investment is approved or rejected.|
|3.2 Mark as approved|Update Record|Automatic, only if the investment is approved|After 3.1|The demand moves to Approved.|

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select the **Playbooks** tab.

    **Tip:** The predefined Demand workflow playbook is listed on this tab. To start from it instead of from a blank playbook, select it and then select **Duplicate**.

3.  Create the playbook.

    1.  Select **New** &gt; **Playbook**.

    2.  In the **Playbook name** field, enter `IT Investment Governance`.

    3.  In the **Description** field, enter a sentence that explains the process to other playbook designers.

    4.  In the **Parent table** field, select Demand \[dmn\_demand\].

        The parent table makes this playbook a demand playbook.

    5.  Select **Build playbook**.

4.  Add a trigger so that only strategic project demands use this playbook.

    1.  Select the **Triggers** icon in the left sidebar.

    2.  Select **Add trigger** &gt; **When record is created or updated**.

    3.  In the **Trigger label** field, enter `Strategic project demand created or updated`.

    4.  Under **Conditions**, add the conditions `Category is Strategic` AND `Type is Project`.

    5.  Select **Save and close**.

    **Note:** The predefined Demand workflow playbook runs on every new demand. To keep it from also running on strategic project demands, add a condition to its trigger that excludes them, for example `Category is not Strategic`.

5.  Add the Intake stage.

    1.  Select **Board view**.

    2.  Select **Add Stage**.

    3.  In the **Label** field, enter `Intake`.

    4.  Describe what happens in the stage in the **Description** field.

    5.  Leave the **Start rule** set to **When playbook starts**

    6.  Select **Save and close**.

6.  Add the Capture business case activity and assign it to the demand manager of the demand.

    1.  In the Intake stage, select **Add activity**.

    2.  Search for `Record Form`, and select it.

    3.  On the **Details** tab, enter `Capture business case` as the label and add a short description.

    4.  On the **Automation** tab, select **Show additional options**.

    5.  In the **Assigned To** field, open the data pill picker and select **Parent Record** &gt; **Demand** &gt; **Demand manager**.

        The activity is assigned to whoever is the demand manager on each demand.

    6.  On the **UI Layout** tab, set **Associated table** to Demand and **Associated record** to the data pill **Parent Record** &gt; **Demand**.

    7.  In **Form fields**, select **Business case**, **Financial benefit**, **Planned start date**, and **Planned end date**, and then select **OK**.

        Include both planned dates. The **Resources** tab of the demand displays resourcing only after both dates are set.

    8.  Select **Save and close**.

7.  Add the Add a benefit plan activity, which creates a benefit plan linked to the demand.

    1.  Select **Add activity**.

    2.  Search for `New Record Form`, and select it.

    3.  On the **Details** tab, enter `Add a benefit plan` as the label, and describe what the user must enter.

        The start rule is set to after activity 1.1 automatically.

    4.  On the **Automation** tab, set **Table** to Benefit Plan \[benefit\_plan\].

    5.  Under **Template Fields**, select **Add Field**.

    6.  Select the **Project/Demand** field, and set it to the data pill **Parent Record** &gt; **Demand**.

        The **Project/Demand** field may display as Work. Setting it links every benefit plan created from this activity to the demand.

    7.  On the **UI Layout** tab, enter `Create record` in the **Tagline** field.

    8.  In **Form fields**, select **Name**, **Category**, **Sub category**, **Start fiscal period**, **End fiscal period**, **Entered currency**, **Entered benefit**, and **Description**.

    9.  Select **Save and close**.

8.  Add the Request resources activity, which sends the user to the **Resources** tab of the demand.

    1.  Select **Add activity**.

    2.  Search for `Instruction` and select it.

        An Instruction activity displays a message with the **Mark Complete** and **Skip** buttons.

    3.  On the **Details** tab, enter `Request resources` as the label, and enter the message for the user as the description.

        For example: `Open the Resources tab on this demand and create resource assignments for the roles this investment needs, for example developer or business analyst. Then select Mark Complete.`

    4.  On the **Automation** tab, verify that **Message** is set to **This activity** &gt; **Description** and that **Wait for user input** is set to **Yes**.

    5.  Select **Save and close**.

9.  Add the Submit for architecture review activity, which moves the demand to Screening automatically.

    1.  Select **Add activity**.

    2.  Search for `Update Record`, and select it.

    3.  On the **Details** tab, enter `Submit for architecture review` as the label, and explain in the description that the demand moves to Screening.

    4.  On the **Automation** tab, set **Record** to the data pill **Parent Record** &gt; **Demand** and **Table** to Demand.

    5.  Under **Fields**, add **State** and set its value to Screening.

    6.  On the **UI Layout** tab, enter `Automated state change` in the **Tagline** field.

        Users see this label in the playbook instead of the default Update Record label.

    7.  Select **Save and close**.

    **Note:** An Update Record activity sets the state without checking any conditions. To check the same conditions that apply when users change the state manually, such as the required role, add a custom demand state transition checker activity before the Update Record activity. For more information, see [Transition checker to move a demand to the next state automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md).

10. Add the Architecture review stage and its activities.

    1.  Select **Add Step** &gt; **Add Stage** to the right of the Intake stage.

    2.  Enter `Architecture review` as the label.

    3.  Describe what the architect checks, and set the start rule to **After specific stages**.

    4.  Add a Record Form activity with the label `Technical fit assessment`.

    5.  On the **Automation** tab, select **Show additional options**.

    6.  In the **Assigned To** field, enter the name of your enterprise architect.

        Only the assigned user can complete the activity. To assign the activity to a team instead, set **Assignment Group**, for example to your enterprise architecture group.

    7.  On the **UI Layout** tab, set the associated table and record as in the Capture business case activity.

    8.  In **Form fields**, select **Impacted Business Applications**, **T-Shirt size**, **Risk of performing**, and **Assumptions**, and then select **OK**.

    9.  Select **Save and close**.

    10. Add an Update Record activity with the label `Mark as qualified`.

    11. Configure it as in the Submit for architecture review activity, but set **State** to Qualified.

        The activity starts after 2.1 Technical fit assessment.

11. Add the Steering Committee decision stage and its activities.

    1.  Select **Add Step** &gt; **Add Stage**.

    2.  Enter `Steering Committee decision` as the label, and set the stage to start after the architecture review stage.

    3.  Select **Add activity**.

    4.  Search for `Ad Hoc Approval` and select **Ask For Ad Hoc Approval**.

    5.  Enter `Investment approval` as the label.

    6.  On the **Automation** tab, set **Approver** to your CIO, **Table** to Demand, and **Record** to the data pill **Parent Record** &gt; **Demand**.

        To have a group approve instead, set **Approver Group**.

    7.  Select **Save and close**.

    8.  Add an Update Record activity with the label `Mark as approved` that sets **State** to Approved.

    9.  On the **Details** tab of the Mark as approved activity, select **Show additional options**.

    10. Add a run condition: set the field to **3.1 Investment approval** &gt; **Approval State** and the value to `approved`.

    11. Select **Save**.

    12. Select **Save and close**.

        If the CIO rejects the investment, the activity is skipped and the demand stays in the Qualified state.

12. Review the playbook in **Board view** and **Diagram view**.

13. Select **Activate**.

    The status changes from Inactive to Active, and new demands that match the trigger start the playbook. After you change an active playbook, select **Activate** again to publish the change. Demands already in progress keep the version of the playbook that they started with.

14. Test the playbook.

    1.  Create a demand with Category set to Strategic and Type set to Project.

        For more information, see [Create a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-a-demand-ppw.md).

    2.  Open it from the List page in demands.

    3.  Select **Playbook** from the demand navigation menu.


## Result

The IT Investment Governance playbook appears with its three stages, and the Capture business case activity is ready for the demand manager.

As users work through the playbook, the demand moves through its states automatically:

-   After the demand manager completes the intake activities, the demand moves to Screening, and the technical fit assessment is assigned to the enterprise architect.
-   After the architect completes the assessment, the demand moves to Qualified, and the approval request goes to the CIO.
-   If the CIO approves, the demand moves to Approved and all three stages show as complete.

## What to do next

Adapt the example to other processes. For example:

-   For marketing demands, replace the enterprise architect with a brand reviewer and the CIO with the CMO, and add campaign fields to the forms.
-   For finance governance, add a decision so that demands above a cost threshold go through an additional finance approval stage.
-   For business units, create one playbook for each unit, and route demands to each playbook with its own trigger condition, for example on the department.

**Related topics**  


[Customize and create playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/create-and-customize-playbooks-ppw.md)

[Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/playbooks-in-demand-workspace-ppw.md)

[Use playbook for a demand](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/portfolio-planning/use-playbooks-in-ppw.md)

[Workflow Studio Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio-playbooks-landing.md)


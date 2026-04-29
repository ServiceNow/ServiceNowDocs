---
title: Create the Tests step in the control test
description: Apply the objective effectiveness of the test step and the operating effectiveness, desired effectiveness of the control test to determine the control effectiveness of the control test. A test step is applied to check the control test at a granular level.
locale: en-US
release: australia
product: Audit Management
classification: audit-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Audit Workspace Overview, Audit Management, Governance, Risk, and Compliance]
---

# Create the Tests step in the control test

Apply the objective effectiveness of the test step and the operating effectiveness, desired effectiveness of the control test to determine the control effectiveness of the control test. A test step is applied to check the control test at a granular level.

## Before you begin

Role required: sn\_audit.admin and sn\_audit.manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Audit Workspace**.

2.  Select the lists icon \(![List icon.](../image/ListsIcon.jpg)\).

3.  Select **All engagements** under **Execution**.

4.  Select the engagement.

    **Note:** You can create a test step for the engagements that are in **Valid** state.

5.  Select the **Audit tasks** tab.

6.  Select a control test link in the **Name** column.

    **Note:** The **Number** starting with CTR are the control tests.

7.  Select the **Test steps** tab to view the list of test steps and create a new test step.

    **Note:** You can also view the list of control test steps that are generated from the test plan within the engagement. For more information, see [Automatically generate control tests from an engagement](../../grc-audit/task/automatically-generate-control-test.md).

8.  Select **New** to create a new test step plan for the control test.

9.  In the new test step plan form, enter the following details:

    -   **Identifier**: The identifier of the test step.
    -   **Control test**: The name of the control test plan. By default, this field is automatically populated.
    -   **Assessment objective**: The assessment objective. An assessment objective is the guideline for how to assess the control.
    -   Values of the **Objective Effectiveness** of test plan:
        -   **None**: Indicates that the assessment procedure hasn’t been analyzed or assessed yet.
        -   **Effective**
        -   **Ineffective**
        -   **Not Applicable**: Indicates that the assessment procedure isn’t valid or not required for this control test check.
    The Control effectiveness of the control test is determined by:

    |Desire effectiveness|Operating effectiveness|Objective effectiveness|Control effectiveness|
    |--------------------|-----------------------|-----------------------|---------------------|
    |None/Effective|None/Effective|Effective|Effective|
    |Effective|Effective|Not applicable/None/Effective|Effective|
    |Ineffective|Ineffective|Not applicable/None/Effective/Ineffective|Ineffective|
    |Ineffective|Ineffective|Ineffective|Ineffective|
    |None/Effective|None/Effective|Effective|Effective|
    |None|None|One is Effective and another Ineffective|Ineffective|
    |None|None|One is None and another is Not applicable|None|

    As long as the control test is in the **Open** or **Work in Progress** state, it does not matter if the objective effectiveness of the test step is None. However, you cannot move the control test to the Review state until you mark every test step assessment objective as either Effective, Ineffective, Not Applicable or None. An error message pops up to indicate that you must check the test step objective and move it out of the None state, so as to move the control test to the **Review** or **Closed Complete** state.

10. Click **Save** to save the test step plan.



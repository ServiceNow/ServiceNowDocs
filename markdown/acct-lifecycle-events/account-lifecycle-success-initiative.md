---
title: Create a success initiative
description: Create a success initiative with a planned set of internal or external tasks to support a success outcome.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure customer success, Customer success, Account Lifecycle Events]
---

# Create a success initiative

Create a success initiative with a planned set of internal or external tasks to support a success outcome.

## Before you begin

Role required: sn\_acct\_lc.ale\_success\_agent, sn\_acct\_lc.ale\_success\_customer

## About this task

Success initiatives are a set of planned activities or tasks that a provider and a customer must complete to achieve a success outcome. A success initiative can include one or more tasks that can be internal or external and can be defined with the Create Success Initiative playbook.

**Note:** The Create Success Initiative playbook has a set of predefined stages and fields. You can add or modify these stages using Playbooks. See [Playbooks](https://www.servicenow.com/docs/access?context=exploring-process-automation-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for details.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and click the **List** icon.

2.  Navigate to the **Customer Success** &gt; **All Initiatives** and click **New** to launch the playbook.

3.  In the Initial Setup page, select the **Success Outcome** with this initiative is to be associated.

4.  Click **Continue** to move to the next tab.

    The success initiative record is created.

5.  In the Plan the Plan section, enter the core information for this initiative as follows.

<table id="table_ofk_5cb_1cc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Success outcome

</td><td>

Select the success outcome associated with this initiative.

</td></tr><tr><td>

Contact

</td><td>

The customer contact responsible for this initiative.

</td></tr><tr><td>

Assigned to

</td><td>

The internal team member responsible for this initiative.

</td></tr><tr><td>

Squad

</td><td>

The team supporting this account for achieving both value and success.

</td></tr><tr><td>

Category

</td><td>

The category associated with this initiative. This can be:-   General
-   Strategic planning
-   Architecture and design
-   Adoption
-   Technical guidance


</td></tr><tr><td>

State

</td><td>

State of the initiative. This can be:-   New
-   In progress
-   Paused
-   Canceled
-   Closed


</td></tr><tr><td>

Progress

</td><td>

Current progress of this initiative. This can be:-   Not Started
-   On-Track
-   At Risk
-   Paused
-   Completed
-   Canceled


</td></tr><tr><td>

Priority

</td><td>

Priority of this initiative in comparison to others. This can be:-   Critical
-   High
-   Medium
-   Low
-   Very Low


</td></tr><tr><td>

Due date

</td><td>

Date on which this initiative is due.

</td></tr><tr><td>

Subject

</td><td>

Enter a subject for this initiative.

</td></tr><tr><td>

Description

</td><td>

Enter a description for this initiative.

</td></tr></tbody>
</table>6.  Click **Mark Complete**.

7.  In the Collab and Complete step, click **Create Task** to automatically create a sample success task or click **Skip** to skip this step.

8.  In the Summarize and Close step, enter the following details.

    -   Closure code: Select the reason for which the record is being closed. This can be:
        -   Achieved
        -   Partially achieved
        -   Missed
        -   Canceled
    -   Close notes: Provide a description on which this initiative is being closed.
9.  Click **Mark Complete** to complete this task.

    **Note:** You can use response templates to provide quick responses, or copy and paste relevant information from a case. Click the **Response template** icon and select the response template you want to use. For more details on response templates, see [Response templates](https://www.servicenow.com/docs/access?context=response-templates-templated-snippets&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


## What to do next

You can perform the following actions:

-   Assign to me: Select this option to reassign this initiative to yourself.
-   Close initiative: Once the initiative has been completed and the Closure code is set to **Achieved**, you can close this initiative.
-   Create success play: Select this option to create a success play. See [Create a success play](account-lifecycle-create-success-play.md) for details.


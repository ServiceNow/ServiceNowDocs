---
title: Add a state model and transitions
description: Add a state model and transitions to specify conditions for moving between states.
locale: en-US
release: xanadu
product: State Management
classification: state-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [State Management, Configure core features, Administer the ServiceNow AI Platform]
---

# Add a state model and transitions

Add a state model and transitions to specify conditions for moving between states.

## Before you begin

Role required: state\_model\_admin or admin

## About this task

Develop and test your state model in a non-production instance before deploying it in the production instance.

## Procedure

1.  Navigate to **All** &gt; **State Management** &gt; **State Models**.

2.  Click **New**.

3.  Fill in the fields on the form.

<table id="table_k2c_wsz_y1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive name for this state model.

</td></tr><tr><td>

Table

</td><td>

Table this state model applies to.

</td></tr><tr><td>

Application

</td><td>

Defaults to **Global**.

</td></tr><tr><td>

Order

</td><td>

Order in which this state model is evaluated for the target table. State models are evaluated in numerical order, from the lowest number to the highest number.Leave space between the numbers so that you can insert a new state model later, if necessary. For example, enter 10 for the first state model to be evaluated, 20 for the next state model to be evaluated, and so on.

</td></tr><tr><td>

Active

</td><td>

Indicates that this state model is enabled. Clear this check box until you define the state transitions for the state model.

</td></tr><tr><td>

Description

</td><td>

Description of this state model.

</td></tr><tr><td>

Condition

</td><td>

Condition builder that sets the conditions for applying this state model to records.For example, you could add the condition **Category is Networking** versus **Category is Security** if there are different state models for networking requests and security requests.

</td></tr><tr><td>

Common Exit Condition

</td><td>

Condition builder that sets any common condition required for moving from one state to another.

</td></tr></tbody>
</table>4.  Open the form context menu and click **Save**.

    The **State Transitions** related list appears.

5.  Click **New** on the **State transitions** related list.

6.  Fill in the fields on the form.

<table id="table_kjw_tdd_fbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

State Model

</td><td>

State model that uses this state transition.

</td></tr><tr><td>

State

</td><td>

State this transition controls, for example **Ready** or **In Progress**.

</td></tr><tr><td>

Application

</td><td>

Defaults to **Global**.

</td></tr><tr><td>

Order

</td><td>

Order in which this state transition is evaluated. State transitions are evaluated in numerical order, from the lowest number to the highest number.For example, if the first predefined state is **New**, give that state the lowest order number so that the conditions for entering and leaving the state are evaluated first.

 Leave space between the numbers so that you can insert a new state transition later, if necessary. For example, enter 10 for the first state transition to be evaluated, 20 for the next state transition to be evaluated, and so on.

</td></tr><tr><td>

Terminal State

</td><td>

Selected if there are no transitions from this state.

</td></tr><tr><td>

Description

</td><td>

Description of this state transition.For example, the **Description** for the Assess state could be `New state can move only to Assess state`.

</td></tr><tr><td>

Enter Condition

</td><td>

Condition builder that sets the conditions for entering this state.

</td></tr><tr><td>

Exit Condition

</td><td>

Condition builder that sets the conditions for exiting this state.

</td></tr></tbody>
</table>7.  Click **Submit**.

    The state model form reopens, and the new transition is added to the related list.

8.  Continue adding state transitions for the remaining states.

9.  When finished adding state transitions in the state model form, select the **Active** check box and click **Update**.



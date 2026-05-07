---
title: Transaction Manager: Stages
description: A stage represents a phase in an organization's selling process. This article illustrates a process with five stages that you can modify to suit your needs.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Stages

A stage represents a phase in an organization's selling process. This article illustrates a process with five stages that you can modify to suit your needs.

Stages represent phases in an organization's selling process. In this example, we demonstrate a process with five stages: Draft, Pending Approval, Approved, Contracted, and Ordered. Your implementation will add or delete stages to accommodate your selling process.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-1.jpeg)

## Ordering stages

An admin can change the order in which stages are evaluated. Select a stage, and then hover over the chevron graphic to alter the order of evaluation. Use the **&lt;** and **&gt;** buttons to change the order. The **+** button creates a new stage at that place in the sequence.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-2.jpeg)

## Transitions between stages

Transitions represent structured movement from one stage to the next in a workflow. Each stage has entry criteria—conditions that must be met before advancing—to ensure consistency and readiness for the next phase.

A transaction cannot automatically transition between stages without an event, which can be represented in the UI as a button, such as **Submit for Approval** or **Revise**. In addition, stage transitions can also be defined for when a new transaction is created or edited.

## Entry criteria

As users progress through the transaction life cycle and execute events tied to transitions, the app evaluates entry criteria to determine which stage applies to the transaction. When an event transition is set to **forward**, CPQ evaluates the entry criteria of the proceeding stages until a stage’s entry criteria are met. If no stages meet the entry criteria, no transition occurs. When an event transition is set to **backward**, the transaction transitions to the stage defined by the administrator without checking its entry criteria. \(Note that the first stage in a process has no entry criteria.\)

For example, a transaction might transition to the **pending approval** stage, or, if approval is not required, it might bypass **pending approval** and move directly to the **approved** stage. This setup can be accomplished using entry criteria.

## Stages and rule groupings

Rule groupings are associated with stages. Rule groupings are executed when the stage is transitioned to and when users update fields or run events while in the stage.

## Stages and views

Stages enable the admin to assign distinct permissions \(views\) to determine how personas observe field data.

For more information about defining views for stages, see [Transaction Manager: Views](transaction-manager-views.md).

## Create a new stage, associate rule groups, and set entry criteria

In the Transaction Manager Admin UI, you start in Stages by default. The defined stages are listed on the page. To create a new stage, click **+ New Stage**.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-1.jpeg)

Enter a name in the **Name** field. As you enter the name, a similar value is entered in the **Variable Name** field. By default, the variable name is the same as the name entered by the admin. However, spaces and special characters are removed from the variable name, which is created using camel case. For example, If you type `Ordered` in the **Name** field, the **Variable Name** field contains **ordered**. To create a custom variable name, click the pencil icon to the right of the field to enter your own value.

Once the name and the variable name are set, click **Save**.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-2.jpeg)

When you click **Save**, you see the stage editor page. In the stage editor, you can assign rule groupings to the stage being created. Use the **Rule Groupings** menu to choose the rule groupings to assign to the new stage.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-3.jpeg)

In the stage editor, in the **Entry Criteria** section, you can create the conditions that are tested before the transaction is allowed to transition into the new stage. The method is the same as the method you use to create conditions in rules. Click **Entry Criteria** to choose the type of condition logic you want to implement.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-4.jpeg)

Click **Take Action When** to select the condition logic.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-5.jpeg)

After you choose the condition logic method, click **+ Add Condition** to add the condition to be tested. You can add multiple conditions to the stage entry criteria. For each conditional statement, choose the field to test, the operator to use, and the value to test for.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-6.jpeg)

When the new stage is fully configured, click **Save**.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-7.jpeg)

## Settings: Behavior on Open Transaction

The **Behavior on Open Transaction** area enables an administrator to determine what rule groupings and integrations run when the user opens a transaction in the stage. Click **Edit Settings**.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-open-1.jpeg)

On the Settings page, use the **Refresh Product Data** toggle to set the product data for the transaction to refresh when the transaction opens.

Click **Add New Action** to add a rule grouping or an integration to the action list.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-open-2.jpeg)

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-open-3.jpeg)

## Settings: Behavior on Idle Timeout

In the **Behavior on Idle Timeout** section of a stage's settings, you can define an event that triggers after a user remains inactive for a time that you specify. This helps improve user experience by executing predefined actions—such as rule groups, integrations, or stage rules—when inactivity is detected.

You can define one such event per stage. If the event fails on its first execution, it is not retried or requeued. To activate this setting, follow these steps:

1.  In the stage's settings, make **Behavior on Idle Timeout** active.

    ![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-idle-1.png)

2.  To add actions, click **Edit Settings** next to **Behavior on Idle Timeout**.

    ![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-idle-2.png)

3.  Set the idle time.

    The **Idle Time Before Actions Run** setting defines how long a user must remain inactive before the configured actions are triggered. The user is considered inactive when there are no clicks, interactions, or key presses.

4.  Add actions to execute on timeout.

    You can define one or more actions that run once the idle timeout is reached. Supported action types include rule groups and integrations.

    -   Use rule groups to execute conditional logic such as updating fields or modifying the UI.
    -   Use integrations to trigger external APIs or services for logging events, sending notifications, or updating external records.

        ![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-idle-3.png)


General guidelines:

-   Carefully set the idle time to balance user convenience with session management and system efficiency.
-   Test all configured rule groups and integrations in a non-production environment before you enable them in live stages.

## Deleting a stage

Deleting a stage is restricted because deleting a stage in use by transactions can cause data issues. Contact Customer Support for more information if a stage deletion is needed.

**Related topics**  


[Transaction Manager: Rules and rule groupings](transaction-manager-rules-and-rule-groupings.md)

[Transaction Manager: Events](transaction-manager-events.md)


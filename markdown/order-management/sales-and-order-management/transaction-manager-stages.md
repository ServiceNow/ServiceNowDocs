---
title: Transaction Manager: Stages
description: Each stage represents a phase in the selling process of an organization. This article illustrates a process with five stages that you can modify to suit your needs.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 6
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Stages

Each stage represents a phase in the selling process of an organization. This article illustrates a process with five stages that you can modify to suit your needs.

Stages represent each phase in an organization's selling process. The stage list shows all stages defined, and their order of evaluation. In this example, we demonstrate a process with five stages. Your implementation will add or delete stages to accommodate your selling process.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-1.jpeg)

The administrator may change the order of evaluation in any stage. Hover over the chevron graphic to alter the order of evaluation. '&lt;' and '&gt;' buttons change the order of stages. The '+' button will create a new stage at that place in the sequence of stages.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-2.jpeg)

## Transitions between stages

Transitions between stages represent the structured movement from one stage to the next in a workflow. Each stage has entry criteria—conditions that must be met before advancing—to ensure consistency and readiness for the next phase.

A transaction cannot transition between stages automatically without an event. In addition, stage transitions may also be defined for "Create New Transaction" or "Edit Transaction \(Open\)" events.

For example, transition between various stages is possible with the help of events. Events may be represented in the UI as buttons, such as “submit for approval”, ”revise”, and so on.

## Entry criteria

Entry criteria determine when a stage will be accessed. As users progress through the transaction life cycle and execute events tied to transitions, the app tests stage entry criteria to determine which stage applies to the transaction next. When an event transition is set to ‘forward,' ServiceNow CPQ evaluates the entry criteria of the proceeding stages, according to the stage order, until a stage’s entry criteria are met. If no stages meet the entry criteria, no transition will occur. When an event transition is set to "backward," the transaction transitions to the stage defined by the administrator without checking its entry criteria.

For example, a transaction transitioning to stage ‘pending approval’ when an approval is required and pending or bypassing the stage ‘pending approval’ and moving to stage ‘approved’ if approval is not required. This could be accomplished with entry criteria.

**Note:** The first stage in a process has no entry criteria.

## Stages and rule groupings

Rule groupings are associated to stages and are run on when the stage is transitioned to and when users update fields or run events while on that stage.

## Stages and views

Stages allow the Admin to define how personas observe field data with distinct permissions \(views\).

Transaction Manager enables admins to configure distinct field data views for personas, each with specific permissions. For more information on defining views for stages, see [Transaction Manager: Views](transaction-manager-views.md).

## Create a new stage, associate rule groups, and set entry criteria

Navigate to the Transaction Manager Admin UI. By default you are placed in the Stages option of the Admin menu. You should see the defined stages displayed on the page. To create a new stage, click **+ New Stage**.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-1.jpeg)

Enter a name in the Name field. As the name is being entered in the Name field, the same value is being mirrored in the Variable Name field. By default, Transaction Manager makes the variable name the same as the name that the Admin enters. However, the Variable name is created using camel case, and all spaces and special characters are removed from the name. For example, If you type “Ordered” in the Name field, the Variable Name field will contain “ordered”. If you want to create your own custom variable names, click the pencil icon to the right of the Variable Name field and you can enter your own value.

Once the Name and Variable Name are set, click **Save**.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-2.jpeg)

Once you click **Save**, you will be brought to the Stage Editor page. In the Stage Editor, you can assign rule groupings to the stage being created. Use the Rule Groupings menu to choose the rule groupings you would like to assign to the new stage.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-3.jpeg)

On the Stage Editor page, under Entry Criteria, you can create the conditions that will be tested before the transaction is allowed to transition into this new stage. The creation of the conditions follows the same procedure as creating conditions in rules. Choose the type of condition logic you want to implement by clicking **Entry Criteria**.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-4.jpeg)

Click **Take Action When** to select the condition logic.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-5.jpeg)

Once the condition logic method is chosen, click **+ Add Condition** to add the specific condition statement that is to be tested. You can add multiple conditions to the stage entry criteria. For each conditional statement, choose the field you want to test, the operator to use, and the value to test for in order to create a complete conditional statement.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-6.jpeg)

Once all conditions are added, and all other changes to the new stage are complete, click **Save** to save the new stage and all its settings.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-7.jpeg)

## Settings: Behavior on Open Transaction

The Behavior on Open Transaction area allows the Administrator to determine what rule groupings and integrations will run when the user opens the transaction and the transaction happens to be in this stage. Click **Edit Settings** to choose the Rule groupings or Integrations you would like to fire when the transaction is opened in this stage.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-open-1.jpeg)

On the Settings page for the Behavior on Open Transaction, use the Refresh Product Data toggle to refresh the product data for the transaction upon opening the transaction.

Click **Add New Action** to add a Rule grouping or Integration to the Action list for the Behavior on Open Transaction for the new stage.

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-open-2.jpeg)

![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-open-3.jpeg)

## Settings: Behavior on Idle Timeout

The Behavior on Idle Timeout feature allows you to define a single event per stage that is triggered after a user remains inactive for a specified time period. This helps improve user experience by executing predefined actions—such as rule groups, integrations, or stage rules—when inactivity is detected.

-   Only one Idle Timeout event is allowed per stage.
-   The idle time can be adjustable.
-   If the event fails on its first execution, it will not be retried or requeued.
-   The event can be set as active or inactive per stage.

Idle timeout is configured in a stage’s settings, under the section titled:``

“Behavior on Idle Timeout” \(found at the bottom right of the stage editor\).

1.  To activate the setting, navigate to the relevant stage.
2.  Locate “Behavior on Idle Timeout.”

    ![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-idle-1.png)

3.  Toggle the setting to Active.
4.  Click **Edit Settings** beside it to add the actions.

    ![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-idle-2.png)

5.  Set the idle time.

    The setting “Idle Time Before Actions Run” defines how long a user must remain inactive \(no clicks, typing, or interactions\) before the configured actions are triggered.


You can define one or more actions that run once the idle timeout is reached. Supported action types include:

-   Rule groups

    Use rule groups to execute conditional logic such as:

    -   Updating fields
    -   Modifying the UI
-   Integrations

    Use integrations to trigger external APIs or services for:

    -   Logging events
    -   Notifying external systems
    -   Updating external records

        ![Transaction Manager: stages](../images/cpq-txn-mgr-stages-create-behavior-on-idle-3.png)


Best practices:

-   Set the idle time carefully to balance user convenience with session management and system efficiency.
-   Test all configured Rule groups and Integrations in a non-production environment before enabling them in live stages.

## Deleting a stage

Deleting a stage is restricted due to potential data issues created by deleting a stage in use by transactions. Contact Customer Support for more information if a stage deletion is needed.


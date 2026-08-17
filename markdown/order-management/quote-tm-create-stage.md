---
title: Create a quote transaction stage
description: Create a stage in the ServiceNow Quote Experience administration interface to define a phase in the quoting process, set entry criteria, and configure what happens when a user opens a transaction or remains inactive in that stage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/quote-tm-create-stage.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 4
breadcrumb: [Stages, CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a quote transaction stage

Create a stage in the ServiceNow Quote Experience administration interface to define a phase in the quoting process, set entry criteria, and configure what happens when a user opens a transaction or remains inactive in that stage.

## Before you begin

Role required: admin

## About this task

A stage represents a phase in the quote lifecycle, from creation through completion. Each stage controls when and how transactions progress through the quote process. You can define entry criteria to control when a transaction can enter a stage, configure what happens when a user opens a transaction at that stage, and specify automated actions that occur if a user remains inactive for a defined period. Stages can be associated with rule groupings and integrations to apply business logic at specific points in the workflow.

When creating a stage, you assign it a variable name that serves as a unique identifier throughout the system—this variable name cannot be changed after creation. To configure stages, you can start by setting up stage properties and entry criteria first, then create and add rule groupings or integrations to the stage afterward.

## Procedure

1.  Navigate to **All** &gt; **CPQ Administration** &gt; **Transaction** &gt; **Stages**.

    The Stages list is displayed by default.

2.  Select **+ New Stage**.

3.  In the **Name** field, enter the name of the new stage.

    As you type, the name is mirrored in the **Variable Name** field in camel case with spaces and special characters removed. For example, entering `Pending Approval` produces the variable name **pendingApproval**. To enter a custom variable name, select the pencil icon to the right of the **Variable Name** field.

4.  Select **Save**.

    The stage editor opens with three configurable areas: rule groupings, entry criteria, and stage settings.

5.  To associate rule groupings with the stage, use the **Rule Groupings** menu to select the rule groupings to assign.

    Rule groupings assigned to a stage execute when the stage is entered and when users update fields or run events while in the stage.

6.  To configure entry criteria, select **Entry Criteria** and then select **Take Action When** to choose the condition logic method.

    -   Select **Always True** if the stage has no entry conditions.
    -   Select **Any Conditions are Met** to advance when any condition is true \(OR logic\).
    -   Select **All Conditions are Met** to advance only when all conditions are true \(AND logic\).
    -   Select **Custom Logic** to combine AND and OR logic using parentheses.
7.  Select **+ Add Condition** to add each condition.

    For each condition, select the field to test, the operator, and the test value.

8.  Select **Save** to save the stage configuration.

9.  In the **Behavior on Open Transaction** area of the stage editor, select **Edit Settings**.

    This area controls which rule groupings and integrations run when a user opens a transaction in this stage.

10. Enable the **Refresh Product Data** toggle to refresh the transaction's product data each time a user opens the transaction in this stage.

11. Select **Add New Action** and choose a rule grouping or integration to run when the transaction opens.

    Repeat this step for each additional action to run on open.

12. In the **Behavior on Idle Timeout** area of the stage editor, activate the toggle to enable idle timeout for this stage.

    Idle timeout defines an action that triggers after a user is inactive for a period you specify. A user is considered inactive when there are no clicks, interactions, or key presses. You can define one idle timeout event per stage. If the event fails on its first execution, it is not retried or requeued.

    **Tip:** Set the idle time carefully to balance user convenience with session management and system efficiency. Test all configured rule groupings and integrations in a non-production environment before enabling them in live stages.

13. Select **Edit Settings** next to **Behavior on Idle Timeout**.

14. In the **Idle Time Before Actions Run** field, enter the period of inactivity that must pass before the configured actions trigger.

15. Select **Add New Action** and choose the action type to run on timeout.

    |Action type|Use when|
    |-----------|--------|
    |**Rule group**|You need to execute conditional logic on timeout, such as updating fields or modifying the quote UI. For more information, see [Quote transaction rules and rule groupings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-rules-and-rule-groups.md)|
    |**Integration**|You need to call an external API or service on timeout, such as logging inactivity events, sending notifications, or updating external records. For more information, see [Quote transaction integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-integrations.md)|

    Repeat this step for each additional action to run on timeout.

16. Select **Save** to save all stage settings.

    The stage is saved with its rule groupings, entry criteria, and configured stage behaviors. The stage is available in the Stages list and can be associated with a blueprint layout.



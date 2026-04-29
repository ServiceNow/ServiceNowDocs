---
title: Transaction Manager: Events
description: Events such as transaction creation, modification, and deletion can be set to trigger rule groups or integrations and to move a transaction from one stage to another.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Transaction Manager, CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Transaction Manager: Events

Events such as transaction creation, modification, and deletion can be set to trigger rule groups or integrations and to move a transaction from one stage to another.

Events are a way to trigger stage rules and integrations or rule groups. These events are usually activated by buttons or API on a layout helping a user to transition from one stage to another.

## System events

System events are frequently used behaviors available for customers out of the box.

Transaction \(header\)

When Transaction Manager is embedded in a CRM, the user is presented with a button in the CRM UI corresponding to these Transaction events. When the user clicks one of these buttons, the CRM calls corresponding CPQ API:

-   Create Transaction: Event triggered to create a new transaction.
-   Edit Transaction: Allows editing an existing transaction, enabling stage-based rule and integration actions.
-   Copy Transaction: Event to clone a transaction and its line items.
-   Upsert Lines: This event manages the creation/update of transaction lines after the user browses catalog \(UI Effect "productSearch"\) to add new lines or reconfigures an existing line. Upsert Lines is automatically run after the user finishes selecting products from the catalog, configuring products, or reconfiguring \(UI Effect “reconfigure”\). Although this event works on lines with the transaction, it works at the transaction level, on all lines in the transaction.

    For more information about UI Effects, see [Transaction Manager: Layouts - UI effects](transaction-manager-layouts-ui-effects.md).

-   Delete Transaction: Event triggered to delete an existing transaction.

Transaction Line:

Transaction Manager line-level events are represented on the native CPQ Transaction Manager UI as buttons:

-   Clone Line: Clones a line and its children, but only for top-level lines in the transaction. Header-level rules also apply after cloning.
-   Delete Lines: Deletes one or more lines from a transaction; UI supports selecting lines, and IDs can be passed in headless mode.

## Event APIs

Event APIs are authorized via session cookie only.

**Warning:** Avoid building a scenario in which the user initiates an event that fires an event API on the same transaction. Because both the UI and the APIs are acting upon the same record, such an implementation can result in unpredictable behavior.

## Custom events

In addition to system events, the admin can define custom events to meet business-specific requirements. To create a custom event, follow these steps.

1.  In Transaction Manager Admin, click **Events**, and then click **+ New Event**.

    ![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-new-1.png)

2.  In the New Event window, enter a name. As the name is entered, it is mirrored in the **Variable Name** field. By default, the variable name is the same as the entered name, but in camel case with all spaces and special characters removed. For example, if you enter the name Total of Manufacturing Lines, the automatically entered variable name is totalOfManufacturingLines. To create a custom variable name, click the pencil icon to the right of the variable name field and enter your own value.

    ![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-new-2.jpeg)

3.  Select the **Transaction Line** level, and then click **Save**.

The event editor opens. By default, events have their event access set to No Access. Click **Edit Event Access**, change the event access level to **Active**, and then click **Done** to return to the event editor.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-total-3.jpeg)

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-access-4.jpeg)

In the Actions area, you can assign either rule groupings or integrations to fire when the event is triggered. To add a new action to the event, click **+ Add New Action** and choose either rule groupings or integration. A menu of the available rule groupings or integrations appears. Choose the rule grouping or integration to apply to the event. You can add multiple rule groupings or integrations to the same event.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-rule-grouping-5.jpeg)

Use the **Transition** toggle to determine whether the event transitions the transaction forward or backward in the stage sequence. By default, the event does not transition the transaction to another stage. Clicking the **Transition** toggle enables the transition function.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-run-stage-rules-6.jpeg)

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-run-stage-rules-7.jpeg)

When you're finished, click **Save**. The new event appears in the event list as either a transaction-level event or a transaction line-level event, depending on which level you chose when the event was created.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-final.png)

## Event settings: Validate configured items

The **Validate configured items** setting on custom header events validates product configurations in the transaction when the event executes. Validation occurs before event actions, which execute regardless of the validation status.

The setting includes a validity period that excludes products validated within a time frame. For example, if the validity period is set to 15 days and a product was validated 7 days ago, the product does not have its configuration validated. If a product was validated 20 days ago, the product has its configuration validated.

Two line-level system fields support this function: **txn.line.configuration.status** \(Boolean\) and txn.line.configuration.validatedAt \(date\).

**Related topics**  


[Transaction Manager: Rules and rule groupings](transaction-manager-rules-and-rule-groupings.md)

[Transaction Manager: Stages](transaction-manager-stages.md)


---
title: Transaction Manager: Events
description: Events can be triggered in the UI, such as by button clicks, or by API. They can trigger Stage Rules and Integrations or Rule Groups.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-11-14"
reading_time_minutes: 5
breadcrumb: [Transaction Manager, ServiceNow CPQ, Configure, price, quote, Explore, Sales Customer Relationship Management]
---

# Transaction Manager: Events

Events can be triggered in the UI, such as by button clicks, or by API. They can trigger Stage Rules and Integrations or Rule Groups.

Events are a way to trigger certain Stage Rules and Integrations or Rule Groups. These events are usually activated by buttons or API on a layout helping a user to transition from one stage to another.

## System events

System events are frequently-used behaviors available for customers out of the box.

Transaction \(header\)

When Transaction Manager is embedded in a CRM, the user is presented with a button in the CRM UI corresponding to these Transaction Events. When the user clicks one of these buttons, the CRM calls corresponding ServiceNow CPQ API:

-   Create Transaction: Event triggered to create a new transaction.
-   Edit Transaction: Allows editing an existing transaction, enabling stage-based rule and integration actions.
-   Copy Transaction: Event to clone a transaction and its line items.
-   Upsert Lines: This event manages the creation/update of transaction lines after the user browses catalog \(UI Effect "productSearch"\) to add new lines or reconfigures an existing line. Upsert Lines is automatically run after the user finishes selecting products from the catalog, configuring products, or reconfiguring \(UI Effect “reconfigure”\). Although this Event works on lines with the Transaction, it works at the Transaction level, on all lines in the Transaction.

    For more information about UI Effects, see [Transaction Manager: Layouts - UI effects](transaction-manager-layouts-ui-effects.md).

-   Delete Transaction: Event triggered to delete an existing transaction.

Transaction Line:

Transaction Manager Line-level Events are represented on the native ServiceNow CPQ Transaction Manager UI as buttons:

-   Clone Line: Clones a line and its children, but only for top-level lines in the transaction. Header-level rules will also apply after cloning. \[Does it clone all of the field-level data\]
-   Delete Lines: Deletes one or more lines from a transaction; UI supports selecting lines, and IDs can be passed in headless mode.

## Event APIs

Currently, Event APIs are authorized via session cookie only.

**Warning:** Creative implementers may be curious to build a scenario in which the user on transaction X initiates an event that fires an Event API on the same transaction. Such an implementation can result in unpredictable behavior, as both UI and APIs are acting upon the same record. ServiceNow CPQ Development is aware of this potential conflict and intends to mitigate it in the future. This release will be announced in Build Notes under "Transaction Locking." In the interim, do not set up this scenario.

## Custom events

In addition to system events, the Admin defines custom events to meet their company's business-specific requirements. To create a custom event, follow these steps.

1.  Navigate to the Transaction Manager Admin UI. From the Admin menu on the left of the Admin UI, click **Events**. Click **+ New Event** to create a new custom Event.

    ![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-new-1.png)

2.  Enter a name in the Name field. As the name value is being entered in the Name field the same value is being mirrored in the Variable Name field. By default, Transaction Manager makes the Variable name the same as the name value that the Admin enters. The Variable name however is created using “camel case” and all spaces and special characters are removed from the name. For example, If you type “Total of Manufacturing Lines” for the Name field, the Variable Name field will contain “totalOfManufacturingLines”. If you want to create your own custom Variable names, click the pencil icon at the right end of the Variable Name field and you will be allowed to enter your own value for Variable name.

    ![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-new-2.jpeg)

3.  4.  
This will be a Transaction Line level Event, so click **Transaction Line** under Select a Level, and then click **Save**.

After clicking the Save button, you will be brought to the Event Editor page. All Events are created with their Event Access set to No Access. Click the Edit Event Access button to change the event access level to Active. After you have set the Access level to Active, click **Done** to return to the Event Editor.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-total-3.jpeg)

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-access-4.jpeg)

In the Actions area of the Event Editor you can assign either Rule Groupings or Integrations to fire when the event is triggered. To add a new Action to the event, click **+ Add New Action** and choose either Rule Groupings or Integration. Regardless of which you choose, you will be given a menu of the available Rule Groupings or Integrations that have been created in Transaction Manager. Choose the Rule Grouping or Integration to apply to the event. You can add multiple Rule Groupings or Integrations to the same Event.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-rule-grouping-5.jpeg)

Also in the Action area is the Transition toggle. Use this toggle to determine if the event will cause the Transaction to transition either forward or backward in the Stage sequence. By default, the event will not cause the transition of the Transaction to another Stage. Clicking the Transition toggle will enable the transition function, and will allow you to choose whether the transition will move the Transaction forward in the Stage sequence or backward in the Stage sequence.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-run-stage-rules-6.jpeg)

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-run-stage-rules-7.jpeg)

Once all of the changes to the event have been completed in the Event Editor, click theSavebutton to save the changes. The new Event will now show up on the event list as either a Transaction level Event or a Transaction Line level Event depending on which level was chosen during the creation process.

![Transaction Manager: Events](../images/cpq-txn-mgr-rules-events-custom-final.png)

## Event settings

Validate the configured Items.

-   Validate configured items is a setting on custom header events that,when enabled, will validate configurations of products in the transaction on event execution. The validation occurs prior to the event actions and the event actions will execute regardless of the validation status.
-   The setting has a ‘Validity period’ which will exclude products validated in that time frame.

    For example, if the validity period is set to 15 days and a product had been validated 7 days prior, that product would not have its configuration validated. If a product had been validated 20 days prior, that product would have it configuration validated.

-   Two line-level system fields support this function:
    -   txn.line.configuration.status- will be ‘valid’ or ‘invalid’ depending on result of configuration validation
    -   txn.line.configuration.validatedAt- date of the last validation


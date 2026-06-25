---
title: Create a manual fallout record
description: Create a fallout record manually for an order task that has a condition or issue that prevents it from being completed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/create-manual-order-fallout-record.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing order fallout, Order Management, Use, Sales Customer Relationship Management]
---

# Create a manual fallout record

Create a fallout record manually for an order task that has a condition or issue that prevents it from being completed.

## Before you begin

Role required: sn\_fallout\_mgmt.fallout\_manager

## About this task

You can create manual records as needed basis so that you can raise awareness of an issue or condition that is preventing order fulfillment. By creating a record manually, you can also assign it to a person for resolution.

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace** .

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Customer Orders** &gt; **All** or **Service Orders** &gt; **All**.

4.  Select and open an existing customer or service order.

5.  To view the line item details, select **Line Items** where \(n\) represents the number of the total number of line items for the order.

6.  In the Order Line Items form, select the order line item that you want to review.

7.  Select the **Order Tasks** tab.

8.  In the Order Tasks form, select the order tasks that you want to review.

9.  When you finish updating the order task, or encounter issues preventing its closure, select the more options icon \[Omitted image "more-options.png"\] Alt text: and then select **Create Fallout**\).

10. On the form, fill in the fields.

    For information about field descriptions, see the Create Fallout form fields section in [Field descriptions for Fallout Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/fields-create-fallout-form.md).

11. Select **Save**.


## Result

When you create a manual fallout record, or an automated one is generated, the following occurs in the related order task:

-   Its **State** field changes to On hold, with a comment on which logged-in user caused it to change.
-   In the Activity section, a work order note indicates that the order task state has changed from its former state, usually In Progress, to On hold. A work order note with the message `A fallout record FOnnnn has been created` also appears.

**Parent Topic:**[Managing order fallout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/fallout-management-overview.md)

**Related topics**  


[Fallout Management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-fallout-management.md)

[Flow Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/flow-designer.md)

[Flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/flows.md)

[Create a flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/create-flow.md)


---
title: Order Line Milestone Data Model
description: The Order Line Milestone table stores milestone records created at order fulfillment time. Understand the table structure, field definitions, and relationships to milestone definitions and order line items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/order-line-milestones-data-model.html
release: australia
topic_type: reference
last_updated: "2026-09-17"
reading_time_minutes: 3
keywords: [order line milestone table, data model, fields, schema]
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Order Line Milestone Data Model

The Order Line Milestone table stores milestone records created at order fulfillment time. Understand the table structure, field definitions, and relationships to milestone definitions and order line items.

## Order Line Milestone table overview

The Order Line Milestone table \(`sn_ind_tmt_orm_order_line_milestone`\) stores milestone records created when orders are submitted. Each record represents a single milestone event on a single order line item.

Records are created by the **Create Order Line Milestones** business rule during order submission. They aren't created manually; they are driven by the **Milestone Flow Policy** decision table.

## Table structure

The table has the following key fields:

|Field|Type|Required|Description|
|-----|----|--------|-----------|
|**Number**|Auto Number|Yes|System-generated unique identifier \(for example, OLMS0001002\). Begins with OLMS.|
|**Milestone**|Reference to Milestone|Yes|Reference to the milestone definition this record is tied to. Set by the Milestone Flow Policy decision table.|
|**Order Line Item**|Reference to Order Line Item|Yes|Reference to the order line item this milestone applies to. Set when the record is created.|
|**Status**|Choice|Yes|Current state: `Open` \(initial state on creation\) or `Reached` \(when milestone is marked complete\).|
|**Sequence**|Integer|No|Optional sequencing value to indicate the order in which milestones are typically reached \(for example, 1, 2, 3\). Useful for reporting and workflow logic.|
|**Milestone reached date**|Date/Time|No|The date and time the milestone transitioned to `Reached` status. Empty until the milestone is marked as reached \(either manually or by a fulfillment flow\).|

## Relationships

-   **Milestone \(Parent\)**

    Each order line milestone references a Milestone record. The milestone definition provides the template—name, description, active status—that the order line milestone inherits.

-   **Order Line Item \(Parent\)**

    Each order line milestone belongs to exactly one order line item. When you view an order line in Workspace, milestones for that line appear in the **Order Line Milestones** related list.

-   **Customer Order \(Ancestor\)**

    Indirectly, through the order line item. You can trace back to the parent order to understand the broader fulfillment context.


## Record creation and updates

**Creation:** Records are created automatically during order submission by the **Create Order Line Milestones** business rule. The rule:

1.  Iterates through each order line in the submitted order.
2.  Passes the order and order line to the **Milestone Flow Policy** decision table.
3.  For each matching decision row, creates a new order line milestone record with the determined milestone.
4.  Sets initial status to `Open` and leaves **Milestone reached date** empty.

**Updates:** Order line milestone records are typically updated to set status to `Reached` when:

-   A user clicks the **Mark as Reached** UI action on the milestone form.
-   A fulfillment flow executes the **Set Order Line Milestone to Reached** action in response to a business event \(for example, domain order closure or characteristic update\).

When status changes to `Reached`, the **Milestone reached date** field is automatically populated with the current date and time.

## Accessing the table

To query or customize the Order Line Milestone table in the platform:

-   Table name: `sn_ind_tmt_orm_order_line_milestone`
-   In Workspace: Navigate to **Order Milestone Setup** → **Order Line Milestones** \(admin view only\) or view the related list on any order line item \(end-user view\).
-   In reports or queries: Reference the table by its system name `sn_ind_tmt_orm_order_line_milestone` to filter or aggregate milestone data.

## Related tables

-   **Milestone \(`sn_ind_tmt_orm_milestone`\)**

    The configuration-time milestone definitions. Each milestone record is referenced by one or more order line milestones.

-   **Order Line Item \(`sn_ind_tmt_orm_order_line_item`\)**

    Parent table. Each order line item can have multiple order line milestones.

-   **Customer Order \(`sn_ind_tmt_orm_order`\)**

    Ancestor table \(through order line item\). Provides order context \(account, order type, status, etc.\).



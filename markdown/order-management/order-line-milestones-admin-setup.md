---
title: Set Up Order Line Milestones
description: Enable milestone creation for your instance, define milestone records, and configure the decision table so milestones are assigned to order lines at fulfillment time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/order-line-milestones-admin-setup.html
release: australia
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 3
keywords: [milestone setup, admin, decision table, configuration]
breadcrumb: [Creating orders, Order Management, Use, Sales Customer Relationship Management]
---

# Set Up Order Line Milestones

Enable milestone creation for your instance, define milestone records, and configure the decision table so milestones are assigned to order lines at fulfillment time.

## Before you begin

You must have admin access to Order Management and permission to:

-   Modify system properties
-   Create milestone records
-   Edit the Milestone Flow Policy decision table
-   Manage business rules

Role required: sn\_ind\_tmt\_orm.order\_agent

## About this task

Order line milestones are inactive by default. To use milestones in your fulfillment process, enable the feature, create your milestone definitions, and configure the decision table that assigns milestones to order lines.

## Procedure

1.  Enable the milestone creation feature.

    Navigate to **System Properties** and search for **sn\_ind\_tmt\_orm.enable\_order\_line\_milestones\_on\_fulfillment**. Set the value to **true**. When enabled, the **Create Order Line Milestones** business rule will run on order submission and create order line milestone records.

2.  Create milestone definitions.

    In Workspace, open the **Order Milestone Setup** section and select **Order Milestone**. Select **New** to create a milestone record.

    Fill in the following fields:

    -   **Number** — Auto-generated. Begins with MS \(for example, MS0001012\).
    -   **Name** — Descriptive name for the milestone \(for example, "SIM card added" or "Domain order closed"\).
    -   **Description** \(optional\) — Additional context about when this milestone applies or what it represents.
    -   **Active** — Check this box to enable the milestone for use in the decision table.
    Select **Save**.

3.  Configure the Milestone Flow Policy decision table.

    The **Milestone Flow Policy** decision table controls which milestone is assigned to each order line. Open this table from **Workflow Studio** under the Order Management application.

    Review the table structure:

    -   **Inputs:** Customer Order and Order Line Item \(mandatory\).
    -   **Conditions:** Product Offering, Specification, and Action. These define the criteria for assigning a milestone.
    -   **Results:** The Milestone record that will be created for matching order lines.
4.  Add a decision row for each product or scenario.

    Select **Add new decision row** to create a row in the decision table.

    Set the conditions:

    -   **Product Offering:** Select the product offering from the order line item \(for example, "Managed Connectivity Services Supreme Bundle"\).
    -   **Specification:** \(optional\) If only certain specifications should trigger a milestone, specify here \(for example, "DSL Access Service"\).
    -   **Action:** The action type on the customer order \(for example, "Add" or "Change"\).
    Set the result to the milestone definition this row should assign. For **Milestone**, choose the milestone \(for example, "Managed Connectivity Services Supreme Bundle"\).

    Repeat for each product, specification, or action combination you want to handle.

5.  Set a default result \(optional\).

    If no decision rows match an order line, the decision table can return a default milestone or no result. In the decision table, you can specify a **Default result** milestone. If left empty, no order line milestone is created for that order line.

6.  Save and test the decision table.

    Select **Save** on the decision table. Select **Test** to verify the table logic by providing sample customer order and order line item inputs. Confirm the table returns the expected milestone.

7.  Verify the business rule status.

    Navigate to **business rules** and search for **Create Order Line Milestones**. Confirm it is **Active**.

    This rule runs when a customer order is submitted and triggers the decision table to create order line milestone records.


## Result

Milestones are now set up. When customers submit orders with products matching your decision table conditions, order line milestones are automatically created with status **Open**. Users can then mark them as reached as fulfillment progresses.

## What to do next

Next, you can configure fulfillment flows to use the **Set Order Line Milestone to Reached** action. This action automatically marks milestones as reached when business conditions are met, such as when a domain order closes or a characteristic is updated.


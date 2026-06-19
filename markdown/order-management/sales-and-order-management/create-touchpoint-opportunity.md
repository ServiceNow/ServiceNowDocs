---
title: Create a touchpoint from an opportunity
description: Create a touchpoint to log a customer interaction directly from an opportunity record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/create-touchpoint-opportunity.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Manage touchpoints, Opportunity Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Create a touchpoint from an opportunity

Create a touchpoint to log a customer interaction directly from an opportunity record.

## Before you begin

-   The CRM Touchpoints plugin \(sn\_crm\_touchpoint\) must be installed.
-   The opportunity must be in a non-closed state. You can't create touchpoints for opportunities in a Closed-Won or Closed-Lost stage.

Role required: sn\_crm\_touchpoint.admin or sn\_crm\_touchpoint.touchpoint\_writer

## About this task

Touchpoints are interaction records that you associate with a specific opportunity. When you create a touchpoint from the opportunity, the system automatically links the touchpoint to that opportunity and populates customer context from the opportunity record.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  In the **Opportunity - All** list, open the opportunity record.

3.  In the opportunity header, select **Create** &gt; **Touchpoint**.

    **Note:** The **Create** button and the Touchpoint option are only visible when you have permission to create CRM Touchpoints. The button is hidden when the opportunity is in a closed state.

4.  In the touchpoint form, complete the required fields.

    The following fields are automatically set and can't be edited:

    -   **Associated entity**: set to Opportunity
    -   **Associated record**: set to the opportunity number
    -   **Category**: set to Sales
    -   **Owner**: set to the user creating the touchpoint
    If the opportunity is account-based, the system also sets **Account** from the opportunity. The **Contact** field is pre-populated from the opportunity contact if one exists, and remains editable.

5.  Select **Save**.


## Result

The touchpoint is created and linked to the opportunity. It appears in the **Touchpoints** tab of the opportunity record.

## What to do next

To view all touchpoints for the opportunity, select the **Touchpoints** tab.

**Parent Topic:**[Manage touchpoints on an opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/manage-touchpoints-opportunity.md)


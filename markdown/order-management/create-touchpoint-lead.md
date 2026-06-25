---
title: Create a touchpoint from a lead
description: Create a touchpoint to log a customer interaction directly from a lead record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/create-touchpoint-lead.html
release: australia
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [Manage touchpoints, Lead Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Create a touchpoint from a lead

Create a touchpoint to log a customer interaction directly from a lead record.

## Before you begin

-   The CRM Touchpoints plugin \(sn\_crm\_touchpoint\) must be installed.
-   The lead must be in a non-closed state. You can't create touchpoints for leads in a Qualified or Disqualified stage.

Role required: sn\_crm\_touchpoint.admin or sn\_crm\_touchpoint.touchpoint\_writer

## About this task

Touchpoints are interaction records that you associate with a specific lead. When you create a touchpoint from the lead, the system automatically links the touchpoint to that lead and populates customer context from the lead record.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  Navigate to **Leads** &gt; **All** and open the lead record.

3.  In the lead header, select **Create** &gt; **Touchpoint**.

    **Note:** The **Create** button is only visible when you have permission to create CRM Touchpoints and the lead is in a non-closed state.

4.  In the touchpoint form, complete the required fields.

    The following fields are automatically set and can't be edited:

    -   **Associated entity**: set to Lead
    -   **Associated record**: set to the lead number
    -   **Category**: set to Pre-Sales
    -   **Owner**: set to the user creating the touchpoint
    -   **Account**: set from the lead account if available, and read-only
    -   **Contact**: set from the lead contact if available, and read-only
    If the lead account or contact changes, the system updates the account and contact on all non-closed touchpoints associated with that lead.

5.  Select **Save**.


## Result

The touchpoint is created and linked to the lead. It appears in the **Touchpoints** tab of the lead record.

## What to do next

To view all touchpoints for the lead, select the **Touchpoints** tab.

**Parent Topic:**[Manage touchpoints on a lead](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-touchpoints-lead.md)

**Related topics**  


[CRM Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-crm-touchpoints.md)

[Install CRM Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-crm-touchpoints.md)

[Create new CRM touchpoint form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-crm-touchpoint-form.md)


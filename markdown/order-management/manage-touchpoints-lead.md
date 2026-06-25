---
title: Manage touchpoints on a lead
description: View, create, and delete touchpoints associated with a lead from the touchpoints related list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/manage-touchpoints-lead.html
release: australia
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 1
breadcrumb: [Lead Management, Lead and opportunity apps, Use, Sales Customer Relationship Management]
---

# Manage touchpoints on a lead

View, create, and delete touchpoints associated with a lead from the touchpoints related list.

## Before you begin

The CRM Touchpoints plugin \(sn\_crm\_touchpoint\) must be installed.

Role required: sn\_crm\_touchpoint.admin or sn\_crm\_touchpoint.touchpoint\_writer

## About this task

The **Touchpoints** tab on a lead record displays all touchpoints associated with that lead. You can create new touchpoints or delete existing ones directly from this list.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  Navigate to **Leads** &gt; **All** and open the lead record and select the **Touchpoints** tab.

    The list displays all touchpoints associated with the lead.

3.  To create a touchpoint, select **New** in the related list Or select **Create Touchpoint** from the Lead header.

    **Note:**

    -   The **New** button is available when you have permission to create CRM Touchpoints.
    -   If the lead is in a Qualified or Disqualified stage, an error message appears when you attempt to save the new touchpoint.
4.  To delete one or more touchpoints, select the checkbox next to each touchpoint and then select **Delete**.

    **Note:**

    -   The **Delete** button is available to users with touchpoint\_admin permission and is only active when at least one touchpoint is selected.
    -   A confirmation prompt appears before the deletion completes.
    The selected touchpoints are removed from the lead.


## Result

Changes are saved to the lead. The Touchpoints tab reflects the current state of all linked touchpoints.

-   **[Create a touchpoint from a lead](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-touchpoint-lead.md)**  
Create a touchpoint to log a customer interaction directly from a lead record.

**Parent Topic:**[Using Lead Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/lead-management-using.md)

**Related topics**  


[CRM Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-crm-touchpoints.md)

[Install CRM Touchpoints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-crm-touchpoints.md)

[Manage touchpoints on an opportunity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/manage-touchpoints-opportunity.md)

[Create new CRM touchpoint form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/create-crm-touchpoint-form.md)


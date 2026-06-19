---
title: Create a customer success definition record
description: Define categories and subcategories for success play workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-create-ale-defn.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Getting started, Customer success, Configure, Customer Success Management]
---

# Create a customer success definition record

Define categories and subcategories for success play workflows.

## Before you begin

-   Define and configure the subflow that triggers the success workflow before starting.
-   Role required: sn\_acct\_lc.ale\_success\_play\_admin

## About this task

The customer success definition table controls what appears in the success play workflow. The category and sub-categories that appear in the success play correspond to a customer success definition record that matches the selected category. When you select a success play, the selected linked flow runs and creates a record in the target table, triggers a playbook, or performs another action as specified in the subflow.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace**and select the **List** icon.

2.  Navigate to the **Customer Success** &gt; **Customer Success Definition** and select **New**.

3.  On the form, fill in the fields.

<table id="table_ddj_yyb_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Flow

</td><td>

Subflow triggered by this Customer Success definition record. Must be defined and configured in Flow Designer.

</td></tr><tr><td>

Category

</td><td>

Category that groups related plays in the success play workflow launcher. Available categories:-   Onboarding
-   Risk Management
-   Success Planning
-   Success Support


</td></tr><tr><td>

Sub category

</td><td>

Subcategory filtered by the selected category.

</td></tr><tr><td>

State

</td><td>

State of this Customer Success definition record:-   Draft
-   Published
-   Closed
-   Canceled


</td></tr><tr><td>

Order

</td><td>

Order in which categories appear in the workflow launcher pages.

</td></tr><tr><td>

Title

</td><td>

Title of the workflow launcher item.

</td></tr><tr><td>

Description

</td><td>

Purpose of this workflow launcher item.

</td></tr></tbody>
</table>4.  Set the state of this record to **Published** and select **Save**.

    The success play is available when the **Create success play** option is selected. See [Create a success play](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-create-success-play.md) for details.


**Parent Topic:**[Getting started with Customer Success](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-basic-config.md)


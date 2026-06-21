---
title: Create a customer success choice record
description: Create a Customer Success Choice record to define a value for a dropdown or lookup field in the Customer Success Management application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/customer-success-management/account-lifecycle-ale-choice.html
release: australia
product: Customer Success Management
classification: customer-success-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Getting started, Customer success, Configure, Customer Success Management]
---

# Create a customer success choice record

Create a Customer Success Choice record to define a value for a dropdown or lookup field in the Customer Success Management application.

## Before you begin

Role required: sn\_ti\_core.write

## About this task

The customer success choice record defines the set of values that appear in the drop-down and lookup fields. Each choice record specifies a name and a category. The category determines the field in which the values are displayed.

For example, if you select the Category as **Service Bridge Integration**, and you create the following customer success choice records:

-   Onboarding
-   Foundation data sync
-   Remote catalog
-   Remote task

These will appear as choices in the Service bridge integration field on the Account Onboarding Case form.

## Procedure

1.  Navigate to **Workspace** &gt; **CSM/FSM Configurable Workspace** and select the List icon.

2.  Navigate to the **Customer Success** &gt; **Customer Success Choice** and select **New**.

3.  Fill in the fields on the form.

<table id="table_rvj_lh1_3jc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the choice, displayed in the consuming field on the target record.

</td></tr><tr><td>

Order

</td><td>

Order in which this choice appears relative to other choices in the same category.

</td></tr><tr><td>

Category

</td><td>

Category that determines which field consumes this choice. -   Driver
-   Service Bridge Integration
-   Customer Success Definition
-   Risk Signal and Issue
-   Color Banding


</td></tr><tr><td>

Description

</td><td>

Description of the choice.

</td></tr></tbody>
</table>4.  Select **Save**.

    The choice record is available as a value in the field associated with the selected category.


**Parent Topic:**[Getting started with Customer Success](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/customer-success-management/account-lifecycle-basic-config.md)


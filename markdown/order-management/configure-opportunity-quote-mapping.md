---
title: Configure transaction-to-quote field mapping
description: When you use Sales CRM capabilities such as opportunity management, advanced approvals, or PDF document generation, CPQ Microservices sync data to the ServiceNow platform. This sync is set up automatically, but custom transaction fields require you to configure the data mapping.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-opportunity-quote-mapping.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [CPQ Quote Experience, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure transaction-to-quote field mapping

When you use Sales CRM capabilities such as opportunity management, advanced approvals, or PDF document generation, CPQ Microservices sync data to the ServiceNow platform. This sync is set up automatically, but custom transaction fields require you to configure the data mapping.

## Before you begin

Role required: admin

Verify that you have the permissions required to add columns on ServiceNow tables.

Activate the Quote Experience plugin \(App ID: sn\_quote\_mgmt\_adv\).

## About this task

Custom transaction fields are mapped to columns on one of two ServiceNow tables:

-   **Quote** — captures header-level quote data.
-   **Quote Lines** — captures individual line data.

To configure the mapping, create a column on the target ServiceNow table, create the corresponding field on the blueprint, map the field to the column, and then deploy the blueprint. Complete the following phases in order.

Consider the following when you map transaction fields:

-   Header-level transaction fields can be mapped only to the **Quote** table.
-   Line-level transaction fields can be mapped only to the **Quote Lines** table.
-   The **External Field Mapping** options are filtered to the column types supported by the current field type.
-   Columns that are already mapped to a field aren't displayed.
-   If you use a ServiceNow table column that has a list specification, you must add all valid choices for data to sync properly. For example, the choices for the **State** column on the **Quote** table must be updated to match the values of the `txn.stage` field.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Search for and select the table to add the column to.

    Select **Quote** for header-level data or **Quote Lines** for line-level data.

3.  On the table record page, in the **Table Columns** related list, select **New**.

4.  Configure the new column and select **Save**.

5.  Navigate to **Product Catalog Management** &gt; **Offerings** &gt; **CPQ Administration**.

6.  Select the transaction.

7.  Add a new field on the blueprint.

    For more information, see [Create a transaction field](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/quote-tm-create-field.md).

8.  Open the field properties page for the new field.

9.  In the **External Field Mapping** property, select the **Quote** or **Quote Lines** column to map the field to.

10. Select **Save**.

11. Deploy the blueprint.


## Result

The custom transaction field is mapped to the selected ServiceNow table column, and data syncs between the transaction and the quote record.


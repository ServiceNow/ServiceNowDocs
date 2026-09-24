---
title: Import business organizations with guided setup
description: Use Customer Service Management guided setup to import existing business organizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/import-csm-bo.html
release: brazil
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 1
breadcrumb: [Create a business organization, Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Import business organizations with guided setup

Use Customer Service Management guided setup to import existing business organizations.

## Before you begin

Role required: admin

## About this task

After importing business organization data, you must also [Set the business organization code property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/set-csm-bo-code-property.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup** and select **Get Started**.

2.  In the Service Model Foundation category, select **Get Started**.

3.  Select **Import Business Organizations**.

4.  Step1: Upload data from an external data source into an import set by selecting **Configure**.

    1.  Fill in the following fields in the Load Data form.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import set table

</td><td>

The data is imported into selected table-   **Create table**: A new table is created in the ServiceNow instance and the data is imported to this table. Provide a name for the table in the Name field.
-   **Existing table**: Select this option and then select a table in the **Import set table** drop-down into which you want to import the data.


</td></tr><tr><td>

Source of the import

</td><td>

-   **File**: Select this option to upload a CSV, XLS, or XML file.
-   **Data Source**: Select this option and then select the data source type from the **Data source** drop-down.


</td></tr></tbody>
</table>    2.  Select **Submit**.

5.  Step 2: Create a transform map.

6.  Step 3: Execute the transform map to transfer the data from import set table to the target table.

7.  Step 4: Verify that the data records are imported into the target table.



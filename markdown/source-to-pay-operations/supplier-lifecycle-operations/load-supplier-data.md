---
title: Load supplier data
description: Load the supplier data from the excel template into the supplier inbound​ staging tables.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Supplier Lifecycle Operations integration framework, Integrating Supplier Lifecycle Operations with other applications, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Load supplier data

Load the supplier data from the excel template into the supplier inbound​ staging tables.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Load Data**.

    The **Load Data page appears**.

2.  In **Import set table**, select **Existing table**.

3.  From the **Import set table** list, select one of the following inbound tables depending on the type of supplier data you want to import:

    -   Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\]
    -   Supplier contact inbound \[sn\_fcms\_intg\_supplier\_contact\_inbound​\]
    -   Supplier payment inbound \[sn\_fcms\_intg\_supplier\_payment\_inbound\_stage\]
4.  In **Source of the Import**, choose **File**.

5.  Browse to the excel template that was created in [Import data into invoice](../../accounts-payable-operations/task/import-external-data-into-invoice.md).

6.  Enter the **Sheet number** of the excel template that needs to be loaded into the staging table.

7.  Enter the **Header row** of the excel template that needs to be loaded into the staging table.

8.  Click **Submit**.


## Result

The supplier data from the Excel file is processed successfully. That is, the relevant supplier data is extracted from the Excel file and stored in the SLO inbound staging tables.

## What to do next

Run the transform map to import supplier data from the SLO inbound staging tables into the SLO primary tables.

-   **[Run transform to update supplier primary data](run-transform-supplier.md)**  
Use transform map and run transform to map the supplier fields from the import set into primary data target tables in Supplier Lifecycle Operations.
-   **[Monitor the integration status of the SLO inbound data import](monitor-integration-status.md)**  
Monitor the status of the integration after a transform runs and completes successfully.

**Parent Topic:**[Supplier Lifecycle Operations integration framework](../concept/slo-int-framework.md)


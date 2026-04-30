---
title: Run transform to update supplier primary data
description: Use transform map and run transform to map the supplier fields from the import set into primary data target tables in Supplier Lifecycle Operations.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Load supplier data, SLO integration framework, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Run transform to update supplier primary data

Use transform map and run transform to map the supplier fields from the import set into primary data target tables in Supplier Lifecycle Operations.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Load Data** &gt; **Run Transform**.

    The **Specify Import set and Transform map** screen appears.

    In the **Import set**, the staging table you selected from [Load supplier data](load-supplier-data.md) is auto populated.

    In **Selected maps, run in order** area, the target supplier table to be mapped in Supplier Lifecycle Operations is auto-populated and selected by default.

2.  Select **Transform**.


## Result

The relevant supplier fields from the import set staging table are mapped to the SLO primary table.

For example, if you uploaded an Excel file with supplier location information, the relevant fields are updated from the Supplier location inbound \[sn\_fcms\_intg\_supplier\_location\_inbound\] staging table into the Supplier Location \[sn\_slm\_m2m\_location\] primary table. As soon as the Supplier Location \[sn\_slm\_m2m\_location\] primary table is updated, the Supplier location outbound \[sn\_spend\_intg\_supplier\_location\_outbound\] table is also updated. An ERP integrator can extract this information from the outbound table and export it into the ERP system.

**Parent Topic:**[Load supplier data](load-supplier-data.md)

**Related topics**  


[Monitor the integration status of the SLO inbound data import](monitor-integration-status.md)


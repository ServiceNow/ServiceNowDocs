---
title: Supplier Email Domain table
description: The Supplier Email Domain \[sn\_slm\_email\_domain\] table stores important information about the email domain of a supplier.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Primary data tables for Supplier Lifecycle Operations, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Supplier Email Domain table

The Supplier Email Domain \[sn\_slm\_email\_domain\] table stores important information about the email domain of a supplier.

## Supplier Email Domain \[sn\_slm\_email\_domain\] table

The Supplier Email Domain \[sn\_slm\_email\_domain\] table contains the following fields.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email Domain

</td><td>

String

</td><td>

Email domain name \(which comes after the @ symbol\) of the supplier.**Note:** By default, the length of the email domain can be 2–4 characters.

</td></tr><tr><td>

Supplier

</td><td>

Reference

</td><td>

Vendor that provides goods and services.

</td></tr></tbody>
</table>**Note:** Multiple supplier records can have the same email domain after removing the unique constraint from the Email Domain column of the Supplier Email Domain \[sn\_slm\_email\_domain\] table.

For more information, see [Supplier Lifecycle Operations data model](slo-data-model.md).

**Parent Topic:**[Primary data tables for Supplier Lifecycle Operations](slo-primary-data-tables.md)


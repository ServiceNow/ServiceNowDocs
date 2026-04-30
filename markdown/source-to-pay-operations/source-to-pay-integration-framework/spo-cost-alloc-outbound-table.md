---
title: Outbound Cost Allocation staging table
description: The Outbound Cost Allocation \[sn\_spend\_intg\_outbound\_cost\_allocation\] staging table stores important data about the cost allocations created so that an ERP integrator can export this data to a third-party ERP system.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Outbound staging tables for Sourcing and Procurement Operations, Outbound staging tables, Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Outbound Cost Allocation staging table

The Outbound Cost Allocation \[sn\_spend\_intg\_outbound\_cost\_allocation\] staging table stores important data about the cost allocations created so that an ERP integrator can export this data to a third-party ERP system.

The following table lists the key fields for the Outbound Cost Allocation \[sn\_spend\_intg\_outbound\_cost\_allocation\] staging table.

**Note:** There are no mandatory fields for this table.

<table id="table_c23_ss5_hzb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allocation amount

</td><td>

String

</td><td>

Amount of cost that is allocated for expenditure.

</td></tr><tr><td>

Allocate by

</td><td>

String

</td><td>

Determines if the cost allocation is made by amount or percentage.

</td></tr><tr><td>

Allocation percentage

</td><td>

String

</td><td>

Percentage of the cost allocated.This field is visible only if the allocation type is set to **Percentage**.

</td></tr><tr><td>

Allocation type

</td><td>

String

</td><td>

Specifies how the cost is allocated. For example, Cost center, Employee credit, or Payroll.

</td></tr><tr><td>

Cost center

</td><td>

String

</td><td>

Cost center that incurs the cost of this allocated transaction amount.

</td></tr><tr><td>

Cost owner

</td><td>

String

</td><td>

User who incurs the cost of this allocated transaction amount.

</td></tr><tr><td>

Employee credit

</td><td>

String

</td><td>

Reference to the employee credit to which this cost allocation is made.This field is visible only if the allocation type is set to **Employee Credit**.

</td></tr><tr><td>

ERP integration status

</td><td>

String

</td><td>

Current status of the ERP integration.

</td></tr><tr><td>

ERP line number

</td><td>

String

</td><td>

Purchase order line number from the ERP system.

</td></tr><tr><td>

ERP source

</td><td>

String

</td><td>

ERP source from which data is imported. For purchase order, receipt, and invoice integrations, the ERP source is determined through the legal entity associated with these records.

</td></tr><tr><td>

Number of payments selected

</td><td>

String

</td><td>

Number of payments that the cost owner selected to pay back for a subsidized purchase.This field is visible only if the allocation type is set to **Payroll**.

</td></tr><tr><td>

Order line

</td><td>

String

</td><td>

Order line associated with the cost allocation.

</td></tr><tr><td>

Processing message

</td><td>

String

</td><td>

A message that describes the current processing status.

</td></tr><tr><td>

Purchase line

</td><td>

String

</td><td>

Purchase line associated with the cost allocation.

</td></tr><tr><td>

Terms accepted on

</td><td>

String

</td><td>

Date and time at which the cost owner has accepted the terms and conditions of the organization to withhold the payroll.This field is visible only if the allocation type is set to **Payroll**.

</td></tr></tbody>
</table>
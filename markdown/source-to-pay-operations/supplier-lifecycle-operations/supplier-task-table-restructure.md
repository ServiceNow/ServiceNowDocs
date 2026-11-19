---
title: Restructured Supplier Task table
description: The Supplier Task table architecture has been restructured in the Washington DC and Yokohama releases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/supplier-lifecycle-operations/supplier-task-table-restructure.html
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Supplier Relationship and Performance Management reference, Supplier Lifecycle Operations reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Restructured Supplier Task table

The Supplier Task table architecture has been restructured in the Washington DC and Yokohama releases.

In releases before the Washington DC release, the Supplier Task \[sn\_slm\_task\] table extended the Task \[task\] table.

Starting with the Washington DC release, the Supplier Task \[sn\_slm\_task\] table extends the Service Task \[sn\_spend\_sdc\_service\_task\] table.

\[Omitted image "supplier-task-structure.png"\] Alt text: Supplier Task table structure

After you upgrade to the Washington DC release, the fix script `glidefix_script_reparent_sn_slm_task.xml` runs to reparent the Supplier Task table on instances with huge count of records \(in millions\). Therefore, it’s advisable to run the upgrade during a period of low interaction.

**Note:** This is a mandatory one-time fix script run on instances upgrading directly to Washington DC from Vancouver or older versions.

**Parent Topic:**[Supplier Relationship and Performance Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/supplier-relationship-and-performance-management-reference.md)


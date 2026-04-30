---
title: Restructured Supplier Task table
description: The Supplier Task table architecture has been restructured in the Washington DC and Yokohama releases.
locale: en-US
release: zurich
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Supplier Relationship and Performance Management reference, Reference, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Restructured Supplier Task table

The Supplier Task table architecture has been restructured in the Washington DC and Yokohama releases.

In releases before the Washington DC release, the Supplier Task \[sn\_slm\_task\] table extended the Task \[task\] table.

Starting with the Washington DC release, the Supplier Task \[sn\_slm\_task\] table extends the Service Task \[sn\_spend\_sdc\_service\_task\] table.

![Supplier Task table structure](../image/supplier-task-structure.png "Supplier Task table structure")

After you upgrade to the Yokohama release, a new field **KPI Instruction** is added in the Supplier Task table. To update the **KPI Instruction** field, [run the fix script SLO - Feb 25 data script](../task/run-fixscript-update-kpi-instruction.md).

**Parent Topic:**[Supplier Relationship and Performance Management reference](supplier-relationship-and-performance-management-reference.md)

**Related topics**  


[Run fix script to update the KPI Instruction field in the Supplier Task table](../task/run-fixscript-update-kpi-instruction.md)

[Run fix script to migrate existing data from the deprecated Action type column after upgrade](../task/fix-script-deprecated-column.md)

[Run fix script to use the Supplier Manager Workspace after upgrading to the Zurich release](../task/access-smw-after-upgrade.md)

[Enable deprecated case types after upgrade](../task/enable-deprecated-case-types.md)


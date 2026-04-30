---
title: Configure fields in contract template to display correct sys\_id value in contract documents
description: As a contract configurator, update an advanced script to print the correct display value for sys\_id variables in the generated contract document.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage contract records, Manage, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure fields in contract template to display correct sys\_id value in contract documents

As a contract configurator, update an advanced script to print the correct display value for sys\_id variables in the generated contract document.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## About this task

Because the script for mapping variables using the Microsoft Word add-in for ServiceNow Contracts uses the toString\(\) function for the sys\_id variable, its display value is not replaced properly in generated contract documents.

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contract Administration** &gt; **Contract Templates**.

2.  Open a contract template.

3.  Navigate to the Template mapping related list.

4.  Select the field for which the advanced script is enabled and the display value is not shown properly.

    Field details are displayed along with the advanced script.

5.  In the script, replace the occurrences of toString\(\) with getDisplayValue\(\).

6.  Select **Update**.


**Parent Topic:**[Manage contract records](cncore-manage-cont-records.md)

**Related topics**  


[View a contract record](cncore-view-contract-rec.md)

[Modify a contract record](cncore-modify-contract-rec.md)


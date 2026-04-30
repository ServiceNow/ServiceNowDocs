---
title: Start migration of SAFe data to EAP
description: Submit a SAFe-EAP migration request and start the migration of data between the tables of Scaled Agile Framework and Enterprise Agile Planning.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Migrate from SAFe, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Start migration of SAFe data to EAP

Submit a SAFe-EAP migration request and start the migration of data between the tables of Scaled Agile Framework and Enterprise Agile Planning.

## Before you begin

Role required: sn\_apw\_advanced.eap\_admin

## About this task

Start data migration of SAFe to EAP. 

## Procedure

1.  Navigate to **All** &gt; **Strategic Planning** &gt; **Enterprise Agile Planning** &gt; **SAFe Migration requests**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For field information, see [SAFe-EAP migration request form](../reference/safe-eap-migration-request-form.md).

    **Note:**

    -   Planning intervals, formerly known as program increments, can only be migrated one time per team. Planning intervals falling before the selected date in the migration request and those created after the migration is complete, cannot be migrated through the automated migration \(Guided Setup\).

        For example, submit migration requests in the sequence of PI 1 &gt; PI 2 &gt; PI 3 and so on.

    -   If the composition of a SAFe ART has been changed any time after it is created, it is suggested to migrate only those PIs that have the current composition of the ART.
    -   For a Portfolio SAFe migration, if a SAFe Epic is associated with SAFe Features but is not linked to any Portfolio, then this Epic will not be migrated by the automated migration.
    -   Migration can be run multiple times for the same criteria. In such case, any newly created records will be migrated to EAP.
    -   If changes are made to already migrated SAFe records, these changes will not be synched with the EAP records.
4.  Select **Submit**.

    **Important:** Submitting the request does not trigger the migration. Open the submitted recorded from the SAFe Migration requests list and select **Start migration**.


## Result

Monitor the progress of data migration:

-   If the migration is successful, the Import Requests related list shows the details of the data migration such as failed count, insert count, and total count of records moved from SAFe to EAP.
-   If the migration encounters any error, the Migration Errors related list shows the details of records that failed to migrate from SAFe to EAP.

## What to do next

[Add Agile Team type to SAFe groups for EAP migration](change-safe-groups-type-to-agile-team.md).


---
title: Verify table, field, and choice mapping between SAFe and EAP
description: Before starting the migration from SAFe, verify that the default mapping of tables, fields, and column choices between Scaled Agile Framework applications and Enterprise Agile Planning is according to your requirements.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migrate from SAFe, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Verify table, field, and choice mapping between SAFe and EAP

Before starting the migration from SAFe, verify that the default mapping of tables, fields, and column choices between Scaled Agile Framework applications and Enterprise Agile Planning is according to your requirements.

## Before you begin

[Verify EAP configuration for migration from SAFe](verify-eap-configuration-for-migration-from-safe.md).

Role required: sn\_apw\_advanced.eap\_admin

## About this task

Verify table, field, and choice mapping between EAP and SAFe. 

## Procedure

1.  Navigate to **sn\_apw\_advanced\_safe\_eap\_mig\_setup.list**.

2.  Select the **SAFe to EAP migration** record.

3.  From the Table Maps related list, verify the table mapping between SAFe and EAP.

4.  Open each table mapping record to verify its field mapping.

    For example, open the **sn\_safe\_epic** record to see how the fields of SAFe epic are mapped to EAP epic.

    If you need to change a field mapping, open its record and update the fields.

5.  From the Field Maps related list, open a choice column record to verify the choice mapping of the fields between SAFe and EAP.

    For example, in the **sn\_safe\_epic** table map, open the **status** field map record to see how the choices for the **Status** field are mapped between SAFe and EAP.

    If you need to change a field mapping, open its record and update the fields.


## What to do next

-   For SAFe Story \[sn\_safe\_story\] and SAFe Scrum Task \[sn\_safe\_scrum\_task\] tables, all default columns are migrated to the Story \[rm\_story\] and Scrum Task \[rm\_scrum\_task\] tables. To include or exclude any columns, update the **sn\_apw\_advanced.SAFeEAPStoryTaskMigrationAPI** script include. See [Modify columns to migrate from SAFe story and SAFe Scrum task tables to EAP](modify-columns-to-migrate-safe-story-task-tables-to-eap.md).
-   [Start migration of SAFe data to EAP](migrate-safe-data-to-eap.md).


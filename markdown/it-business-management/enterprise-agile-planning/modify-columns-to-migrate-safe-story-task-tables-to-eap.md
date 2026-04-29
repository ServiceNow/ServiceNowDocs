---
title: Modify columns to migrate from SAFe story and SAFe Scrum task tables to EAP
description: For the SAFe Story and SAFe Scrum task tables, ensure that only the data from the necessary columns is migrated to Enterprise Agile Planning. By updating a Script Include, include or exclude any columns according to your requirements.
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Migrate from SAFe, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Modify columns to migrate from SAFe story and SAFe Scrum task tables to EAP

For the SAFe Story and SAFe Scrum task tables, ensure that only the data from the necessary columns is migrated to Enterprise Agile Planning. By updating a Script Include, include or exclude any columns according to your requirements.

## Before you begin

[Verify table, field, and choice mapping between SAFe and EAP](verify-table-field-and-choice-mapping-between-safe-and-eap.md).

Role required: sn\_apw\_advanced.eap\_admin

## About this task

Modify columns of the SAFe Story and Scrum Task tables to migrate to EAP. 

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Search for and open the **sn\_apw\_advanced.SAFeEAPStoryTaskMigrationAPI** script include.

3.  Follow the comments in the **Script** field to include or exclude any columns of the SAFe Story and SAFe Scrum Task tables.

4.  Save the form.


## What to do next

[Start migration of SAFe data to EAP](migrate-safe-data-to-eap.md).


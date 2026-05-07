---
title: Migrate SDS from chemical safety register to chemical item
description: Migrate your existing safety data sheets \(SDS\) from Chemical safety register to chemical item in Health and Safety Environmental Management.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-11-28"
reading_time_minutes: 1
breadcrumb: [Configure, Health and Safety Environmental Management, Health and Safety, Employee Service Management]
---

# Migrate SDS from chemical safety register to chemical item

Migrate your existing safety data sheets \(SDS\) from Chemical safety register to chemical item in Health and Safety Environmental Management.

## Before you begin

Role required: sn\_ohs\_im.admin

## About this task

When you install the Health and Safety Environmental Management, the SDS document attachment saved to the Chemical Safety Register \(sn\_hs\_rm\_safety\_register\_chemical\) table migrates to the document \(sn\_ohs\_im\_document\_v2\) table.

The tool supports batch migration of up to 200 records at a time. After migration, all documents can be efficiently managed within the new list.

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Standards and documentation \(Deprecated\)** &gt; **Document migration**.

2.  Select **Chemical item** and then select **Migrate 200 records**.

    The migration records and their migration status are listed in the **Migration records** list.

3.  Repeat step 2 until you have migrated all existing document records.


## Result

-   The count of documents that have successfully migrated, documents pending migration, and failed migration are listed in the **Migrated records**, **Remaining records**, and **Fail records** widgets.
-   The successfully migrated records appear appears under the **Document** related list of the respective **Chemical item** record.

**Parent Topic:**[Setting up Health and Safety Environmental Management](../concept/hs-setting-up-environmental-management.md)


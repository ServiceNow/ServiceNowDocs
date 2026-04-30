---
title: Coalesce records on a normal value
description: Coalescence enables an administrator to redirect references to multiple records containing variants of the same field value to point to a single record, based on a normal value.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Normal values, Field normalization and transformation, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Coalesce records on a normal value

Coalescence enables an administrator to redirect references to multiple records containing variants of the same field value to point to a single record, based on a normal value.

## Before you begin

Role required: admin

## About this task

An example of this is the Company table that might have multiple variants of a company name, such as Hewlett-Packard, Hewlett-Packard, Inc., Hewlett-Packard Incorporated, HP, and so on. Potentially, thousands of records might reference each of these duplicate company records. Using the variants of the Hewlett-Packard name as aliases, coalescence unifies all these references into a single record that normalizes the **Name** field in the Company record to a normal value such as **HP**.

**Note:** Coalescing normal values changes the record values permanently. If a rollback is performed, records will be returned to the table, but the normalized values will not be rolled back to the original variants.

When the references are fixed, all table fields directly corresponding to sys\_dictionary get fixed. The secondary references are not fixed. If you have filter conditions that has the old, pre coelesced company names, they aren't fixed either.

## Procedure

1.  Navigate to **All** &gt; **Field Normalization** &gt; **Configuration** &gt; **Normalizations**

2.  Select a normalization record.

3.  Enable **Coalesce each normal**.

    The system adds the **Coalesce to** field to the Normal Value form.

4.  Create one or more normal value records for this normalization record.

    Create related aliases and rules as needed.

5.  For each normal value record, set **Coalesce to** by selecting the record that contains the normal value.

    For example, suppose your Company table contains several variations of the name ServiceNow. When you create the Normal Value record, you select the Company record for ServiceNow, Inc.. During normalization, the system updates any references to variant records to instead refer to the normal record.

    The system updates any references to records that match aliases and rules to instead point to the normal record. The system also deletes the duplicate records from the table.

6.  [Start](t_ApplyAliases.md) all the **Alias application** data jobs to replace the aliases with the normal value in existing records in the database.

    The system starts the **Coalesce to normal** data jobs for each alias.


**Parent Topic:**[Normal values](../concept/c_WhatFieldNormalizationDoes.md)


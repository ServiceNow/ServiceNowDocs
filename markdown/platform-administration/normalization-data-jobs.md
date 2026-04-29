---
title: Normalization and transformation data jobs
description: The system uses data jobs to change field values during normalization and transformation.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Normalization and transformation data jobs

The system uses data jobs to change field values during normalization and transformation.

Administrators must manually start data jobs that apply field changes. All transformation records open in Test mode by default, which blocks administrators from running manual data jobs that apply changes to existing data. Most data jobs have a roll back option to revert changes after the job completes. By default, the system provides these data jobs.

**Note:**

If the Field Normalization plugin is active, the normalization engine executes on insert of records into a table according to normalization rules. To learn more about this plugin, see [Activate Field Normalization](../task/activate-field-normalization.md).

If the Field Normalization plugin is not active, a data job runs to normalize the values. The data job saves the previous values in the rolled back fields to revert them if necessary.

|Name|Used for|Description|
|----|--------|-----------|
|Pending value collection|Normalization|The system runs this job to collect field values that will change during the next field normalization run. The system runs this job whenever you insert or update a field normalization record. Since this data job does not change any field values, there is no roll back option.|
|Normal value change|Normalization|Run this job to rerun field normalization and update field values when you change a normal value. The system creates this job whenever you change a normal value. Roll back the data job to revert the normalized fields to the previous normal value.|
|Alias application|Normalization|Run this job to normalize all field values that match an alias. The system creates this job whenever you create or update an alias. Roll back the data job to revert normalized fields to their previous values.|
|Rule application|Normalization|Run this job to normalize all field values that match a rule. The system creates this job whenever you create or update a rule. Roll back the data job to revert normalized fields to their previous values.|
|Coalesce too normal|Normalization|Run this job to normalize the reference field values by replacing references to multiple duplicate records with one reference to a normalized record. The system creates this job whenever you change a normal value that applies to a reference field. Roll back the data job to restore the duplicate records as valid options. The rollback does not restore references to the previous records.|
|Transform application|Transformation|Run this job to transform all field values that match the transformation conditions. You cannot start this job while the Transformation record is in **Test** mode. The system creates this job whenever you create or update a transformation record. Roll back the data job to revert transformed fields to their previous values.|


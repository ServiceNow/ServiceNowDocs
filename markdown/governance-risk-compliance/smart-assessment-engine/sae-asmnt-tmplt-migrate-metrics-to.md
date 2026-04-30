---
title: Migrate a legacy metric type to an assessment template
description: Migrate an existing metric type to an SAE assessment template. You can leverage the existing assessment designs while using Smart Assessment Engine.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Creating an assessment template from legacy assessment metric types, Configure, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Migrate a legacy metric type to an assessment template

Migrate an existing metric type to an SAE assessment template. You can leverage the existing assessment designs while using Smart Assessment Engine.

## Before you begin

Role required: sn\_smart\_asmt.assessment\_admin

## About this task

SAE must be running on the same instance as the metric data to migrate.

## Procedure

1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Migrations**.

2.  On the Assessment template migrations list, select **New** and then fill in the Assessment template migration form.

    You specify the metric type to migrate and the template category that the assessment template should be associated with. The system automatically fills in the other settings.

<table id="table_nkg_2jy_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number, starting with the text ATMIG, that the system assigned to the migration record for the metric type. You can use the number to search for the record.

</td></tr><tr><td>

Source metric type

</td><td>

Metric type to migrate to the assessment template format.

</td></tr><tr><td>

Purpose

</td><td>

Purpose that the new assessment template should be a member of. For example, Risk, Performance, Security, Personal data, and so on.

 Template purposes enforce data segregation for templates. A purpose controls which users can view a template. Each assessment template is associated with a purpose. To view a template within a specific purpose, you must have a category role associated with that purpose.

 By default, newly defined template categories are active.

 **Note:** You can only select one purpose.

</td></tr><tr><td>

Migration status

</td><td>

Value that changes as the template migration process proceeds.

-   New: Status of a template migration definition before you start migration.
-   In progress: Status for after you start the migration process, the process is in progress until it finishes.
-   Completed: Status of a template migration if all items \(metric type, metric categories, and metrics\) migrate, which means that the template is ready for you to review, update, and eventually publish.
-   Partially completed: Status when any of the downstream elements like the questions, sections, or metric category haven’t migrated successfully. In this case, you must address the errors and restart the migration process.
-   Errored: Status when an error occurs during the migration. In this case, you must address the errors and restart the migration process.


</td></tr><tr><td>

Target assessment template

</td><td>

New template that the existing metric type is migrated to.

 **Important:** If the migration status is **Errored**, the field shows no value.

</td></tr></tbody>
</table>3.  Select **Migrate**.


## Result

The Section migration related list is updated as migration proceeds. You can view the data that was migrated from the metric type to the Smart Assessment Engine assessment template in the related lists on the Assessment template migration form. See [Results of migrating a metric category to an assessment template](../reference/sae-migrate-asmnt-template-form.md).

**Related topics**  


[How legacy metric types are migrated to sections in templates](../reference/sae-how-legacy-metrics-migrated.md)

[Results of migrating a metric category to an assessment template](../reference/sae-migrate-asmnt-template-form.md)


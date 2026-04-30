---
title: Results of migrating a metric category to an assessment template
description: You can view the data that was migrated from the metric type to the Smart Assessment Engine assessment template in the related lists on the Assessment template migration form.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reference, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Results of migrating a metric category to an assessment template

You can view the data that was migrated from the metric type to the Smart Assessment Engine assessment template in the related lists on the Assessment template migration form.

## Tracking assessment template migration

After you have filled out the Assessment template migration form and started the migration process, you can view the progress and confirm if it completed successfully or if there were any errors. For more information on the migration process, see [Creating an assessment template from legacy assessment metric types](../concept/sae-asmnt-template-migrating.md), [Migrate a legacy metric type to an assessment template](../task/sae-asmnt-tmplt-migrate-metrics-to.md), and [How legacy metric types are migrated to sections in templates](sae-how-legacy-metrics-migrated.md).

## Viewing the migration results

To view your migration results, navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Template Migrations**. In the Assessment template migrations list, select the migration number. Each migration record for a metric type is assigned a unique number that starts with the text ATMIG. The form displays the values that were used to generate the template. The related lists display the status and content of the migrated data. The Section migrations table provides a description of the fields in the related lists.

## Results of the migration

The following table describes the fields in the Section migrations related list.

<table id="table_rqd_1cy_bzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number that starts with the text ATSMIG in the migration record for the section. You can use the number to search for the record.

</td></tr><tr><td>

Source metric category

</td><td>

Metric category that is created from the section after the metric types are migrated.

</td></tr><tr><td>

Target section

</td><td>

Section that was populated during the migration.

</td></tr><tr><td>

Migration status

</td><td>

Migration status:-   **Completed**: The migration is completed successfully.
-   **Errored**: An error occurred during the migration.

</td></tr><tr><td>

Error details

</td><td>

Description of an error that occurred during the unsuccessful migration.

</td></tr></tbody>
</table>Select the down arrow for a section to view the list of questions in the section. The following table describes the fields in the Question migrations related list.

<table id="table_vdm_1sz_w1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number, starting with the text ATQMIG, that the system assigned to the migration record for the question. You can use the number to search for the record.

</td></tr><tr><td>

Source metric

</td><td>

Metric that is created from a question after the assessment template migration.

</td></tr><tr><td>

Target question

</td><td>

Question that was created after the migration.

</td></tr><tr><td>

Migration status

</td><td>

Migration status:-   **Completed**: The migration is completed successfully.
-   **Not supported**: The metric in the original metric type isn’t supported for the migration.
-   **Errored**: An error occurred during the migration.

</td></tr><tr><td>

Error details

</td><td>

Description of an error that occurred during the unsuccessful migration.

</td></tr></tbody>
</table>Select the down arrow for a question to view the list of response options for the question. The following table describes the fields in the Response option migrations related list.

<table id="table_rc1_3sd_1bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Response option migrations

</td></tr><tr><td>

Number

</td><td>

Unique number, starting with the text ATROMIG, that the system assigned to the migration record for the response option. You can use the number to search for the record.

</td></tr><tr><td>

Source metric definition

</td><td>

Metric definition from the options that are migrated for a question.

</td></tr><tr><td>

Source template definition

</td><td>

Field referenced for the template definition from the response options that are automatically filled in if the data type of the source metric is a template.

</td></tr><tr><td>

Target response option

</td><td>

Field that shows the response option that was created after migrating the source.

</td></tr><tr><td>

Migration status

</td><td>

Migration status:-   **Completed**: The migration is completed successfully.
-   **Errored**: An error occurred during the migration.

</td></tr><tr><td>

Error details

</td><td>

Description of an error that occurred during the unsuccessful migration.

</td></tr></tbody>
</table>**Related topics**  


[How legacy metric types are migrated to sections in templates](sae-how-legacy-metrics-migrated.md)


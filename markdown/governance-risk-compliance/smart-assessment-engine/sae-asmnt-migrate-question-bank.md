---
title: Migrate a classic question bank or assessment template
description: Migrate a classic question bank or an existing assessment template into a new or existing Smart Assessment Engine question bank.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/sae-asmnt-migrate-question-bank.html
release: brazil
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Creating an assessment template from legacy assessment metric types, Configure, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Migrate a classic question bank or assessment template

Migrate a classic question bank or an existing assessment template into a new or existing Smart Assessment Engine question bank.

## Before you begin

Role required: sn\_smart\_asmt.assessment\_admin

## About this task

SAE must be running on the same instance as the classic question bank or the assessment template that you want to migrate.

## Procedure

1.  Navigate to **All** &gt; **Smart Assessment Engine** &gt; **Administration** &gt; **Question Bank Migrations**.

2.  On the Question bank migrations list, select **New** and then fill in the Question bank migration form.

<table id="table_qb-migration-form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique number, starting with the text QBMIG, that the system assigns to the migration record for the question bank. You can use the number to search for the record.

</td></tr><tr><td>

Migration source type

</td><td>

Type of content to migrate: **Classic question bank** or **Smart assessment template**.

</td></tr><tr><td>

Source metric categories

</td><td>

One or more legacy metric categories to migrate into the question bank.

 This field appears only when **Migration source type** is set to **Classic question bank**.

</td></tr><tr><td>

Source assessment template

</td><td>

Existing SAE assessment template whose sections and questions you want to copy into a question bank.

 This field appears only when **Migration source type** is set to **Smart assessment template**.

</td></tr><tr><td>

Purposes

</td><td>

One or more purposes for the new question bank.

 This field is required when **Create question bank** is selected.

</td></tr><tr><td>

Create question bank

</td><td>

Option to create a question bank as the migration target. This option is selected by default. Clear this option to migrate into an existing question bank instead.

</td></tr><tr><td>

Target question bank name

</td><td>

Name for the new question bank.

 This field is required when **Create question bank** is selected.

</td></tr><tr><td>

Target question bank description

</td><td>

Description for the new question bank.

 This field appears only when **Create question bank** is selected.

</td></tr><tr><td>

Target question bank

</td><td>

Existing question bank to migrate the content into.

 This field is required when **Create question bank** isn't selected. Once the migration starts, this field becomes read-only.

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

Error details

</td><td>

Description of an error that occurred during the unsuccessful migration.

</td></tr></tbody>
</table>3.  Select **Migrate**.


## Result

The Section migrations and Question migrations related lists update as the migration proceeds.

When the source is a classic question bank, unsupported questions are marked accordingly and the migration continues with the remaining questions. A classic source migration doesn't roll back.

When the source is an assessment template and an error occurs, the system reverts only the sections and questions that this migration run added. Any content that already existed in the target question bank is kept.

**Related topics**  


[Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/smart-assessment-engine/question-bank.md)

[Create a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-create.md)


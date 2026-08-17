---
title: Edit a value template
description: Edit a value template to change how AI Control Tower calculates value for the AI systems it is mapped to.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-ai-edit-value-template.html
release: australia
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
breadcrumb: [Configure, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Edit a value template

Edit a value template to change how AI Control Tower calculates value for the AI systems it is mapped to.

## Before you begin

Role required:

-   AI steward \[sn\_ai\_g overnance\_ai\_steward\]
-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## About this task

You can edit a value template directly, or duplicate it to make changes while keeping the original. Duplicating is useful when you want to preserve the history of a published template.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and templates** &gt; **Templates**.

2.  Select the asset whose value template you want to edit, and then select **Duplicate**.

    A new dialog box opens so you can select what to duplicate. Then a tab with the same details as the original template opens for editing.

    **Note:** Duplicating a template creates a copy in the Draft state, as a custom template, that you can edit. The original template is unchanged. For a published template, you can edit only a limited number of fields.

3.  Edit the value template according to your requirements.

    See [Value template form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/measure-ai-reference-value-template-form.md) for field descriptions.

4.  Validate and test the formula against the available dataset by selecting **Validate and calculate output**.

    You can preview calculations from the past 30 days using the new template before publishing. This lets you evaluate the impact of the new template while preserving the historical data from the previous version.

5.  If you're satisfied with the output, publish the template by selecting **Publish template**.

    Publishing modifies the value template across all instances, and later calculations use the new template.

    After a template is published, you can't edit its basic details, but you can still add more assets for mapping to it. Testing is not available for published templates.


## Result

AI Control Tower calculates value for the mapped AI systems by using the updated template.


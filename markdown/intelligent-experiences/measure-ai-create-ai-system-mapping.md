---
title: Map Value template to an AI system
description: Add a mapping to link a value template to a specific AI system, so that AI Control Tower calculates that system's value by using the template.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-ai-create-ai-system-mapping.html
release: australia
topic_type: task
last_updated: "2026-07-26"
reading_time_minutes: 1
breadcrumb: [Configure, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Map Value template to an AI system

Add a mapping to link a value template to a specific AI system, so that AI Control Tower calculates that system's value by using the template.

## Before you begin

Role required:

-   AI steward \[sn\_ai\_g overnance\_ai\_steward\]
-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## About this task

Adding a mapping links one value template to one AI system. On the AI system mapping view, assets are grouped by the template they are mapped to, and you add new mappings from there.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and templates** &gt; **Templates**.

2.  On the **AI system mapping** sub-tab, select **Add mapping**.

3.  On the Add mapping form, fill in the fields.

<table id="table_szt_fgt_1kc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template name

</td><td>

Name of the value template that you want to map with an AI asset.

</td></tr><tr><td>

Persona

</td><td>

The persona is read-only and is set automatically from the selected template.

</td></tr><tr><td>

AI system type

</td><td>

Select a type of AI system: -   agentic AI
-   generative AI
-   Classic AI


</td></tr><tr><td>

AI asset name

</td><td>

Name of the AI asset for which you want to add the value template mapping.

</td></tr></tbody>
</table>4.  Select **Save**.

    The new mapping appears in the **AI system mapping** list immediately.


## Result

The AI system is mapped to the value template, and AI Control Tower calculates the system's value by using that template.


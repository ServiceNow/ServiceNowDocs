---
title: Assign a default template
description: Assign default value templates to AI systems by defining the criteria such as AI system category, vendor, and skill type, so that the matching systems use it automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/measure-ai-assign-default-template.html
release: australia
topic_type: task
last_updated: "2026-07-26"
reading_time_minutes: 1
breadcrumb: [Configure, Measure AI impact and value, Measure AI impact, AI Control Tower, Enable AI experiences]
---

# Assign a default template

Assign default value templates to AI systems by defining the criteria such as AI system category, vendor, and skill type, so that the matching systems use it automatically.

## Before you begin

Confirm that a published value template exists. See [Create a value template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/measure-ai-create-value-template.md) for more information.

Role required:

-   AI steward \[sn\_ai\_g overnance\_ai\_steward\]
-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

## About this task

A default template rule automatically applies a value template to any AI system that matches the criteria you define.

If an AI system has its own template mapping, that mapping is used instead of the default.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Settings** &gt; **Rules and templates** &gt; **Templates**.

2.  On the **Default template rules** sub-tab, select **Assign default template**.

3.  On the Assign default template form, fill in the fields.

<table id="table_x4x_v5m_1kc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template name

</td><td>

Default template name that you want to assign to an AI system.

</td></tr><tr><td>

Vendor

</td><td>

Software vendor of the AI system to which you want to assign the default template.

</td></tr><tr><td>

AI system category

</td><td>

Category of the AI system to which you want to assign the default template.**Note:** For the **AI Skill** system category, specify the skill type, Default or Creator.

</td></tr></tbody>
</table>    \[Omitted image "measure-ai-assign-default-template.png"\] Alt text: Assign default template form in AI Control Tower

4.  Select **Assign as default**.

    If a default rule already exists for the same vendor, AI system category, and skill type, this assignment updates that rule to use the new value template. Otherwise, a new default rule is created.


## Result

AI systems that match the rule, use the assigned value template by default.


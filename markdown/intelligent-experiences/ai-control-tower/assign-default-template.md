---
title: Assign a default template
description: Assign a template as default for a specific type of AI system.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-24"
reading_time_minutes: 1
breadcrumb: [Using value templates, Using AI Control Tower, AI Control Tower, Enable AI experiences]
---

# Assign a default template

Assign a template as default for a specific type of AI system.

## Before you begin

Role required: AI steward \[sn\_ai\_g overnance\_ai\_steward\]

## Procedure

1.  Navigate to **Workspaces** &gt; **AI Control Tower**.

2.  From the AI Control Tower, open the Configurations view.

3.  From the navigation menu of the Configurations view, navigate to **Controls** &gt; **Value templates**.

4.  Select **Assign default template**.

5.  On the Assign default template form, fill in the fields.

<table id="table_rly_nfj_khc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Template name

</td><td>

Name of the value template that you want to assign as default to an AI system.

</td></tr><tr><td>

Vendors

</td><td>

Name of the software vendor who has developed the selected AI system.

</td></tr><tr><td>

AI system category

</td><td>

Name of the AI system category to which you want to assign the default template.**Note:** If you select the **AI Skill** category, you must specify the skill type to either Default or Creator.

</td></tr></tbody>
</table>6.  Select **Assign as default**.

    The template has now been assigned as default to the selected AI system and is available in the **Default template mapping** list.

    If the selected configuration matches with any existing default assignment, it updates the existing template.


**Parent Topic:**[Using value templates](../concept/using-value-templates.md)


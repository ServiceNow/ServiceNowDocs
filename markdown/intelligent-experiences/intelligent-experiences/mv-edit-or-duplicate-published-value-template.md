---
title: Edit a published value template
description: Change the department, description, or AI system mappings of a published value template, and remove templates that you no longer need while keeping value calculation uninterrupted.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Edit a published value template

Change the department, description, or AI system mappings of a published value template, and remove templates that you no longer need while keeping value calculation uninterrupted.

## Before you begin

The value template must be published.

Role required: sn\_ai\_governance\_ai\_steward

## About this task

After you publish a template, you can't change its metric. You can still change the department and the description, and you can add or remove the AI systems that the template is mapped to.

The actions that you can perform on a template depend on its current state:

<table><thead><tr><th>

Template state

</th><th>

Permitted actions

</th></tr></thead><tbody><tr><td>

Published

</td><td>

-   Metric fields can't be edited.
-   Template details \(Department, Description\) can be updated.
-   Mapping records can be added or removed.
-   Can use the **Duplicate** action to clone the template, with or without its mapping records. Cloned templates start in the draft state.

</td></tr><tr><td>

Draft

</td><td>

-   All fields \(metrics, template details, mapping records\) are editable.
-   Draft templates can be deleted or published.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to **Settings** &gt; **Rules and templates** &gt; **Templates** &gt; **All templates**.

3.  Select the template that you want to edit.

    To reuse a published template as a starting point, select **Duplicate template**.You can duplicate the template with or without its mapping records. The cloned template is created in the draft state, so you can edit all of its fields before you publish it.

4.  Select **Edit template**.

5.  Change the department and description, and then select **Next**.

6.  In the mapping step, you can do the following:

    1.  To add a mapping, select an option from the **AI system type** list, select an option from the **AI system** list, and then select **Map AI systems**.

        When you add an AI system, the AI Control Tower starts calculating value for it against this template.

    2.  To remove the mapping, select \[Omitted image "ad-delete-icon.png"\] Alt text: Delete icon beside the AI system type that you want to delete.

        Each deployed AI system must have a published template so that value calculation continues. When you map the AI system to another published template, the AI Control Tower retires the earlier mapping. A message explains this when you try to remove the only mapping.

7.  Select **Save**.


## Result

Changes to the template are saved.


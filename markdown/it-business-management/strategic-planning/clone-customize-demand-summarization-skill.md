---
title: Copy and customize the demand summarization skill
description: Copy the base demand summarization skill and customize it with your own fields, related entities, and prompt to summarize demands.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/clone-customize-demand-summarization-skill.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: task
last_updated: "2026-08-12"
reading_time_minutes: 3
keywords: [clone, Demand Summarization, Now Assist for Strategic Portfolio Management]
breadcrumb: [Configure the demand AI skills, Configure, Next Experience for Demand Management in Strategic Planning, Strategic Planning, Strategic Portfolio Management]
---

# Copy and customize the demand summarization skill

Copy the base demand summarization skill and customize it with your own fields, related entities, and prompt to summarize demands.

## Before you begin

Role required: sn\_nowassist\_admin.nsa\_admin

## About this task

The demand summarization skill generates a summary of a demand record from a set of input fields and related lists. The base skill can be copied to include fields or related entities specific to your organization's demand process that are not included in the base skill. Copying creates an independent copy that you customize with your own fields, related entities, and prompt. The copied skill then summarizes demands using your configuration.

**Note:** The existing skill, either base or copy, are deactivated after a new copy is activated.

## Procedure

1.  Navigate to **Admin** &gt; **AI Admin Hub**.

2.  Select **AI Skills**.

3.  In the navigation panel, select **Technology** &gt; **SPM**.

4.  Select the **Options** menu from the demand summarization skill card.

    \[Omitted image "demand-make-copy-skill-option.png"\] Alt text: Make a copy is available under the Options menu.

5.  Select **Make a copy**.

6.  Select **Make a copy** in the confirmation pop-up.

    The skill configuration setup opens.

7.  Add or remove an input field.

<table id="choicetable_zn4_5qk_fkc"><thead><tr><th align="left" id="d194679e157">

Goal

</th><th align="left" id="d194679e160">

Action

</th></tr></thead><tbody><tr><td id="d194679e166">

**Add a field**

</td><td>

1.  Select **Add additional input field**.
2.  Select a field from the Additional input field list.
3.  Provide a description for the field.


</td></tr><tr><td id="d194679e190">

**Remove a field**

</td><td>

Select the cross icon next to an input field.

</td></tr></tbody>
</table>    For more information on the default input fields and related tables, see [Inputs for AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/skill-inputs-for-ai-skills.md).

8.  Add conditions for the skill.

9.  Add or remove a field from a related table, add or remove a related table, or add rule conditions for each related table.

<table id="choicetable_wzc_j5k_fkc"><thead><tr><th align="left" id="d194679e227">

Goal

</th><th align="left" id="d194679e230">

Action

</th></tr></thead><tbody><tr><td id="d194679e236">

**Add a field from a related table**

</td><td>

1.  Select **Add field** for a related table.
2.  Select a field from the Related table field list.
3.  Provide a description for the field.


</td></tr><tr><td id="d194679e260">

**Remove a field from a related table**

</td><td>

Select the cross icon next to a related table field.

</td></tr><tr><td id="d194679e269">

**Add a related table**

</td><td>

1.  Select **Add related table**.
2.  Select a table from the Related table list.
3.  Select a field from the Related table field list.
4.  Provide a description for the field.


</td></tr><tr><td id="d194679e296">

**Remove a related table**

</td><td>

Select the cross icon next to a related table.

</td></tr><tr><td id="d194679e306">

**Add rule conditions for a related table**

</td><td>

1.  Select the **Add rule conditions** toggle.
2.  Define the rule conditions.


</td></tr></tbody>
</table>10. Add relationship table fields.

    1.  Select **Add relationship table**.

    2.  Select a field from the Relationship table field list.

11. Select whether any additional data source should be considered by the skill.

    A check mark next to each step indicates whether the step is completed, partially completed, or not completed. After configuring a step, select **Save and continue** to go to the next step. Return to a previous step by selecting **Back**.

    **Note:** Some configuration options are read-only.

12. Define the trigger for the skill.

    -   **Automatic**: The skill is initiated without user interaction. When users navigate to the **AI Overview** page of a demand, the summary of the record is auto-generated.
    -   **User trigger**: The skill is initiated when users select the **Summarize** action on a demand record.
13. Define and review the user accesses.

14. Choose where to display the skill.

    The display options may vary from skill to skill.

    **In-product desktop**: When selected, the skill is displayed on forms and workspaces.

15. Open the role selection list next to the Display toggle, and select the roles that can use the skill.

    The user roles added in the **Define access** page for each ACL can be selected in this step.

16. Review the configuration and select **Activate**.


## Result

The copy of the demand summarization skill is activated. This will now be used to summarize demands.

## What to do next

After cloning the demand summarization skill, you can create and customize prompts for the skill using the AI Skill Kit. You can use a base prompt and create a prompt of your own. For more information, see [Create a prompt](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-prompt-template.md). This prompt will be applied to the skill in Next Experience for Demand Management.


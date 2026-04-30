---
title: Configure and activate a skill for Now Assist for Security Incident Response
description: Configure and review the details for a skill in the Guided Setup. You can activate a skill from the Guided Setup.
locale: en-US
release: xanadu
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2025-05-16"
reading_time_minutes: 4
keywords: [Now Assist Security Operations]
breadcrumb: [Configuring Now Assist for Security Incident Response, Now Assist for Security Incident Response, Security Operations]
---

# Configure and activate a skill for Now Assist for Security Incident Response

Configure and review the details for a skill in the Guided Setup. You can activate a skill from the Guided Setup.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  Select **Security Operations** from the list.

    You cannot edit the skills that are included with the application. To edit the default settings, you must make a copy. For more information about customizing a skill, see [Customize a Now Assist for Security Incident Response skill](cust-now-assist-security-incident-skill.md).

    These Security Incident Response skills are displayed:

    -   Resolution notes generation
    -   Security incident summarization
    -   Security operations metrics analysis

        **Note:**

        This skill is activated for use with an AI agent. See [Analyze security operations metrics agentic workflow](assess-metrics-sir-aiagent.md) for more information.

    -   Correlation insights generation
    -   Post incident analysis
    -   Security incident recommended actions

        The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

3.  Select **Activate skill** for the skill that you want.

    **Note:** After you activate a skill, you must deactivate it if you want to edit the configuration settings.

4.  Follow the steps to configure and activate a skill using the Guided Setup.

    **Note:** Some skills do not require all the configuration steps listed below. Select the only tasks that are displayed in the left panel and follow the prompts. After you have completed all the tasks, activate the skill.

5.  Select **General Details**.

6.  Select **Save and continue** to go to the next step in the Guided Setup.

7.  Select **Choose input** to configure the inputs or triggers for the selected skill.

    Some, or all of the following input templates for the skill are listed: **Work In Progress**, **Review**, and **Closed**. The **Work In Progress** template is selected.

    You might prefer to leave these input templates in their default settings until you become familiar with how the skills for Now Assist for Security Incident Response work.

    However, for some of the skills you can modify certain related table fields, test the prompt on a security incident, define the availability of the skill, and choose where the skill is displayed.

    If you choose to modify fields, select only the supported options from the lists provided as part of your input data.

    If you modify the inputs or triggers for a skill, you determine how and when a skill is used. You can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on. However, you can copy a skill and customize it. For more information, see [Customize a Now Assist for Security Incident Response skill](cust-now-assist-security-incident-skill.md).

8.  If available, select **Customize Prompt** to test the prompt on a security incident record.

9.  Select **Save and continue** to go to the next step in the Guided Setup.

10. Choose one of the following options to define availability.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d372685e285">

Option

</th><th align="left" id="d372685e288">

Description

</th></tr></thead><tbody><tr><td id="d372685e294">

**Skill is always available**

</td><td>

Skill is always available to users.

</td></tr><tr><td id="d372685e303">

**Customize skill availability**

</td><td>

The skill is available only when certain conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>11. Select **Save and continue** to go to the next step in the Guided Setup.

12. Choose **Select display**.

    Select the expand icons \(![Expand icon.](../image/icon-expand.png)\) in the sections under Select Display to determine where you'd like the skill to display and who can view it. Skills might have some or all of the following options after you expand a section.

<table id="choicetable_x1c_5b2_1cc"><thead><tr><th align="left" id="d372685e353">

Option

</th><th align="left" id="d372685e356">

Description

</th></tr></thead><tbody><tr><td id="d372685e362">

**In-product desktop**

</td><td>

Select the **Display** toggle so that Now Assist skills with this option are displayed on forms and workspaces.

</td></tr><tr><td id="d372685e377">

**Now Assist panel**

</td><td>

Select the **Display** toggle to display the skill in the Now Assist panel. **Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Turn on the Now Assist panel](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

The security incident recommended actions and post-incident analysis skills are not available from the Now Assist panel.

</td></tr><tr><td id="d372685e408">

**Conversational experiences**

</td><td>

Verify where the skill is displayed and add roles for who can view it.Select **Now Assist Panel** in the Conversational experiences field to display the skill in the Now Assist panel.

</td></tr></tbody>
</table>13. Select **Save and continue** to go to the next step.

14. Review your choices and select **Activate** to complete the configuration for the skill.

15. Select **Select back to skills** to return to the Now Assist skills page.



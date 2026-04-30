---
title: Configure a skill for Now Assist for Security Incident Response
description: Configure and review the details for a skill in the Guided Setup. You can deactivate, edit, and reactivate a skill from the Guided Setup.
locale: en-US
release: yokohama
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-01-15"
reading_time_minutes: 4
keywords: [Now Assist Security Operations, skill configuration]
breadcrumb: [Configure, Now Assist for Security Incident Response, Security Operations]
---

# Configure a skill for Now Assist for Security Incident Response

Configure and review the details for a skill in the Guided Setup. You can deactivate, edit, and reactivate a skill from the Guided Setup.

## Before you begin

Role required: admin

## About this task

**Important:** Some Now Assist skills, agents, and agentic workflows are turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills**.

2.  With **Technology** selected in the navigation panel, select **Security Operations** from the list.

    The Now Assist skills for Security Operations page is displayed. The Now Assist for Security Incident Response skills are active by default and supported for Now Assist for Security Incident Response.

    -   Security incident recommended actions

        The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

    -   Post incident analysis
    -   Correlation insights generation
    -   Security incident summarization
    -   Resolution notes generation
    -   Security operations metrics analysis
    -   Generate content for shift handover
    -   Security Incident Quality Assessment
    The following steps are optional. You must deactivate a skill to configure it using the Guided Setup.

3.  Select **Deactivate skill** for the skill that you want to configure.

4.  Follow the steps to configure and reactivate a skill using the Guided Setup.

    **Note:** Some skills do not require all the configuration steps listed below. Select only the tasks that are displayed in the left panel and follow the prompts. After you have completed the tasks, activate the skill.

    1.  In the navigation panel, select **Choose input** to configure the inputs or triggers for the selected skill.

        Some, or all of the following input templates for the skill are listed: **Work In Progress**, **Review**, and **Closed**. The **Work In Progress** template is selected.

        You might prefer to leave these input templates in their default settings until you become familiar with how the skills for Now Assist for Security Operations work.

        However, for some of the skills you can modify certain related table fields, test the prompt on a security incident, define the availability of the skill, and choose where the skill is displayed.

        For the Security Incident Quality Assessment skill, select **Assessment Rules** to activate or deactivate the current rules, or to add a new rule.

        If you choose to modify fields, select only the supported options from the lists provided as part of your input data.

        If you modify the inputs or triggers for a skill, you determine how and when a skill is used. You can't modify a skill's input data source. The data source contains the tables and fields that the skill relies on. However, you can copy a skill and customize it. For more information, see [Customize a Now Assist for Security Incident Response skill](cust-now-assist-security-incident-skill.md).

5.  Select **Save and continue** to go to the next step in the Guided Setup.

6.  Test the prompt on a security incident record.

7.  Select **Save and continue** to go to the next step in the Guided Setup.

8.  Choose one of the following options to define availability.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d385091e308">

Option

</th><th align="left" id="d385091e311">

Description

</th></tr></thead><tbody><tr><td id="d385091e317">

**Skill is always available**

</td><td>

Skill is always available to users.

</td></tr><tr><td id="d385091e326">

**Customize skill availability**

</td><td>

The skill is available only when certain conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>9.  Select **Save and continue** to go to the next step in the Guided Setup.

10. Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_x1c_5b2_1cc"><thead><tr><th align="left" id="d385091e361">

Option

</th><th align="left" id="d385091e364">

Description

</th></tr></thead><tbody><tr><td id="d385091e370">

**In-product**

</td><td>

Now Assist skills are displayed on forms and workspaces.

</td></tr><tr><td id="d385091e381">

**User roles**

</td><td>

Select the expand icon \(![Expand icon.](../image/icon-expand.png)\)

</td></tr><tr><td id="d385091e397">

**Now Assist panel**

</td><td>

Now Assist skills are available in the Now Assist panel. **Note:** If you don't see this option, you must activate the Now Assist panel. For more information, see [Activate Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

The security incident recommended actions and post-incident analysis skills are not available from the Now Assist panel.

</td></tr><tr><td id="d385091e427">

**Conversational experiences**

</td><td>

Verify where the skill is displayed and add roles for who can view it.Select **Now Assist Panel** in the Conversational experiences field to display the skill in the Now Assist panel.

</td></tr></tbody>
</table>11. Select **Save and continue** to go to the next step.

12. Add or remove roles.

    By default, the sn\_si.analyst and sn\_si.manager roles are added and can see the results from automated skills generation. You can add or remove roles only if you [Customize a Now Assist for Security Incident Response skill](cust-now-assist-security-incident-skill.md).

13. Review your choices and select **Activate** to complete the configuration for the skill.

14. Select **Return to Security Incident**.

    The skill is displayed in the Active skills section.



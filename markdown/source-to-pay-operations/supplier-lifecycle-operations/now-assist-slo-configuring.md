---
title: Configure Now Assist for Supplier Lifecycle Operations \(SLO\)
description: If you have the admin role, you can configure the Now Assist for Supplier Lifecycle Operations \(SLO\) application so that your supplier managers can use the generative AI skills in Source-to-Pay Workspace and in Core UI.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Now Assist for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure Now Assist for Supplier Lifecycle Operations \(SLO\)

If you have the admin role, you can configure the Now Assist for Supplier Lifecycle Operations \(SLO\) application so that your supplier managers can use the generative AI skills in Source-to-Pay Workspace and in Core UI.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see ServiceNow product tiers.

Role required: admin

## About this task

Use the Now Assist Admin console to configure Now Assist for SLO. This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see Overview tab in Now Assist Admin.

The following table lists the feature and skill that you can access from the Now Assist Admin console.

|Now Assist for SLO feature|Skill|
|--------------------------|-----|
|Case summarization|Supplier case summarization|
|KPI performance summarization|Supplier performance summarization|

![Now Assist skills for SLO section, showing the Case summarization and performance summarization feature cards.](../image/now-assist-slo-skills-activate.png "Now Assist skills for SLO")

## Procedure

1.  Install the Now Assist for Supplier Lifecycle Operations \(SLO\) plugin \(com.snc.sn\_supplier\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Supporting information for Now Assist for Supplier Lifecycle Operations \(SLO\)](../concept/now-assist-slo-supporting-info.md).
    -   For information about the installation process, see Install Now Assist plugins.
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Features** to access the **Now Assist Features** tab of the Now Assist Admin console.

3.  Expand the **Finance and Supply Chain** workflow group and select **Supplier Lifecycle Operations**.

    The Supplier Lifecycle Operations feature is located under the Finance and Supply Chain workflow group. Each feature has its associated skill.

4.  Activate and configure the required skill for Now Assist for Supplier Lifecycle Operations \(SLO\).

    **For example**

<table id="table_bcq_z34_tcc"><thead><tr><th>

Skill

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Supplier case summarization

</td><td>

1.  On the Case summarization skill card, select **View details**.
2.  In the All available Case summarization skills section, activate the Supplier case summarization skill by selecting **Activate skill**.


</td></tr></tbody>
</table>5.  Select **General Details**, review the details about the skill, and select **Save and continue** to go to the next step in the Guided Setup.

6.  Configure and active a skill by using the Guided Setup.

7.  Select **View Case Input** and review the base input table and input fields, and then select **Save and continue** to go to the next step in the Guided Setup.

8.  Test the prompt on a case by selecting **Customize &amp; Test Prompt** and then selecting **Save and continue** to go to the next step in the Guided Setup.

9.  Define the availability of the skill by selecting **Define Availability**, and then selecting one of the following options.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d28213e387">

Option

</th><th align="left" id="d28213e390">

Description

</th></tr></thead><tbody><tr><td id="d28213e396">

**Skill is always available**

</td><td>

The skill is available to users at all times.

</td></tr><tr><td id="d28213e405">

**Customize skill availability**

</td><td>

The skill is available only when certain conditions are met \(default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>10. Select **Save and continue** to go to the next step in the Guided Setup.

11. Display the Now Assist skills on forms and workspaces by selecting **Select display** and then **In-product desktop**.

12. Select **Save and continue** to go to the next step.

13. Review your choices and complete the configuration of the skill by selecting **Activate**.

14. Select **Return to Case summarization**.

    The skill is displayed in the Active skills section.


**Related topics**  


[Customize a Now Assist for Supplier Lifecycle Operations \(SLO\) skill for Case summarization](now-assist-slo-cust-skill.md)

[Customize Now Assist for Supplier Lifecycle Operations \(SLO\) to use the Virtual Agent chat](cust-now-assist-slo-va.md)

[Configure skill input for Now Assist for Supplier Lifecycle Operations \(SLO\)](../reference/now-assist-slo-skill-input-triggers.md)

[Use Now Assist for Supplier Lifecycle Operations \(SLO\)](../concept/now-assist-slo-using.md)


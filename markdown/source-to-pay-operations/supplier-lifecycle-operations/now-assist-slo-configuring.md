---
title: Configure ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)
description: Configure the ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) application to enable supplier managers to use generative AI skills in Source-to-Pay Workspace and Core UI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-configuring.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [generative AI, gen AI, genai, artificial intelligence, Now Assist Admin, Case summarization, KPI performance summarization]
breadcrumb: [ServiceNow Otto for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)

Configure the ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) application to enable supplier managers to use generative AI skills in Source-to-Pay Workspace and Core UI.

## Before you begin

**Note:** Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents. For more information, see [ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md).

Role required: admin

## About this task

Use the AI Admin Hub to configure ServiceNow Otto for SLO. This console contains everything that you need to install the plugins and configure the generative AI skills. For additional information, see [Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configuring-now-assist.md).

The following table lists the feature and skill that you can access from the AI Admin Hub.

|ServiceNow Otto for SLO feature|Skill|
|-------------------------------|-----|
|Case summarization|Supplier case summarization|
|KPI performance summarization|Supplier performance summarization|

\[Omitted image "now-assist-slo-skills.png"\] Alt text: Now Assist skills for Supplier Lifecycle Operations

## Procedure

1.  Install the ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) plugin \(com.snc.sn\_supplier\_gen\_ai\).

    -   For information about the plugin dependencies and plugin activation order, see [Supporting information for ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-supporting-info.md).
    -   For information about the installation process, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).
2.  Navigate to **All** &gt; **AI Admin Hub** &gt; **Skills** and select the **AI Skills** tab of the AI Admin Hub.

3.  Expand the **Finance and Supply Chain** workflow group and select **Supplier Lifecycle Operations**.

    The Supplier Lifecycle Operations features are grouped under the Finance and Supply Chain workflow group. Each feature has its associated skill.

4.  Activate and configure the AI skills for Supplier Lifecycle Operations.

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

6.  Configure and activate a skill by using the Guided Setup.

7.  Select **Choose input** for the skill and review the base input table and input fields, and then select **Save and continue** to go to the next step in the Guided Setup.

8.  Select **Customize and test Prompt** to test the prompt on a record

9.  Select **Save and continue** to go to the next step in the Guided Setup.

10. Select **Define Availability** and select one of the following options.

<table id="choicetable_e25_bvj_1cc"><thead><tr><th align="left" id="d121955e399">

Option

</th><th align="left" id="d121955e402">

Description

</th></tr></thead><tbody><tr><td id="d121955e408">

**Skill is always available**

</td><td>

The skill is available to users at all times.

</td></tr><tr><td id="d121955e417">

**Customize skill availability**

</td><td>

The skill is available only when certain conditions are met \(Default\).Use the condition builder to set your conditions.

</td></tr></tbody>
</table>11. Select **Save and continue** to go to the next step in the Guided Setup.

12. Choose **Select display** to determine where you'd like to display the skill.

<table id="choicetable_x1c_5b2_1cc"><thead><tr><th align="left" id="d121955e453">

Option

</th><th align="left" id="d121955e456">

Description

</th></tr></thead><tbody><tr><td id="d121955e462">

**In-product desktop**

</td><td>

AI skills are displayed on forms and workspaces.

</td></tr><tr><td id="d121955e471">

**ServiceNow Otto panel**

</td><td>

AI skills are available in the ServiceNow Otto panel. Turn on multi-language support for user-entered text with Dynamic Translation in ServiceNow Otto applications. For more information, see [Configure multilingual service for ServiceNow Otto applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/enable-dynamic-translation-for-now-assist-applications.md).**Note:** If you don't see this option, you must activate the ServiceNow Otto panel. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).

</td></tr></tbody>
</table>13. Select **Save and continue** to go to the next step.

14. Review your choices and complete the configuration of the skill by selecting **Activate**.

15. Select **Return to Supplier Lifecycle Operations**.

    The skill is activated.


**Related topics**  


[Customize a ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) skill for Case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-cust-skill.md)

[Customize ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) to use the Virtual Agent chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/cust-now-assist-slo-va.md)

[Configure skill input for ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-skill-input-triggers.md)

[Use ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo-using.md)


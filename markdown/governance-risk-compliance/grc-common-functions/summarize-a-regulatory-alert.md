---
title: Activate the Regulatory alert summarization skill
description: Activate and then configure the summarization skill from Now Assist to generate a brief summary of a regulatory alert by selecting the specific fields you would like included in the summary.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Now Assist, generative AI, GenAI, ServiceNow AI Platform]
breadcrumb: [Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Activate the Regulatory alert summarization skill

Activate and then configure the summarization skill from Now Assist to generate a brief summary of a regulatory alert by selecting the specific fields you would like included in the summary.

## Before you begin

Install the Now Assist for IRM plugin \(sn\_irm\_gen\_ai\).

Role required: admin or sn\_nowassist\_admin.nsa\_admin

## About this task

**Important:** After installing Now Assist for IRM, all Now Assist for IRM skills and agentic workflows are activated by default.

To summarize a regulatory alert, you must specify the fields from which the summary must obtain information. For example, while choosing the input data for the summary, you can specify the following fields from which data must be obtained:

-   Description
-   Regulatory authority
-   Effective date
-   Compliance date

Also, define when the skill must be available: should it be available at all times or should it be available only when a particular condition is met? By default, a regulatory alert in the Regulatory Change Management application shows the options to create a summary when the alert is in New state. However, you can specify any state or any condition under which the summarization can be done. You can achieve this when you modify the **Define availability** section. After you generate the summary, you can choose to share the summary and populate the **Additional comments** field of the regulatory alert. Doing this helps the regulatory analyst to get a quick glance at the summary. At every stage of the procedure ensure that you save the form.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **Now Assist Admin**.

2.  Select **Now Assist Features** &gt; **Technology** &gt; **Risk &amp; Sustainability** within the Now Assist Features tab.

3.  Select **Activate skill** under the **Regulatory alert summarization** skill.

4.  Select the General details section to review the following fields and confirm that the recommendation skill meets your requirements.

    **Note:**

    You can perform the following actions on Now Assist skills if you have the sn\_generative\_ai.nsa\_admin role:

    -   [Edit a Now Assist skill](https://www.servicenow.com/docs/access?context=edit-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [Make a copy of a Now Assist skill](https://www.servicenow.com/docs/access?context=make-a-copy-of-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [Troubleshoot a Now Assist skill](https://www.servicenow.com/docs/access?context=troubleshoot-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
<table id="id_o2v_k4c_cfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name of the skill

</td><td>

Name of the skill.

</td></tr><tr><td>

Add a brief description

</td><td>

Description of the Regulatory alert summarization skill.

</td></tr><tr><td class="sub-head" colspan="2">

**More details on the skills**

</td></tr><tr><td>

Product workflow

</td><td>

Name of the workflow.The Regulatory alert summarization skill is part of the Technology workflow.

</td></tr><tr><td>

Product name

</td><td>

Product name that these skills are associated with.The Regulatory alert summarization skill is part of the IRM \(Integrated Risk Management\) products, otherwise known as Risk &amp; Sustainability.

</td></tr><tr><td>

LLM service

</td><td>

LLM service used for this skill.

</td></tr><tr><td>

Skill template

</td><td>

Template used for this skill.

</td></tr></tbody>
</table>5.  Review the data that the large language model considers while creating the summary, select **Choose Input** and to view the Base table and Input templates used to collect data.

    The Base table and Input templates define how data is structured and transmitted to a large language model \(LLM\) for generating responses as part of the Regulatory Alert Summarization skill. These fields are read-only.

    These fields provide essential context to the LLM while preserving data integrity. Two input templates are defined based on the record’s state: one for the Default state and another for the New state. Each template includes rule conditions that determine when it’s applied. To enrich the context further, related tables are included, specifically linking regulatory alerts to taxonomy data using fields like taxonomy name and taxonomy category. This setup helps ensure that the LLM receives structured, relevant, and contextual information.

    For more information, see [Choose input data form](../reference/input-data-rcm-skill.md).

6.  To specify the conditions when the skill becomes available, select **Define availability**.

    1.  To ensure that the skill isn’t dependent on any condition and is always available, select **Skill is always available**.

    2.  To make the skill available only when certain conditions are met, such as the regulatory alert being in the New state, select **Customize skill availability** and build the conditions using the condition builder.

7.  To define the user roles that can access the skill, select **Define access** and add the required user roles.

8.  To view the skill in the application, select **Select display** and then toggle the **Display** button.

9.  Select **Save and continue**.

10. To view the details of the skill, select **Review and activate**.

11. Select **Return to Risk &amp; Sustainability** to return to the page listing all risk and sustainability-related skills or close the dialog box to remain on the same page.



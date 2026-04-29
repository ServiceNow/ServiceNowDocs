---
title: Activate Regulatory alert recommendation skills
description: Configure the recommendation skill from Now Assist to generate the recommendations of the impacted areas for a regulatory alert.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [Now Assist, generative AI, GenAI, ServiceNow AI Platform]
breadcrumb: [Configure, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Activate Regulatory alert recommendation skills

Configure the recommendation skill from Now Assist to generate the recommendations of the impacted areas for a regulatory alert.

## Before you begin

Install the Now Assist for IRM plugin \(sn\_irm\_gen\_ai\).

Role required: admin or sn\_nowassist\_admin.nsa\_admin

## About this task

**Important:** After installing Now Assist for IRM, all Now Assist for IRM skills and agentic workflows are activated by default.

Recommendation skills help regulatory analysts quickly identify impacted areas by generating AI-driven suggestions based on the content of a regulatory alert. These skills can be configured to be available at all times or conditionally triggered depending on the alert’s status. They’re typically accessible when the alert is in any state except Closed or Cancelled. To generate meaningful recommendations, the LLM analyzes defined data sources and input fields. After recommendations are generated, you can accept or dismiss them individually, with accepted recommendations helping to streamline impact analysis and improve compliance accuracy. For more information, see [Recommendation contexts and templates](../../grc-rcm/concept/recommendation-contexts.md).

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **Now Assist Admin**.

2.  Navigate to the Now Assist **Skills** tab and select **Technology** &gt; **Risk &amp; Sustainability**.

3.  Select the recommendation skill that you want to activate and then select **Activate skill**.

    |Option|Description|
    |------|-----------|
    |**Regulatory alert impacted citations**|Generate the recommendations for the citations of a regulatory alert.|
    |**Regulatory alert impacted control objectives**|Generate the recommendations for the control objectives of a regulatory alert.|
    |**Regulatory alert impacted controls**|Generate the recommendations for the controls of a regulatory alert.|
    |**Regulatory alert impacted policies**|Generate the recommendations for the policies of a regulatory alert.|

    **Note:** Make sure that all necessary recommendation skills are activated so that all relevant recommendations can be generated for impacted areas.

4.  Select the General details section to review the following fields and confirm that the recommendation skill meets your requirements.

    **Note:**

    You can perform the following actions on Now Assist skills if you have the sn\_generative\_ai.nsa\_admin role:

    -   [Edit a Now Assist skill](https://www.servicenow.com/docs/access?context=edit-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [Make a copy of a Now Assist skill](https://www.servicenow.com/docs/access?context=make-a-copy-of-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    -   [Troubleshoot a Now Assist skill](https://www.servicenow.com/docs/access?context=troubleshoot-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US)
    Activating a copy of a Regulatory alert impacted citations, Regulatory alert impacted control objectives, Regulatory alert impacted controls, or Regulatory alert impacted policies skill deactivates any other version of the same skill, including the default version.

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

Description of the Regulatory alert impacted citations, Regulatory alert impacted control objectives, Regulatory alert impacted controls, or Regulatory alert impacted policies skill.

</td></tr><tr><td class="sub-head" colspan="2">

**More details on the skills**

</td></tr><tr><td>

Product workflow

</td><td>

Name of the workflow.The Regulatory alert impacted citations, Regulatory alert impacted control objectives, or Regulatory alert impacted controls skills are part of the Technology workflow.

</td></tr><tr><td>

Product name

</td><td>

Product name that these skills are associated with.The Regulatory alert impacted citations, Regulatory alert impacted control objectives, Regulatory alert impacted controls, or Regulatory alert impacted policies skills are part of the IRM \(Integrated Risk Management\) products, otherwise known as Risk &amp; Sustainability.

</td></tr><tr><td>

LLM service

</td><td>

LLM service used for this skill.

</td></tr><tr><td>

Skill template

</td><td>

Template used for this skill.

</td></tr></tbody>
</table>5.  Define the user roles that can access the skill by selecting **Define access** and specifying a User access option.

<table id="choicetable_mvq_4wl_tgc"><thead><tr><th align="left" id="d31832e344">

Option

</th><th align="left" id="d31832e347">

Description

</th></tr></thead><tbody><tr><td id="d31832e353">

**Any authenticated user**

</td><td>

Any user that has successfully logged in can access this skill.

</td></tr><tr><td id="d31832e362">

**Select Roles**

</td><td>

A user with the role you specify can access this skill. **Note:** For recommendation skills, the default user roles are sn\_grc\_reg\_change.user or sn\_grc\_comp\_genai.reg\_change\_ai\_user.

</td></tr></tbody>
</table>6.  Select **Save and continue**.

7.  Specify whether you want the skill to be available in all Integrated Risk Management \(IRM\) products by selecting **Select display** and then toggling the **Display** button.

8.  Select **Save and continue**.

9.  Select **Review and activate** to view a setup summary for the skill.

    This includes a description of the skill, accessibility of the skill, and display option of the skill.

10. Select **Activate**.

    The Now Assist recommendation skills for a regulatory alert are activated.

11. Select **Return to Risk &amp; Sustainability** to return to the page listing all risk and sustainability-related skills or close the dialog box to remain on the same page.


## What to do next

You can now use a recommendation skills for regulatory alerts. You can generate recommendations for any regulatory alert that is not in the Closed or Cancelled state. For more information, see [Generate recommendations for a regulatory alert](create-recommendation-reg-alert.md).


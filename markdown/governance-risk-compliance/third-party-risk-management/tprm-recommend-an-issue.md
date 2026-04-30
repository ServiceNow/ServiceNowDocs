---
title: Activate TPRM issue recommendation skill
description: Activate the TPRM issue recommendation skill from Now Assist for TPRM to generate recommendations for TPRM issues.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, GenAI, ServiceNow AI Platform]
breadcrumb: [Configure, Now Assist, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Activate TPRM issue recommendation skill

Activate the TPRM issue recommendation skill from Now Assist for TPRM to generate recommendations for TPRM issues.

## Before you begin

Install the Now Assist for TPRM plugin \(sn\_tprm\_gen\_ai\).

Role required: admin

## About this task

**Important:** After installing Now Assist for TPRM, all Now Assist for TPRM skills are activated by default.

The recommendation skill helps third-party risk assessors quickly identify issues by generating AI-driven suggestions based on the content of assessment responses. Recommendations simplify the process of associating issues and creating tasks, and are accessible when an external assessment questionnaire has received responses.

To generate meaningful recommendations, data must be available from completed prior assessments and previously created issues. The recommendation skill uses these historical issues, along with their associated questions and responses, as reference data. After recommendations are generated, you can accept or dismiss them individually. For more information, see [Generate issue recommendations for TPRM](create-recommendation-tprm-issue.md).

**Note:** If you want generated issues to be created using historical data for individual third party, you need to navigate to **All** &gt; **System Properties** &gt; **All** select `sn_tprm_genai.same_vendor_required` and set the property to true.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **Now Assist Admin**.

2.  Navigate to the Now Assist **Skills** tab and select **Technology** &gt; **Risk &amp; Sustainability**.

3.  Select the **TPRM Issue recommendation** skill and then select **Activate skill**.

4.  View the skill in the Now Assist context menu by selecting **Select display** and then toggling the **Display** button.

    This skill is now available to be used in the Vendor Management Workspace.

5.  Select **Save and continue**.

6.  Review and confirm that the recommendation skill meets your requirements.

    1.  Select **Define access** review or update the conditions when the skill is accessible to users.

        |Field|Description|
        |-----|-----------|
        |Decision type|Allow if|
        |Roles|sn\_tprm\_genai.nowassist\_user|

<table id="table_rzt_smq_23c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Roles

</td><td>

sn\_tprm\_genai.nowassist\_user

 sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer

</td></tr></tbody>
</table>7.  Select **Save and continue**.

8.  Select **Review and activate** to view a setup summary for the skill.

    This includes a description of the skill, accessibility of the skill, and display option of the skill.

9.  Select **Activate**.

    The TPRM issue recommendations skill is activated.

10. Select **Return to Risk &amp; Sustainability** to return to the page listing all risk and sustainability-related skills or close the dialog box to remain on the same page.


## What to do next

You can now use the recommendation for TPRM issues skill. You can generate issue recommendations for questionnaires that are part of an external assessment with responses received. For more information, see [Generate issue recommendations for TPRM](create-recommendation-tprm-issue.md).


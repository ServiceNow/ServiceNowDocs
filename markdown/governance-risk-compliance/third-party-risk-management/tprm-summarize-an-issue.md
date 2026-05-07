---
title: Activate the TPRM issue summarization skill
description: Activate the TPRM summarization skill from Now Assist for TPRM to generate a brief summary of a TPRM issue by selecting the specific fields that you would like included in the summary.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, generative AI, GenAI, ServiceNow AI Platform]
breadcrumb: [Configure, Now Assist, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Activate the TPRM issue summarization skill

Activate the TPRM summarization skill from Now Assist for TPRM to generate a brief summary of a TPRM issue by selecting the specific fields that you would like included in the summary.

## Before you begin

Install the Now Assist for TPRM plugin \(sn\_tprm\_gen\_ai\).

Role required: admin

## About this task

**Important:** After installing Now Assist for TPRM, all Now Assist for TPRM skills are activated by default.

By default, a TPRM issue in the Third-party Risk Management application shows the options to create a summary in any state. After you generate the summary, you can choose to share the summary and populate the Work notes of the TPRM issue. Adding the summary to the work notes helps the risk analyst to get a quick glance at the latest summary version.

## Procedure

1.  Navigate to **All** &gt; **Admin Center** &gt; **Now Assist Admin**.

2.  Navigate to the Now Assist **Skills** tab and select **Technology** &gt; **Risk &amp; Sustainability**.

3.  Under the **TPRM issue summarization** skill, select **Activate skill**.

4.  View the skill in all Risk &amp; Sustainability products by selecting **Select display** and then toggling the **Display** button.

    The skill can be displayed in the Vendor Management Workspace and the workspaces of other Now Assist Risk &amp; Sustainability products when they are installed.

5.  Review and confirm that the summarization skill meets your requirements.

    1.  Review the data that the LLM considers while creating the summary, such as the Base table and Input templates used to collect data by selecting **Choose input**.

        The Base table and Input templates define how data is structured and transmitted to a large language model \(LLM\) for generating responses as part of the TPRM issue summarization skill. These fields are read-only.

    2.  Select **Define availability** review or update the conditions when the skill becomes available.

        1.  Ensure that the skill isn’t dependent on any condition and is always available by selecting **Skill is always available**.
        2.  Make the skill available only when certain conditions are met, such as the TPRM issue being in the New state by selecting **Customize skill availability** and build the conditions using the condition builder.
    3.  Update the definitions for user roles that can access the skill by selecting **Define access**.

        **Note:**

        You can perform the following actions on Now Assist skills if you have the sn\_generative\_ai.nsa\_admin role:

        -   [Edit a Now Assist skill](https://www.servicenow.com/docs/access?context=edit-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
        -   [Troubleshoot a Now Assist skill](https://www.servicenow.com/docs/access?context=troubleshoot-a-now-assist-skill&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).
6.  Select **Save and continue**.

7.  View the details of the skill by selecting **Review and activate**.

8.  Select **Activate** and then select **Risk &amp; Sustainability**.



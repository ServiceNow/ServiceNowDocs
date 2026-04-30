---
title: Analyze security operations metrics agentic workflow
description: Chat with an AI agent from the Now Assist panel to help you gain insight into how efficiently your security analysts are working with security incidents resolution.
locale: en-US
release: yokohama
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2025-04-22"
reading_time_minutes: 4
breadcrumb: [Analyze security operations metrics, Use agentic workflows, Now Assist for Security Incident Response, Security Operations]
---

# Analyze security operations metrics agentic workflow

Chat with an AI agent from the Now Assist panel to help you gain insight into how efficiently your security analysts are working with security incidents resolution.

## Before you begin

You must activate the Now Assist Security operations metrics analysis skill before you can use the AI agents with the Analyze security operations metrics agentic workflow. For more information, see [Configure a skill for Now Assist for Security Incident Response](activate-skills-for-now-assist-security-incident.md).

Role required: sn\_si.manager

## Procedure

1.  Select the Now Assist icon \(![Now Assist icon.](../../../common/image/icon-ai-sparkle.png)\) from anywhere in your instance.

    The Now Assist panel is displayed.

2.  Select **Analyze Security Operations Metrics** in the Now Assist panel.

3.  At the prompt, select **Analyze security incident metrics**.

    The Analyze security operations metrics agentic workflow case is on-demand. You can enter any query in natural language, but you might consider using the prompts described in the following table and steps to become familiar with the metrics data that is available and what you can do with it.

<table id="table_as3_vcb_x2c"><thead><tr><th>

Your request or response

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enter a name for one of your security analyst groups and request metrics, for example:-   **Analyze security operations metrics for L1 Analyst team.**
-   **Security metrics for L1 Analyst team for the past six months.**
-   **How did the L1 Analyst team perform last month?**


</td><td>

Specify a team by name and indicate a time period.

</td></tr><tr><td>

**End the session**, or **Stop**.

</td><td>

End the conversation.

</td></tr></tbody>
</table>    You might prefer to have the Security Incident Response workspace open in another tab so that you can refer to assignment groups, dates, and other information for your prompts.

    Your conversation is saved until you start a new chat. To start a new chat, select the New chat icon \(![New chat icon.](../../../common/image/icon-zoom-in.png)\).

    Your request is repeated and displayed in highlighted text with more information.

    After a few moments, you are prompted to provide more information about a specific analyst or an analyst group.

4.  Enter an assignment group name, for example, **L1 Analysts team**.

5.  At the prompt, enter a time range, for example, **The past six months**.

    The results for mean time to resolve \(MTTR\), mean time to assign \(MTTA\), and the total number of security incidents your team handled are displayed. Select the link for more information. A new tab opens with a list in UI16.

6.  Expand the **Sources** list and select the **Security Incident List** link.

    A list of security incidents that are assigned to the L1 Analysts group is displayed in a new tab in UI 16. At the top of the list, the date range that you requested \(**6 months**\) is displayed in the following format: `Opened > = 2024-09-23 > Opened < = 2025-03-23`. You are prompted if you would like to see more detailed analysis for MTTR, MTTA, or case volume.

    From this list, you can select a link to open individual security incidents to review. You can enter a record number from the list in the chat for the AI agent to summarize.

7.  Return to the chat and enter your request for a performance metric in natural language, for example, `Yes, dive deeper on MTTR.`

    More information is provided for your request that includes a summary and data organized into sections for fields on the security incident.

    -   Category Analysis - Breakdown by category. Examples might include `Unauthorized Access`,`Unpatched Vulnerability`, `False Positive`, and so on.
    -   Priority Analysis - Breakdown by severity: Critical, High, Moderate.
    -   Team Analysis - Breakdown of MTTR by team individual members.
    -   Outlier Analysis - Breakdown of security incidents that have unusually high, low, or other unique values.
8.  At the prompt, enter an affirmative response to the request for improvement suggestions.

    Your suggestions are displayed. Based on the results of the assessment, you might want to look up more information about specific types of security incidents.

9.  At the prompt, for example, request in natural language for all the security incidents in the phishing category that are in the state **Analysis**.

10. Select the **View results** link.

    A list of security incidents that match your request is provided in a new tab in UI16.

    From this list, you can open individual incidents and request summaries from the AI agent.

11. Modify system properties for the source fields that are used for metric analysis and the value for the outlier factor.

    -   sn\_sec\_gen\_ai.aia\_metric\_analysis\_dimensions - The AI agent breaks analysis down based on the following fields when analyzing MTTR and MTTA metrics: **category**, **priority**, **close\_code**, **assigned\_to**, **alert\_sensor**. Users with the sn\_si.manager and sn\_si.admin roles can modify this list.
    -   sn\_sec\_gen\_ai.aia\_metric\_analysis\_outlier\_factor - This property determines the outlier factor for MTTR and MTTA. The default outlier value is 2. By default, a record is an outlier if its MTTR exceeds 2 times the average time that it takes an assignment group to resolve security incidents for the time range that you requested. Users with the sn\_si.manager and sn\_si.admin roles can modify this value.


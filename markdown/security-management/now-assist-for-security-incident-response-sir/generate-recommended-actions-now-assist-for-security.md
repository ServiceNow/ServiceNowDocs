---
title: Generate recommended actions for a security incident with Now Assist for Security Incident Response
description: Automatically generate the next steps your analysts can take to help them close a security incident in the Security Incident Response Workspace. The recommended steps are based on existing security incidents and knowledge articles.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for Security Incident Response, Security Operations]
---

# Generate recommended actions for a security incident with Now Assist for Security Incident Response

Automatically generate the next steps your analysts can take to help them close a security incident in the Security Incident Response Workspace. The recommended steps are based on existing security incidents and knowledge articles.

## Before you begin

Recommended next steps work for active security incidents in any states other than **Closed** or **Cancelled**.

The AI Search application must be enabled so that the Recommended Actions skill works for security incidents. To verify AI Search is enabled on your instance, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. Contact support if the page indicates AI Search is not enabled.

Roles required: sn\_si.analyst, sn\_si.manager, or sn\_si.basic

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see Now Assist skills, agents, and agentic workflows on by default.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace** and open a security incident that is assigned to you.

2.  Select the **Recommended Actions** icon in the contextual sidebar.

    ![Recommended actions button selected in the contextual sidebar](../image/contextual-sidebar-genai.png)

3.  Select **Get recommendations**.

4.  In the Check AI generated content modal, select **I acknowledge**.

    Generated recommended actions are displayed in cards. Up to four references for the actions are displayed at the top. These references can be any combination of knowledge articles \(KB\)s or security incidents \(SIR\#\).

5.  In a card, choose one.

    |Option|Description|
    |------|-----------|
    |**View details**|View the details for this remediation action.|
    |**Save to work notes**|Review the work notes and have the option to edit them before you save them to the work notes of the security incident.|
    |**Select a Reference link**|View the security incident or the knowledge article used as the sources for these actions.|

    **Note:** Click **Show More** button to view the recommended actions in chronological order, guiding the security analysts through the next best steps for analyzing and investigating the security incident.

6.  Select the refresh icon in the Recommended actions panel to regenerate the recommended actions.

    The recommended actions remain cached for one hour. You might choose to refresh the recommended steps if:

    -   You believe information related to the security incident has changed since the last time you generated the actions.
    -   You leave the page, log out, log back in, and return within one hour to the security incident.
    You must regenerate the actions starting with step 3 to view the them after one hour.

7.  Click on the **Helpful** or **Not helpful** icons to share your feedback on the recommendations.

    **Note:** If you mark a recommendation as **Not Helpful**, then you’ll have the option to add detailed feedback which helps in improving the quality of future recommendations.

8.  Select **Create response task** on a card.

    A new tab opens in the workspace. The **Short description** and the **Description** fields are populated automatically from the details on the recommended action card you selected.

9.  Edit the form as needed and the select **Save** to create the response task.

    Until you change the Value on the system property, the two options on any recommended actions you generate remain **View details** and **Create response task**.

10. Create a response task from the recommended actions.

    By default, the workflow provides you with the option to save the recommended actions to work notes from the cards. If you want to have the option to create a response task from an action card instead of saving them to work notes, you must change the Value field for the **SecOps Recommended Action** \[sn\_sec\_ra.card\_action\_config\] system property.

    1.  As a user with the Security Incident Manager role \[sn\_si.manager\], navigate to sys\_properties.LIST.

    2.  Locate the SecOps Recommended Action \[sn\_sec\_ra.card\_action\_config\] system property and open the record.

    3.  Change the Value from `share_to_work_notes` to `create_task`.

    4.  Save the record.

    5.  Return to the security incident record and refresh the page.

        The action cards provide you with the options to **View details** and **Create response task**.



---
title: Generate closure notes for a security incident with Now Assist for Security Incident Response
description: Automatically generate a draft of the closure notes for a security incident when you close it. The draft is editable and will be reviewed prior to closing the security incident, and it can be used or modified as needed. Closure notes provide information about the resolution of a security incident to other analysts, managers, and key stakeholders.
locale: en-US
release: yokohama
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-01-14"
reading_time_minutes: 3
keywords: [Now Assist Security Operations]
breadcrumb: [Use generative AI skills, Now Assist for Security Incident Response, Security Operations]
---

# Generate closure notes for a security incident with Now Assist for Security Incident Response

Automatically generate a draft of the closure notes for a security incident when you close it. The draft is editable and will be reviewed prior to closing the security incident, and it can be used or modified as needed. Closure notes provide information about the resolution of a security incident to other analysts, managers, and key stakeholders.

## Before you begin

Roles required: sn\_si.analyst, sn\_si.manager or sn\_si.basic

**Note:**

If the Close code or Close notes fields are already updated for a security incident, Now Assist will not modify these fields, regardless of the incident’s current state. To enable Now Assist to update these fields, ensure that both the Close Code and Closure Notes fields are left blank.

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  In the legacy Core UI, navigate to **All** &gt; **Security Incident** &gt; **Incidents** and open a security incident that is assigned to you.

2.  Alternatively, navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace** and open a security incident that is assigned to you.

3.  Close the security incident.

<table id="choicetable_dkw_4rr_1cc"><thead><tr><th align="left" id="d286875e134">

Option

</th><th align="left" id="d286875e137">

Description

</th></tr></thead><tbody><tr><td id="d286875e143">

**Close the security incident in legacy Core UI16**

</td><td>

1.  Change the **State** field to **Closed**.

The Closure modal is displayed.

2.  Click on the **Close notes** section. The close notes will be auto-generated if no text exists, or you can modify the existing text as needed by choosing the required option from NACM.

**Note:** You might want to review the generated text and make sure it's accurate before you close the security incident. Edit the notes or delete them to provide your own. You can also **Elaborate** or **Shorten** the generated text.

3.  Select the required option from the Now Assist Context menu. **Elaborate** will help you to elaborate the text and replaces the selected resolution text. In case, if you wish to shorten the resolution text you can select **Shorten** option from the Context menu to make the text more concise.
4.  Update the Close code and select **Close incident**.

The resolution summary is displayed in the Resolution Information section on the security incident record.

**Note:** Using the Now Assist Context menu, you can directly add or generate the resolution notes in the **Close notes** section on the incident record itself, when the incident is in the **Review** state. For more information, see the screen shot below.

</td></tr><tr><td id="d286875e213">

**Close the security incident from the Security Incident Response Workspace**

</td><td>

1.  On the **Details** tab of the workspace, change the **State** field to **Closed**.

The stepper modal is displayed.

2.  Review each step and select **Next**.
3.  Select **Provide resolution details**
4.  Click on the **Close notes** section. The close notes will be auto-generated if no text exists, or you can modify the existing text as needed using the NowAssist options.

**Note:** You might want to review the generated text and make sure it's accurate before you close the security incident. Edit the notes or delete them to provide your own. You can also **Elaborate** or **Shorten** the generated text.

5.  Select the required option from the Now Assist Context menu. **Elaborate** will help you to elaborate the text and replaces the selected resolution text. In case, if you wish to shorten the resolution text you can select **Shorten** option from the Context menu to make the text more concise.
6.  Update the Close code and select **Close incident**.

The resolution summary is displayed on the **Details** tab on the security incident record in the workspace.

**Note:** Using the Now Assist Context menu, you can directly add or generate the resolution notes in the **Close notes** section on the incident record itself, when the incident is in the **Review** state. For more information, see the screen shot below.

</td></tr></tbody>
</table>    The following screen shot depicts the resolution notes generated for closing the security incident in Core UI16.

    ![Close the security incident - Resolution notes generated in Core UI16.](../image/NA-RN-UI16.png)

    Auto-generated resolution notes from the Security Incident Response Workspace.

    ![Resolution Notes on the Security Incident Response workspace](../image/NA-RN-NAPanel.png)

    Edit the resolution notes generated using the Now Assist context menu on the Security Incident Response workspace.

    ![Now Assist Context menu for the Close notes.](../image/NA-R-notes.png)



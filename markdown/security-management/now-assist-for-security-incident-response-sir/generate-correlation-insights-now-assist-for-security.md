---
title: Generate correlation insights in the Now Assist panel with Now Assist for Security Incident Response
description: Generate correlation insights from the Now Assist panel to help you connect past events to the security incident that you are working on.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore correlation insights, Use generative AI skills, Now Assist for Security Incident Response, Security Operations]
---

# Generate correlation insights in the Now Assist panel with Now Assist for Security Incident Response

Generate correlation insights from the Now Assist panel to help you connect past events to the security incident that you are working on.

## Before you begin

Roles required: sn\_si.analyst, sn\_si.manager, or sn\_si.basic

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace** and open a security incident that is assigned to you.

2.  Alternatively, in the legacy UI \(UI16\), locate a security incident on the Security Incidents \[sn\_si\_incident\] table and open it.

3.  Select the Now Assist icon \(![AI Sparkle icon.](../../../common/image/icon-ai-sparkle.png)\) in the top header to open the Now Assist panel.

4.  Select **Generate correlation insights**.

    Correlation insights are generated if one or more of the following values can be matched. The following filters to base your insights on are displayed in the Now Assist panel. Only the filters that have matches to other security incidents are displayed.

    **Note:** If you do not have a security incident record open, you are prompted to enter the number for a security incident record after you select **Generate correlation insights**.

    -   **Configuration item** \(CI\): Records that have the same CI to help you identify potential vulnerabilities in specific systems. An example might be a user’s laptop.
    -   **Affected user**: Past incidents that have the same user to help you see patterns such as frequent phishing attempts or multiple unauthorized access attempts. An example is a specific user’s name.
    -   **Observables**: Records that are linked by shared observables that suggest potential ongoing attacks or repeated use of malicious infrastructure. Examples might include IP addresses, URLs, or file hashes. You must enter an exact value for an observable, for example, a complete file hash.
    If no matching data exists for any of these filters, none are displayed. You are prompted to add one of these values to the security incident that you are working from, save it, and reset your conversation in the panel and try again.

5.  Reset your conversation by selecting the Now Assist more options menu icon \(![More options menu icon.](../image/now-assist-reset-icon.png)\) in the panel and select **Reset Conversation**.

6.  Select a filter.

    Matching results are displayed in the Now Assist panel.

    In the following example, **Configuration item** was requested. The search returned a high-level summary and links to records that have a matching configuration item.

    Results are grouped by record type: security incident record \(SIR\), incident \(INC\), change request \(CHG\), problem \(PRB\), and vulnerable item \(VIT\).

    -   The Affected users filter returns: SIR, INC, and CHG records.
    -   The Configuration filter item returns: SIR, INC, CHG, PRB, and VIT records.
    -   The Observables filter returns SIR records.
    ![Now Assist panel with returned records for a configuration item for correlation insights.](../image/NAP-C-Insights.png)

7.  Modify the 30-day limit for the query by following these steps:

    1.  As a user with the Security Incident Manager role \[sn\_si.manager\], navigate to sys\_properties.LIST.

    2.  Locate the Correlation lookback period \[sn\_sec\_gen\_ai.correlation\_lookback\_period\] system property and open the record.

    3.  Enter a number in the **Value** field up to 360.

    4.  Save the record.

    5.  Return to the security incident record and refresh the page.



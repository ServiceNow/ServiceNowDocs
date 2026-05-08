---
title: Generate correlation insights from the Security Incident Response Workspace with Now Assist for Security Incident Response
description: Generate and view correlation insights in the Security Incident Response Workspace to help you connect past events to the security incident you're working on.
locale: en-US
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore correlation insights, Use generative AI skills, Now Assist for Security Incident Response, Security Operations]
---

# Generate correlation insights from the Security Incident Response Workspace with Now Assist for Security Incident Response

Generate and view correlation insights in the Security Incident Response Workspace to help you connect past events to the security incident you're working on.

## Before you begin

Roles required: sn\_si.analyst, sn\_si.manager, or sn\_si.basic

## About this task

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see Now Assist skills, agents, and agentic workflows on by default.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace** and open a security incident that is assigned to you.

2.  Select the **Investigation** tab on the security incident record.

3.  Select one or more filters that you want to base your correlation insights on.

    You can select more than one observable.

    -   **Associated Observables**: Records that are linked by shared observables that suggest potential ongoing attacks or repeated use of malicious infrastructure. Examples might include IP addresses, URLs, or file hashes.
    -   **Configuration items** \(CI\): Records that have the same CIs to help you identify potential vulnerabilities in specific systems. An example might be users' laptops.
    -   **Affected Users**: Past incidents that have the same users to help you see patterns such as frequent phishing attempts or multiple unauthorized access attempts. An example is a specific user’s name.
    A list of matching items is displayed.

4.  Select the items from the list that you want to generate insights for.

5.  Select **Generate Insights**.

    A dialog opens. After a few moments, your correlation insights are displayed. You have the following options from this dialog:

    -   Refresh insights \(![Circling arrows icon that refresh the page.](../../secops-integration-threat-security-center/image/enrich-refresh-icon.png)\) - You can change the items in the list after your initial insights are generated and update your results.
    -   Expand \(![Arrows icon that expands the page.](../../../common/image/icon-fit-to-screen.png)\) - Resize the dialog and drag it around on the page.
    You have the following options for each correlation insight entry in the dialog.

    -   **Change time range** - Select a time range to reload the dialog with matching insights. Your results for this entry are automatically regenerated if you select a new time range. The time range for each entry is displayed next to the insight, for example, `35.35.35.35. (100 days)`.
    -   Last generated - The date that the insight was last generated.
    -   Rate the content - \(![Thumbs up icon for helpful.](../image/icon-helpful.png)\) and \(![Thumbs down icon for not helpful.](../image/icon-not-helpful.png)\).
    -   Copy - \(![Pages icon to show copy action.](../image/icon-copy.png)\) Copy the insight to the clipboard.
    -   **Share to work notes** - Edit the content and publish it to the work notes on the security incident.
    Correlation insights are stored for observables when you generate them for the first time based on the default lookup period \(30 days\). These insights are stored until you regenerate insights for the observables with a different lookup period. Modify the 30-day limit for the query by following these steps:

    1.  As a user with the Security Incident Manager role \[sn\_si.manager\], navigate to sys\_properties.LIST.
    2.  Locate the Correlation lookback period \[sn\_sec\_gen\_ai.correlation\_lookback\_period\] system property and open the record.
    3.  Enter a number in the **Value** field up to 360.
    4.  Save the record.
    5.  Return to the security incident record and refresh the page.
    6.  Generate correlation insights. Your results are based on your new lookup period.


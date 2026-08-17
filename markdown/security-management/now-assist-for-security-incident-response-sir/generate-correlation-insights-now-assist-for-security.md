---
title: Generate correlation insights in the ServiceNow Otto panel
description: Generate correlation insights from the ServiceNow Otto panel to help you connect past events to the security incident that you're working on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/now-assist-for-security-incident-response-sir/generate-correlation-insights-now-assist-for-security.html
release: australia
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore correlation insights, Use generative AI skills, ServiceNow Otto for Security Incident Response \(SIR\), Security Operations]
---

# Generate correlation insights in the ServiceNow Otto panel

Generate correlation insights from the ServiceNow Otto panel to help you connect past events to the security incident that you're working on.

## Before you begin

Roles required: sn\_si.analyst, sn\_si.manager, or sn\_si.basic

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Security Incident Response Workspace** and open a security incident that is assigned to you.

2.  Alternatively, in the legacy UI \(UI16\), locate a security incident on the Security Incidents \[sn\_si\_incident\] table and open it.

3.  Select the ServiceNow Otto icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: AI Sparkle icon.\) in the top header to open the ServiceNow Otto panel.

4.  Select **Generate correlation insights**.

    Correlation insights are generated if one or more of the following values can be matched. The following filters to base your insights on are displayed in the panel. Only the filters that have matches to other security incidents are displayed.

    **Note:** If you don't have a security incident record open, you are prompted to enter the number for a security incident record after you select **Generate correlation insights**.

    -   **Configuration item** \(CI\): Records that have the same CI to help you identify potential vulnerabilities in specific systems. An example might be a user’s laptop.
    -   **Affected user**: Past incidents that have the same user to help you see patterns such as frequent phishing attempts or multiple unauthorized access attempts. An example is a specific user’s name.
    -   **Observables**: Records that are linked by shared observables that suggest potential ongoing attacks or repeated use of malicious infrastructure. Examples might include IP addresses, URLs, or file hashes. You must enter an exact value for an observable, for example, a complete file hash.
    If no matching data exists for any of these filters, none are displayed. Add one of these values to the security incident that you're working from, save it, and reset your conversation in the panel and try again.

5.  Reset your conversation by selecting the **More options menu** icon \(\[Omitted image "now-assist-reset-icon.png"\] Alt text: More options menu icon.\) in the panel and select **Reset Conversation**.

6.  Select a filter.

    Matching results are displayed in the panel.

    In the following example, **Configuration item** was requested. The search returned a high-level summary and links to records that have a matching configuration item.

    Results are grouped by record type: security incident record \(SIR\), incident \(INC\), change request \(CHG\), problem \(PRB\), and vulnerable item \(VIT\).

    -   The Affected users filter returns: SIR, INC, and CHG records.
    -   The Configuration filter item returns: SIR, INC, CHG, PRB, and VIT records.
    -   The Observables filter returns SIR records.
    \[Omitted image "NAP-C-Insights.png"\] Alt text: ServiceNow Otto panel with returned records for a configuration item for correlation insights.

7.  Modify the 30-day limit for the query by following these steps:

    1.  As a user with the Security Incident Manager role \[sn\_si.manager\], navigate to sys\_properties.LIST.

    2.  Locate the Correlation lookback period \[sn\_sec\_gen\_ai.correlation\_lookback\_period\] system property and open the record.

    3.  Enter a number in the **Value** field up to 360.

    4.  Save the record.

    5.  Return to the security incident record and refresh the page.



---
title: Exploring correlation insights with Now Assist for Security Incident Response
description: You can generate correlation insights to help you avoid duplicating your investigation into affected users, configuration items, and observables and help you resolve the security incident that you are working on more quickly. You select the criteria from a security incident that you want to base the correlation insights on.
locale: en-US
release: xanadu
product: Now Assist for Security Incident Response \(SIR\)
classification: now-assist-for-security-incident-response-sir
topic_type: concept
last_updated: "2025-01-22"
reading_time_minutes: 3
breadcrumb: [Using Now Assist for Security Incident Response to close security incidents, Now Assist for Security Incident Response, Security Operations]
---

# Exploring correlation insights with Now Assist for Security Incident Response

You can generate correlation insights to help you avoid duplicating your investigation into affected users, configuration items, and observables and help you resolve the security incident that you are working on more quickly. You select the criteria from a security incident that you want to base the correlation insights on.

## Generating correlation insights from the Security Incident Response Workspace

Starting with version 3.2.1 of Now Assist for Security Incident Response, you can generate and view correlation insights in the Security Incident Response Workspace.

-   Generate correlation insights from the **Investigation** tab for a security incident in any state in the Security Incident Response Workspace.
-   The agent asks you which CI or Affected user you would you like to correlate the security incident with from the related lists. Previously, if you selected a configuration item \(CI\) or affected user to base your insights on, the lookup returned the primary affected user or primary CI associated with a security incident.
-   You can generate insights for multiple items simultaneously for **Associated Observables**, **Configuration items**, and **Affected Users**.
-   Results are displayed in a modeless dialog that you can resize and move.
-   Your time range for the lookup of correlation is 30 days.

    **Note:** After you generate an observable associated with a security incident, the insights are stored for that observable until you regenerate it with a different time range. Your insights for your new time range are displayed.


The correlation insights generation skill must be activated before you can see the **Generate correlation insights** option in the Security Incident Response Workspace. For more information, see [Configure and activate a skill for Now Assist for Security Incident Response](activate-skills-for-now-assist-security-incident.md).

## Generating correlation insights from the Now Assist panel in the Security Incident Response Workspace and in UI \(UI16\)

-   You can generate correlation insights from a security incident record in any state in the Security Incident Response Workspace or in the legacy UI \(UI16\).
-   By default, correlation insights search for matching records from the last 30 days.
-   You can locate and review values for the **Configuration item**, **Affected user**, and **Observables** for correlation insights filters on the **Details** tab in the Security Incident Response workspace, or on the **Configuration Items**, **Affected Users**, and **Observables** related lists in the legacy UI \(UI16\).
-   Your search criteria and results remain displayed in the Now Assist panel until you reset the conversation. To reset your conversation, select the Now Assist reset menu icon \(![](../image/now-assist-reset-icon.png)\) in the panel and select **Reset Conversation**.
-   You must have access to the following tables to view these records in the generated correlation insights:
    -   Configuration item \[cmdb\_ci\] table.
    -   Incident \[incident\] table.
    -   Change request \[change\_request\] table.
    -   Problem \[problem\] table.
    -   Vulnerable item \[sn\_vul\_vulnerable\_item\] table.
    -   Associate observable \[sn\_ti\_observable\] table.
-   Your results for correlation insights are based on the tables that you have access to. For example, if you want to view vulnerable items \(VIT\)s in your correlation insights results, you must have the Vulnerability Response application installed and the read access role \(sn\_vul.read\_all\).

For the steps to generate correlation insights, see [Generate correlation insights with Now Assist for Security Incident Response](generate-correlation-insights-now-assist-for-security.md).


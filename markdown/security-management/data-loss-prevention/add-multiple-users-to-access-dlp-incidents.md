---
title: Add multiple users to access DLP incidents
description: Use the escalation chain feature to allow all the respective users who are involved in the incident to access the DLP incidents from the list view, though the incident is assigned to a different user.
locale: en-US
release: australia
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create response due date rules, Administer, Data Loss Prevention Incident Response, Security Operations]
---

# Add multiple users to access DLP incidents

Use the escalation chain feature to allow all the respective users who are involved in the incident to access the DLP incidents from the list view, though the incident is assigned to a different user.

## Before you begin

Role required:

-   sn\_dlir.admin - Create, edit, and delete.
-   sn\_dlir.read, sn\_dlir.analyst, and sn\_dlir.analyst\_read - View \(read-only\).

## Procedure

1.  Navigate to **DLP** &gt; **DLP Analyst Workspace**.

    On the list view, the users and their delegates should be able to view the DLP incident under **Escalated** incidents tab on the end user portal.

2.  Open any incident.

3.  Click **Escalate** button to escalate an incident.

4.  Select the user or user group from the drop down list.

    You can add multiple users to the escalation chain, all the users who has access are listed on the Details section of the form view and also under the **All** incidents tab. The escalation chain is displayed based on the configuration settings. For more information, see [Configure advanced settings](configure-advanced-settings-dlp.md)

5.  Click **Submit**.

    After you submit, the incident will then be assigned to a manager however the end user can still view the incident.

6.  To verify this, navigate to the **DLP User Workspace** as an end user.

    All the incidents that are assigned to the end user are displayed.

7.  View the escalated incidents list under the **Escalated Incidents** section.

    You can also view the users access list under the **Escalation Chain** column on the list view.

8.  Open any incident.

9.  Click **Respond** button to submit incident response.

10. Select the response from the drop down list.

11. Click **Submit**.


**Parent Topic:**[Create response due date rules](setup-response-due-date-rules.md)


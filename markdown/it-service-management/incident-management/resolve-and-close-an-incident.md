---
title: Resolve and close an incident
description: When the service is restored by rectifying the issue that resulted for an incident, you can set the incident state as resolved. If the user is satisfied with the resolution, the user can close the incident. The incident can also auto-close after a certain time based on the incident auto-close properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/incident-management/resolve-and-close-an-incident.html
release: brazil
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Incident resolution and closure, Managing incidents, Incident Management, IT Service Management]
---

# Resolve and close an incident

When the service is restored by rectifying the issue that resulted for an incident, you can set the incident state as resolved. If the user is satisfied with the resolution, the user can close the incident. The incident can also auto-close after a certain time based on the incident auto-close properties.

## Before you begin

Role required:

-   For resolution: itil, list\_updater, sn\_incident\_write, or admin
-   For closure: itil\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

    **Note:** If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the UI16 module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/service-operations-workspace/redirect-ui16-module-links-sow.md).

2.  Open the incident that you want to resolve and close.

3.  In the Resolution Information section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Resolved by|The user who resolved the issue and the date and time the incident was closed.|
    |Resolved|The date and time when the incident was resolved.|
    |Resolution code|Information to categorize resolved cases.|
    |Resolution notes|Document how an incident is resolved.|

4.  Click **Resolve**.

    The incident is in the resolved state.

    **Note:** When an incident is put to **On-Hold** state with reason as **Awaiting Caller Information**, a notification for input response is sent to the caller for a specific number of attempts or strikes within specific time intervals. The business days are considered for a time interval. If the caller adds a comment on the Service Portal or replies to the notification email, the incident automatically moves to the **In Progress** state, and the assigned agent receives a notification. If the caller does not respond after all attempts are exhausted, the incident is automatically resolved with the resolution code **Resolved - No response from caller** and a resolution note indicating no caller response. You can control the number of attempts or strikes and the time interval between the attempts, using the following incident properties:

    -   **The number of attempts made before an incident that is waiting for a caller response is automatically resolved if no reply is received. Setting this value to 0 will disable the automation for this instance** \(**com.snc.incident.strike.count**\) - By default, the value is set to 3.
    -   **Wait period in business days between two attempts. Incidents will be auto resolved after all the attempts are completed** \(**com.snc.incident.strike.wait\_period**\) - By default, the value is set to 1.
5.  Click **Close Incident**.

    The incident is closed.

    **Note:** Even when an incident is closed or canceled, you can edit the following fields on the Incident form, if you have an admin role: **Subcategory**, **Service**, **Service Offerings**, **Description**, **Contact type**, **Watch list**, **Work notes list,** **Parent Incident**, **Problem**, **Change Request**, **Caused by Change**, **Resolved by**, **Resolved**, **Reassignment count**.


**Parent Topic:**[Incident resolution and closure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/incident-management/c_IncidentResolutionAndRecovery.md)


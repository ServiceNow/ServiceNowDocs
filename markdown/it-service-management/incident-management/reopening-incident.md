---
title: Reopening an incident
description: Reopen an incident from the resolution notification email or from the incident to get answer for your query.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# Reopening an incident

Reopen an incident from the resolution notification email or from the incident to get answer for your query.

When an incident is resolved, an incident resolution email notification is sent to you. If you are not satisfied with the resolution of your incident, you can request to reopen the incident using any of the following methods:

-   Select the **Reopen incident** link from the incident resolution email notification.
-   Select the **Reopen incident** option on the incident form in Incident Management.

Once an incident is reopened, the state of the incident is then changed from **Resolved** to **In Progress**. You can reopen a resolved incident if you are an agent with incident write access \(sn\_incident\_write\) role.

If the incident is already closed and you request to reopen the incident by replying to the resolution notification email, a new incident is opened with selected field values from the closed incident. The values of the fields that you mention in the **List of fields \(comma-separated\) to copy from the original incident when an incident is reopened by email** property \(**com.snc.incident.clone\_fields\_on\_reopen**\) are copied from the closed incident to the new incident. Add the text `Please reopen` to the subject line of the email.

-   If an incident is reopened by a user after it was resolved, the **Last reopened by** and the **Last reopened at** fields are automatically populated with the name of the person who reopened it and the date and time when the incident is reopened. During audit, this information helps you to generate various reports for reopened incidents.
-   On the Incident form, there is an existing field named **Reopen count**. Incidents that were reopened prior to the Kingston release, may already have some non-zero values in the **Reopen count** field while the values in the new fields, **Last reopened by** and the **Last reopened at** are null. For incidents that are reopened after the Kingston release, the **Last reopened by** and the **Last reopened at** fields are populated.
-   If you do not have any roles in the system \(ESS\) and you change the incident state to **Resolved**, you receive a notification with a **Reopen incident** link.
-   If you do not have any roles in the system \(ESS\) and you are the caller, you can click **Reopen incident** on the incident form to reopen the incident. Add the text `Please reopen` to the subject line of the email.

    **Note:** An ESS user is not able to resolve, reopen, or close a major incident even if the user is the caller.



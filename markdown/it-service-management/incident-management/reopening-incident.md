---
title: Reopening an incident
description: Reopen a resolved incident from the incident's resolution notification email or from the incident form in Incident Management to further investigate an issue that is still impacting you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/reopening-incident.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Managing incidents, Incident Management, IT Service Management]
---

# Reopening an incident

Reopen a resolved incident from the incident's resolution notification email or from the incident form in Incident Management to further investigate an issue that is still impacting you.

When an incident is resolved, an incident resolution email notification is sent to you. If you are not satisfied with the resolution of your incident, you can request to reopen the incident using any of the following methods:

-   Select the **Reopen incident** link from the incident resolution email notification.
-   Select the **Reopen** option on the incident form in Incident Management or the Portal UIs, such as Service Portal and Employee Service Center \(ESC\) portal.

\[Omitted image "reopen-incident-form.png"\] Alt text: Reopen option on the incident form

\[Omitted image "reopen-service-portal.png"\] Alt text: Reopen option in the service portal

\[Omitted image "reopen-employee-center.png"\] Alt text: Reopen option in the Employee Service Center portal

After an incident is reopened, its state changes from **Resolved** to **In Progress**.

The following conditions are applicable when reopening an incident:

-   You can reopen a resolved incident if you are an agent with incident write access \(sn\_incident\_write\), the caller, or the **Opened by** \(requester\) user for the incident.
-   Both the caller and the requester can view and use the **Reopen incident** option on the Portal UIs, such as Service Portal and ESC portal.
-   Agents can view and use the **Reopen** option on the incident form to reopen any assigned incident. On the Portal UI, the **Reopen incident** option is available only for incidents assigned to you, or where you are the caller or requester.
-   If an resolved incident is reopened by a user, the **Last reopened by** and the **Last reopened at** fields are automatically populated with the user who reopened it along with the date and time. During audit, this information helps you to generate various reports for reopened incidents.
-   On the Incident form, there is an existing field named **Reopen count**. Incidents that were reopened before the Kingston release may already have some non-zero values in the **Reopen count** field while the values in the **Last reopened by** and the **Last reopened at** fields are null. For incidents that are reopened after the Kingston release, the **Last reopened by** and the **Last reopened at** fields are populated.
-   If you're an employee self-service \(ESS\) user with no roles in the system and you change the incident state to **Resolved**, you receive a notification with a **Reopen incident** link.
-   If you do not have any roles in the system \(ESS\) and you are the caller, you can select **Reopen** on the incident form to reopen the incident.

    **Note:** An ESS user can't resolve, reopen, or close a major incident even if the user is the caller.


If the incident is already closed, you cannot reopen that incident. However, you can request to reopen the incident by replying to the resolution notification email. In such case, a new incident is opened with selected field values that are copied from the closed incident. To enable this feature, you must add fields as values in the **List of fields \(comma-separated\) to copy from the original incident when an incident is reopened by email** \(**com.snc.incident.clone\_fields\_on\_reopen**\) incident property. These fields are copied from the closed incident to the new incident. Add the text `Please reopen` to the subject line of the email.


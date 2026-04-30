---
title: Reopening an incident
description: Reopen a resolved incident from the incident’s resolution notification email or from the incident form in Incident Management to further investigate an issue that is still impacting you.
locale: en-US
release: zurich
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage, Incident Management, IT Service Management]
---

# Reopening an incident

Reopen a resolved incident from the incident’s resolution notification email or from the incident form in Incident Management to further investigate an issue that is still impacting you.

When an incident is resolved, an incident resolution email notification is sent to you. If you are not satisfied with the resolution of your incident, you can request to reopen the incident using any of the following methods:

-   Select the **Reopen incident** link from the incident resolution email notification.
-   Select the **Reopen** option on the incident form in Incident Management or the Portal UI’s such as Service Portal and Employee Service Center \(ESC\) portal.

![Reopen option on the incident form](../image/reopen-incident-form.png "Reopen option on the incident form")

![Reopen option in the service portal](../image/reopen-service-portal.png "Reopen option in the Service portal")

![Reopen option in the service portal](../image/reopen-employee-center.png "Reopen option in the Employee Service Center (ESC) portal")

Once an incident is reopened, the state of the incident is then changed from **Resolved** to **In Progress**.

The following conditions are applicable when reopening an incident:

-   You can reopen a resolved incident if you are an agent with incident write access \(sn\_incident\_write\), or caller, or **Opened by** \(requester\) user for the incident.
-   Both the caller and the requester can view and use the **Reopen incident** option on the Portal UIs, such as Service Portal and ESC portal.
-   If you are an agent, you can view and use the **Reopen** option on the incident form to reopen any incident that is assigned to you or to other agents. However, on the Portal UI, you can only view and use the **Reopen incident** option to reopen an incident if it’s assigned to you or you are the caller or requester for the incident.
-   If an incident is reopened by a user after it was resolved, the **Last reopened by** and the **Last reopened at** fields are automatically populated with the name of the person who reopened it and the date and time when the incident is reopened. During audit, this information helps you to generate various reports for reopened incidents.
-   On the Incident form, there is an existing field named **Reopen count**. Incidents that were reopened prior to the Kingston release, may already have some non-zero values in the **Reopen count** field while the values in the new fields, **Last reopened by** and the **Last reopened at** are null. For incidents that are reopened after the Kingston release, the **Last reopened by** and the **Last reopened at** fields are populated.
-   If you do not have any roles in the system \(ESS\) and you change the incident state to **Resolved**, you receive a notification with a **Reopen incident** link.
-   If you do not have any roles in the system \(ESS\) and you are the caller, you can click **Reopen** on the incident form to reopen the incident.

    **Note:** An ESS user is not able to resolve, reopen, or close a major incident even if the user is the caller.


If the incident is already closed, you cannot reopen that incident. However, if you request to reopen the incident by replying to the resolution notification email, a new incident is opened with selected field values that are copied from the closed incident. To enable this feature, you must add fields as values in the **List of fields \(comma-separated\) to copy from the original incident when an incident is reopened by email** \(**com.snc.incident.clone\_fields\_on\_reopen**\) incident property. These fields are copied from the closed incident to the new incident. Add the text `Please reopen` to the subject line of the email.


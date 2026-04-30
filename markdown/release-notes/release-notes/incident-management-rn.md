---
title: Incident Management release notes
description: The ServiceNow Incident Management application restores normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
---

# Incident Management release notes

The ServiceNow® Incident Management application restores normal service operations while minimizing the impact to business operations and maintaining quality. Incident Management was enhanced and updated in the Xanadu release.

## Incident Management highlights for the Xanadu release

Control when an incident record link in the email notifications redirects to the incident record in Service Operations Workspace \(SOW\).

See [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information.

## Changed in this release

-   **[Email notification link redirection behavior](https://www.servicenow.com/docs/access?context=t_ViewIncidentNotification&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    In email notifications, you can now decide where the links to an incident record are redirected. Instead of an incident record automatically opening in the classic UI16 interface in Incident Management, the incident record can be opened in SOW. The incident record link in an email notification opens in SOW only if the following conditions are met:

    -   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) system property is set to true.
    -   The user selecting the incident record link has the sn\_sow.sow\_user role.
    The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior.

    To ensure consistency, the email notification template is updated to send the notification from SOW in the same format as sent from classic UI16 interface. Also, the template theme is updated to match the Next Experience theme.


## Activation information

Incident Management is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[IT Service Management release notes](it-service-management-rn-landing.md)


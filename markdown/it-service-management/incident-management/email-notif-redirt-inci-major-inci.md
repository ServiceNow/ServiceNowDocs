---
title: Email notification redirection for incidents and major incidents
description: You can redirect users from email notification links to incident or major incident records in Service Operations Workspace \(SOW\) instead of the UI16 interface of Incident Management or Major Incident Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/email-notif-redirt-inci-major-inci.html
release: australia
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [View incident notifications, Configuring Incident Management, Incident Management, IT Service Management]
---

# Email notification redirection for incidents and major incidents

You can redirect users from email notification links to incident or major incident records in Service Operations Workspace \(SOW\) instead of the UI16 interface of Incident Management or Major Incident Management.

## Email notification redirection for Incident Management

In incident email notifications, you can decide where the links to an incident record are redirected. Instead of an incident record automatically opening in the UI16 interface in Incident Management, the record can be opened in SOW.

The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior. The incident record link in an email notification opens in SOW only if you have the sn\_sow.sow\_user role and any of the following conditions are met:

-   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`. Setting this property to true enables the email redirection behavior for all tables including incident.
-   You can create the **Redirect SOW Email notification for Incident Management** \(**sow\_email\_notification\_redirect.incident**\) property and set it to `true` to enable the email redirection behavior specifically for the incident table. This property, if created and set, overrides the **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) base system property.

## Email notification redirection for Major Incident Management

In major incident email notifications, you can decide where the links to a major incident record are redirected. Instead of a major incident record automatically opening in the UI16 interface in Major Incident Management, the record can be opened in SOW.

The ITSM Notifications Redirection \(com.snc.itsm.notifications\_redirection\) plugin is installed and activated automatically to support this behavior. The major incident record link in an email notification opens in SOW only if the following conditions are met:

-   The **Redirect SOW Email notification** \(**sow\_email\_notification\_redirect**\) property is set to `true`. Setting this property to true enables the email redirection behavior for all tables including major incident.
-   The **Redirect SOW Email notification for Major Incident Management** \(**sn\_major\_inc\_mgmt.sow\_email\_notification\_redirect.mim**\) property is set to `true`.
-   You have the sn\_sow.sow\_user role.

**Parent Topic:**[View incident notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/t_ViewIncidentNotification.md)


---
title: Restrict access to certain major security incidents
description: Manage access to sensitive major security incidents by restricting view and modify permissions to authorized users and groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/restrict-access-major-security-incidents.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Update Major Security Incident details, Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Restrict access to certain major security incidents

Manage access to sensitive major security incidents by restricting view and modify permissions to authorized users and groups.

## Before you begin

Role required: sn\_msi.workspace\_manager

Users with the admin role can also view the major security incident regardless of the allowed members or groups list. The admin role includes the `sn_msi.restriction_access_admin` role, which bypasses the enforce restriction check. This behavior applies in both Workspace and classic UI.

## About this task

Use restrictions to control which users and groups can view or modify specific major security incidents. After enforcement, only authorized members, workspace managers, and users with the admin role can access the restricted incidents.

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Major Security Incidents**.

2.  Select the **Lists** view.

3.  Choose the required major security incident record.

4.  Select the **Details** tab.

5.  Scroll down and select the **Restriction** section.

6.  Select the **Enforce restriction** check box to enable the restriction of the major security incident.

    \[Omitted image "msim-restrict-access.png"\] Alt text: Limit access to major security incidents only to certain groups or users.

7.  In the **Allowed members** field, select the users who can view or modify the major security incident using the Search option.

8.  In the **Allowed groups** field, select the groups who can view or modify the major security incident using the Search option.

    **Note:** After the **Enforce restriction** check box is enabled for the major security incident, only the sn\_msi.workspace\_manager and allowed members or groups will have access to view or modify the major security incident.

9.  Select **Save**.


**Parent Topic:**[Update Major Security Incident details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/msim-details-tab.md)


---
title: Restrict access to certain major security incidents
description: Manage who can view or modify major security incidents that contain sensitive information. You can enforce major security incident restrictions to determine who has access to view or modify certain major security incident records and related lists and limit the read or write access only to certain users or groups.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Update Major Security Incident details, Use, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Restrict access to certain major security incidents

Manage who can view or modify major security incidents that contain sensitive information. You can enforce major security incident restrictions to determine who has access to view or modify certain major security incident records and related lists and limit the read or write access only to certain users or groups.

## Before you begin

Role required: sn\_msi.workspace\_manager

## About this task

Major security incident restrictions enable you to hide critical major security incidents from being accessed or modified by all users or groups in a particular organization. These restrictions enable you to provide a more granular way to control the major security incidents a user or group can view or modify. You can enforce a major security incident restriction by selecting the **Enforce restriction** check box and selecting the users or groups allowed to view or modify the particular major security incident.

After you enforce the restriction on major security incidents or related lists to certain users or groups, all the remaining users or groups in your organization won’t be able to view or modify these major security incidents or related lists.

## Procedure

1.  Navigate to **Workspaces** &gt; **Major Security Incident Management** &gt; **Major Security Incidents**.

2.  Select the **Lists** view.

3.  Choose the required major security incident record.

4.  Select the **Details** tab.

5.  Scroll down and select the **Restriction** section.

6.  Select the **Enforce restriction** check box to enable the restriction of the major security incident.

    ![Limit access to major security incidents only to certain groups or users.](../image/msim-restrict-access.png "Restrict access to major security incidents")

7.  In the Allowed members field, select the users who can view or modify the major security incident using the Search option.

8.  In the Allowed groups field, select the groups who can view or modify the major security incident using the Search option.

    **Note:** After the **Enforce restriction** check box is enabled for the major security incident, only the sn\_msi.workspace\_manager and allowed members or groups will have access to view or modify the major security incident.

9.  Select **Save**.


**Parent Topic:**[Update Major Security Incident details](../concept/msim-details-tab.md)


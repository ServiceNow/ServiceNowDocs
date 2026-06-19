---
title: Restrict access to security incidents
description: Manage the access of the security incidents that contains sensitive information. You can enforce security incident restrictions to determine who can access a certain incident and limit the access only to specific users or groups.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/restrict-access-security-incidents.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Restrict access to security incidents

Manage the access of the security incidents that contains sensitive information. You can enforce security incident restrictions to determine who can access a certain incident and limit the access only to specific users or groups.

## Before you begin

Role required: sn\_si.admin

## About this task

Security incident restrictions enable you to hide critical security incidents from being accessed by other users in a particular organization. These restrictions enable you to provide a more granular way to control the security incidents a user can access. You can enforce a security incident restriction by enabling the **Enforce restriction** check box, and then selecting the users or groups who are allowed to access the particular security incident.

After you enforce the restriction on specific security incidents and limit the access to certain users or groups, then all the other remaining users in your organization won’t be able to access these security incidents even if they search for a particular restricted security incident.

## Procedure

1.  Open a security incident that you want to restrict.

2.  If you are using classic UI, perform the following:

    1.  Click the **Restriction** tab.

    2.  Select the **Enforce restriction** check box to enable the restriction of the security incident.

        \[Omitted image "si-restriction.png"\] Alt text: Restrict access to security incidents

    3.  In the Allowed members field, click the \[Omitted image "lock-icon.png"\] Alt text: Lock icon icon to select the users who can access the security incident.

    4.  Select the \[Omitted image "add-me-icon.png"\] Alt text: Add me icon icon to add yourself as the allowed user.

    5.  Select the \[Omitted image "add-remove-users.png"\] Alt text: Add and Remove multiple users icon to add or remove users.

    6.  In the Allowed groups field, click the \[Omitted image "lock-icon.png"\] Alt text: Lock icon icon to select the groups who can access the security incident.

    7.  Select the \[Omitted image "add-remove-users.png"\] Alt text: Add and Remove multiple groups icon to add or remove groups.

        **Note:** After the **Enforce restriction** check box is enabled for the security incident, only the sn\_si.admin and allowed members or groups will have access to the security incident.

    8.  Click **Update**.

3.  If you are using SIR Workspace, perform the following:

    1.  From the security incident, click the **Details** tab.

    2.  Scroll down and click the **Restriction** section.

    3.  Select the **Enforce restriction** check box to enable the restriction of the security incident.

        \[Omitted image "si-restriction-worskpace.png"\] Alt text: Restrict access to security incidents on SIR Workspace

    4.  In the Allowed members field, select the users who can access the security incident using the Search option.

    5.  In the Allowed groups field, select the groups who can access the security incident using the Search option.

        **Note:** After the **Enforce restriction** check box is enabled for the security incident, only the sn\_si.admin and allowed members or groups will have access to the security incident.

    6.  Click **Save**.



---
title: Add unmatched affected user for security incidents
description: Add affected users that could not be matched to the existing system user records during data processing for preserving the context for the security analysts.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View affected items for a security incident, View information in a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add unmatched affected user for security incidents

Add affected users that could not be matched to the existing system user records during data processing for preserving the context for the security analysts.

## Before you begin

Role required: sn\_si.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Incident Response Workspace**.

2.  Open a security incident for which you want to add unmatched affected user.

3.  Select the **Related Records** tab.

4.  Select **Unmatched Affected Users** in the **Business Impact** list.

5.  On the Unmatched Affected Users page, select **New**.

6.  On the Create New Security Incident Unmatched User form, fill in fields.

    |Field|Description|
    |-----|-----------|
    |Security Incident|The security incident number. This value is auto-populated from the security incident number.|
    |User Information|Information of the affected user. For example, name, email. This value should be unique for each user.|

7.  Select **Save**.


## Result

The newly added unmatched affected user is added on the Unmatched Affected Users page.


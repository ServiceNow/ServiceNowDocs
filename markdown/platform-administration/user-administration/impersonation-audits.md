---
title: User impersonation auditing
description: User impersonation auditing creates a structured, dedicated audit trail for every impersonation session.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 1
keywords: [user impersonation, auditing, audit trail, security, administrator, session lifecycle, system logs, impersonation session, audit records, transaction logs]
audience: administrator
breadcrumb: [Impersonating users, Monitoring user activity, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# User impersonation auditing

User impersonation auditing creates a structured, dedicated audit trail for every impersonation session.

Impersonation activity is indistinguishable from regular user activity in a standard audit trail, you can't reliably attribute changes to the administrator who made them rather than the user they were impersonating. With the user impersonation auditing you can capture every impersonation session as a self-contained audit set, clearly separated from ordinary session data and accessible to administrators through system logs.

## Plugin and feature property

-   Plugin required for user impersonation auditing \(`com.glide.security.audit`\).
-   Property to control the feature user impersonation auditing \(`glide.audit.user.impersonation.enabled`\).

## Accessing impersonation audit records

Impersonation audit records are available to security administrators through **System Logs** &gt; **User Impersonation**. The list view displays a summary of all impersonation sessions recorded on the instance, including the identities of both parties and the session duration. Selecting any session record opens the detail view, which presents the complete audit set — the start entry, all actions in chronological order, and the closing entry — in a single place. This allows a security administrator to verify that the actions taken during a session were appropriate and within the expected scope of the impersonation.

## Audit record fields

Each entry in an impersonation audit set, whether a session-level record or an action-level entry, captures the following information.

|Field|Description|Example value|
|-----|-----------|-------------|
|Impersonated by|User who initiated the impersonation session.|`john.smith`|
|Impersonated to|User whose identity is being assumed.|`jane.doe`|
|Impersonation Start Time|Timestamp when the impersonation session began.|`2024-06-10 09:15:32 UTC`|
|Impersonation End Time|Timestamp when the session was terminated.|`2024-06-10 09:47:11 UTC`|

Select the **Impersonation Start Time** to know more about the impersonation activity. Following details are displayed:

-   Created
-   Type
-   Origin Application
-   Created by
-   Response time
-   Output length
-   SQL count
-   SQL time
-   Business rule count
-   ACL Time
-   URL

You can use the **Personailze List Columns** options to add more columns to the log.

**Note:** Impersonation audit records follow the same retention policy as transaction logs. The default retention period is `seven` days, but this is configurable by a system administrator. Any change to the transaction log retention setting applies equally to impersonation audit records.

**Parent Topic:**[Impersonating users](c_ImpersonateAUser.md)


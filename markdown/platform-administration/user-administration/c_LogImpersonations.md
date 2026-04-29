---
title: Impersonation logs
description: Impersonations are logged in the system log.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Impersonating users, Monitoring user activity, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Impersonation logs

Impersonations are logged in the system log.

Log impersonations for either interactive \(UI\) or non-interactive sessions.

## Impersonation logging for interactive sessions

Interactive sessions are performed through the user interface \(UI\). Enable or disable impersonation logging for interactive sessions using the **glide.sys.log\_impersonation** property.

If you enable impersonation logging for interactive sessions by setting **glide.sys.log\_impersonation** to **true**, all interactive sessions are recorded in the log.

|Property|Description|
|--------|-----------|
|**glide.sys.log\_impersonation**|Enables \(**true**\) or disables \(**false**\) impersonation logging for interactive sessions.|

## Impersonation logging for non-interactive sessions

Non-interactive sessions are performed by applications and scripts, not through the UI.

Impersonation logging of non-interactive sessions is turned off by default. If you enable impersonation logging by setting the **glide.sys.log\_impersonation.non\_interactive** property to **true**, impersonations of non-interactive sessions are recorded in the impersonate log.

Even with **glide.sys.log\_impersonation.non\_interactive** set to **true**, the system doesn’t log certain common impersonation tasks performed on behalf of the default users \(**system**, **soap.guest**, and **guest**\) because the application impersonates those default users to perform a variety of tasks.

Use the **glide.sys.log\_impersonation.non\_interactive.exclusion** property to exclude impersonations by other users in addition to the default users.

<table id="table_hjb_ntk_kbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.sys.log\_impersonation.non\_interactive**

</td><td>

Enables \(**true**\) or disables \(**false**\) impersonation logging for non-interactive sessions.

</td></tr><tr><td>

**glide.sys.log\_impersonation.non\_interactive.exclusion**

</td><td>

Excludes impersonation logging of non-interactive sessions for specified users.Enter user names as a comma-separated list. Default users \(**system**, **soap.guest**, and **guest**\) don’t need to be included in the list.

</td></tr></tbody>
</table>**Parent Topic:**[Impersonating users](c_ImpersonateAUser.md)


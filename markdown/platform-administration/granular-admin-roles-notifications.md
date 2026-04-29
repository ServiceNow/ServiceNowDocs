---
title: Granular admin roles for Notifications
description: Granular admin roles enable organizations to assign specific administrative permissions based on functional responsibilities, replacing broad admin access with targeted role assignments. Use the new admin roles to grant users administrative capability without using the admin role.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Granular admin roles for Notifications

Granular admin roles enable organizations to assign specific administrative permissions based on functional responsibilities, replacing broad admin access with targeted role assignments. Use the new admin roles to grant users administrative capability without using the admin role.

<table id="table_ybm_1vy_f3c"><thead><tr><th>

Role name

</th><th>

Functionality

</th><th>

Description

</th><th>

Plugin

</th></tr></thead><tbody><tr><td>

email\_bounce\_admin

</td><td>

Email Bounce

</td><td>

Provides access to configure email bounce related tables.

</td><td>

com.glide.email.bounce\_management

</td></tr><tr><td>

smime\_certificate\_admin

</td><td>

SMIME

</td><td>

-   To install a private key in the KMF module, the user needs the sn\_kmf.cryptographic\_manager role
-   To install a CA or Email certificate, the user requires the smime\_certificate\_admin role
-   To check SMIME logs, the user must have the email\_log\_viewer role

</td><td>

com.glide.email.smime

</td></tr><tr><td>

email\_log\_viewer

</td><td>

Email logs, SMIME logs

</td><td>

Provides access to view email logs and SMIME logs.

</td><td>

com.glide.mailbox

</td></tr><tr><td>

email\_digest\_admin

</td><td>

Email digest

</td><td>

Provides access to sys\_email\_digest\_part\_user and sys\_email\_digest\_part tables.

</td><td>

com.glide.email\_digest

</td></tr><tr><td>

notification\_classification\_admin

</td><td>

Notification classification

</td><td>

Provides access for adding add Notification classification to sys\_notification\_classification table.

</td><td>

com.glide.notification.classification

</td></tr><tr><td>

notification\_category\_admin

</td><td>

Notification category

</td><td>

Provides access for adding add Notification category to sys\_notification\_category table.

</td><td>

com.glide.notification.preference.service

</td></tr><tr><td>

push\_admin

</td><td>

Push credential

</td><td>

Provides access for push\_admin to sys\_push\_instance\_credential table.

</td><td>

com.glide.push\_proxy

</td></tr><tr><td>

portal\_notification\_pref\_admin

</td><td>

Widget preference

</td><td>

Provides access to sys\_recipient\_user\_mapping table.

</td><td>

com.glide.notification.unify.preference.service

</td></tr><tr><td>

notification\_admin

</td><td>

Notifications

</td><td>

Provides access to configure notifications through the sysevent\_email\_action table,with access to the sys\_email\_layout and sysevent\_email\_template tables. Additionally,they can set the digest interval.

 For Request Translation user needs to have localization\_requestor role.

</td><td>

com.glide.notification

</td></tr><tr><td>

email\_admin

</td><td>

Resend email, Reprocess Email

</td><td>

Provides access to reprocess inbound emails and resend outbound emails. Additionally, to view logs, they must have the email\_log\_viewer role.

</td><td>

com.glide.mailbox

</td></tr><tr><td>

oauth\_admin

</td><td>

Authorize Email Account Access, Test Connection

</td><td>

Provides access to authorize an email account and do test connection. To view logs, they must have the email\_log\_viewer role.

</td><td>

com.glide.mailbox

</td></tr></tbody>
</table>**Parent Topic:**[Reference](../concept/reference-email-admin.md)


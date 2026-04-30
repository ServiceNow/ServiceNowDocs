---
title: Email address internationalization
description: Email address internationalization allows international character support for email addresses for non-English characters when sending and receiving emails. Email addresses can have non American Standard Code for Information Interchange \(ASCII\) characters.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Email client, Notifications, Configure core features, Administer]
---

# Email address internationalization

Email address internationalization allows international character support for email addresses for non-English characters when sending and receiving emails. Email addresses can have non American Standard Code for Information Interchange \(ASCII\) characters.

Enable or disable International characters in an email by running a scheduled job.

The **glide.email\_address.rfc6530.enabled** system property can be set to true only if the configured email SMTP server for the instance supports SMTP UTF8 extension. This property by default enables sending and receiving of inbound emails to and from international email addresses including processing of the emails received from encoded international email addresses.

## Enable or disable email address internationalization

Enable email address internationalization by setting the **glide.email\_address.rfc6530.enabled** system property to `true`.

Disable email address internationalization by setting the **glide.email\_address.rfc6530.enabled** system property to `false`.

-   **[Customize email address internationalization](../task/customize-email-int.md)**  
Customize email address internationalization to turn off processing of inbound and outbound emails, disable support for inbound emails or to add email address format for decoding international email addresses.

**Parent Topic:**[Configure email client](configuring-email-client.md)


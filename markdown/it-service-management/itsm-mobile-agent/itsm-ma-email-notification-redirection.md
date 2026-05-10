---
title: ITSM Mobile email notification redirection via web
description: Redirect the users to the ITSM Mobile application from the mobile web browser to open and view the task records.
locale: en-US
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# ITSM Mobile email notification redirection via web

Redirect the users to the ITSM Mobile application from the mobile web browser to open and view the task records.

When you select the record link from the email notifications on the mobile, the link opens in the mobile web browser with a pop-up banner prompting you to view the record in the ITSM Mobile application which provides a faster and more intuitive way to access the records.

To enable this feature, set the **Enable universal links** \(**glide.sg.universal\_links.enabled**\) system property to `true`.

The feature is based on the universal linking of mobile. For more information, see [Universal linking for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/universal-links-mobile.md).

The email notification redirection is applicable to the following type of records:

-   Incident
-   Incident task
-   Catalog task
-   Change request
-   Change task


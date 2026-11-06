---
title: ITSM Mobile email notification redirection from the web
description: Email notification redirection opens task records from email notifications in the ITSM Mobile application instead of the mobile web browser.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/itsm-mobile-agent/itsm-ma-email-notification-redirection.html
release: australia
product: ITSM Mobile Agent
classification: itsm-mobile-agent
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring ITSM Mobile Agent, ITSM Mobile Agent, IT Service Management]
---

# ITSM Mobile email notification redirection from the web

Email notification redirection opens task records from email notifications in the ITSM Mobile application instead of the mobile web browser.

When you select the record link in an email notification on your mobile device, the link opens in the mobile web browser. A pop-up banner prompts you to view the record in the ITSM Mobile application.

To enable this feature, set the **Enable universal links** \(**glide.sg.universal\_links.enabled**\) system property to `true`.

The feature uses mobile universal links. For details about how universal links work, see [Universal linking for mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/universal-links-mobile.md).

The email notification redirection applies to the following types of records:

-   Incident
-   Incident task
-   Catalog task
-   Change request
-   Change task


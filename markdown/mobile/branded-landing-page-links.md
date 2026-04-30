---
title: Navigation links within a branded landing page
description: Learn about the different behavior of trusted or untrusted links on your branded landing page.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Branded landing page, Mobile instances, Configuring the Mobile Platform, Mobile Platform]
---

# Navigation links within a branded landing page

Learn about the different behavior of trusted or untrusted links on your branded landing page.

There are two types of links that you can use on a pre-login branded landing page, trusted and untrusted.

## Trusted links

Trusted links are ServiceNow supported links, which must contain one of the following:

-   A URL path ending with `*.servicenow.com`
-   A URL path ending with `*.service-now.com`
-   Domain and sub-domains of the branded landing page.

When using these path types, a dialog box does not display. These trusted links can be general hyperlinks to another web page within the trusted domains or mobile deep links. For more information, see [Deep linking for mobile](../concept/deep-link-mobile.md).

## Untrusted links

Users selecting an untrusted link within a ServiceNow mobile app opens a dialog box with the following options:

-   Accept: Informs the user that they're loading content from outside the mobile app and it might contain security risks.
-   Use External Browser: Opens the content in an external browser outside of the ServiceNow mobile app.
-   Cancel: Closes the pop-up and does not open the link.


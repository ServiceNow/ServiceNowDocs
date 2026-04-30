---
title: Enable expansion of universal linking to mobile browser \(MESP\) pages
description: Enable the expanded universal linking option to display the web banner on mobile browser pages when the user does not have the appropriate mobile app installed. By default this mobile universal linking option is not available in the base system.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Universal linking for mobile, Mobile URLs, Configuring the Mobile Platform, Mobile Platform]
---

# Enable expansion of universal linking to mobile browser \(MESP\) pages

Enable the expanded universal linking option to display the web banner on mobile browser pages when the user does not have the appropriate mobile app installed. By default this mobile universal linking option is not available in the base system.

## Before you begin

The mobile universal linking feature must be enabled, see [Enable mobile universal linking](universal-linking-enable.md).

Role required: admin

## Procedure

1.  In the web-based UI, enter `sys_properties.list` in the filter navigator, to open a list of system properties.

2.  In the **Name** field search for the term `*universal`.

3.  Click the property `glide.sg.universal_links.open_unsupported_links`.

4.  In the universal links system property table, set the **Value** field to `True`.

5.  Right-click in the header and select **Save**.

6.  Select the mobile app you want to redirect the user to, each time they tap the link in the banner.

    The default is the Mobile Agent.

    1.  Return to the system properties table.

    2.  Click the property `glide.sg.universal_links.unsupported_link_default_native_client`.

    3.  In the universal links unsupported links system property table, set the **Value** field to either `agent`, `requester`, or `onboarding`.

7.  Right-click in the header and select **Save**.


**Parent Topic:**[Universal linking for mobile](../concept/universal-links-mobile.md)


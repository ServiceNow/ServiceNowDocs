---
title: Mobile experience switcher
description: Enable users to switch between multiple mobile app experiences, also known as mobile app config, in the Settings page. The mobile experience switcher allows users to select multiple app experiences that match the users roles and permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/mobile-experience-switcher.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 1
breadcrumb: [Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile experience switcher

Enable users to switch between multiple mobile app experiences, also known as mobile app config, in the Settings page. The mobile experience switcher allows users to select multiple app experiences that match the users roles and permissions.

|Experience switcher unopened|Experience switcher with open sheet of options|
|----------------------------|----------------------------------------------|
|\[Omitted image "ex-switcher-collapse.png"\] Alt text: Experience switcher in an unopened state|\[Omitted image "ex-switcher-open.png"\] Alt text: Experience switcher in an opened state|

## Things to consider

Consider the following when configuring the experience switcher:

-   The Experiences option only displays when more than one mobile app config record is created and is active.
-   You can configure the label, order, and visibility of each experience in the switcher.
-   The switcher displays experiences based on user roles, permissions, and user criteria.
-   New users see the highest-priority experience \(the one with the lowest order value\) on first launch.
-   Existing users see the last experience they selected, even if a higher-priority experience was added since their previous session.

    **Note:** This behavior applies only when the switcher is enabled. When turned off, the highest-priority available experience is displayed

-   Your last-used experience persists at the device level, it doesn't reset when you log out.

-   **[Configure the mobile experience switcher](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/mobile-exp-switcher-config.md)**  
Learn how to configure the mobile experience switcher.

**Parent Topic:**[Considerations before implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/imp-considerations.md)


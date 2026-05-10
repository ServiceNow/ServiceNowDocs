---
title: Create regions for language selection in portals
description: Create regions to group languages in the language selector in portal headers.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create regions for language selection in portals

Create regions to group languages in the language selector in portal headers.

## Before you begin

Role required: admin

## About this task

In portal headers, the language selector displays the current language selection of the user and a menu of languages that the user can choose from. If languages are assigned to regions, languages display according to the configured region groups.

![A list of languages grouped by regions in the language selector of a portal.](../../localization/image/lang-selector-regions.png "Languages grouped by region in a portal header")

For more information about the language selector in portal headers, see [Enable a language selector in portal headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/configure-header-menu.md).

## Procedure

1.  Create regions.

    1.  Navigate to **System Localization** &gt; **Regions**.

    2.  Select **New**.

    3.  In the **Region** field, add a name for the region.

    4.  In the **Order** field, assign a numerical value in multiples of hundred for the region.

        The order controls where the regions appear in the language selector, with the lowest ordered region on the left and the highest ordered region on the right.

    5.  Select **Submit**.

    6.  Repeat these steps to create additional regions.

2.  Assign languages to regions.

    1.  Navigate to **System Localization** &gt; **Language Regions**.

    2.  Select **New**.

    3.  In the **Region** field, select a region from the list.

    4.  In the **Language** field, select a language to assign to the region from the list.

    5.  Select **Submit**.

    6.  Repeat these steps to assign additional languages to regions.



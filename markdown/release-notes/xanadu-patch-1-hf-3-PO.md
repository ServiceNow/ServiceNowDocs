---
title: Xanadu Patch 1 Hotfix 3
description: The Xanadu Patch 1 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-10-29"
reading_time_minutes: 1
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 1 Hotfix 3

The Xanadu Patch 1 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 10-23-2024\_0647

    Build tag: glide-xanadu-07-02-2024\_\_patch1-hotfix3-10-21-2024


**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

UI Field Administration

 PRB1795835

</td><td>

The campaign date picker opens in a lower position than usual

</td><td>

The campaign date picker, which is the calendar with a date and time selection field, is positioned offset and lower than its usual correct position.

</td><td>

1.  Install the latest Content Publishing and Content Experiences app.
2.  Navigate to the Content Experience Builder.
3.  Select the date pickers **Start Time** and **End Time**.

 Expected behavior: The date picker opens in the correct position.

 Actual behavior: The date picker is opens in a lower position than usual in the campaign builder.

</td></tr><tr><td>

Notification Preferences

 PRB1806559

</td><td>

A complete list of subscription notifications is not displayed in the drop down list

</td><td>

 

</td><td>

1.  Log into the instance.
2.  Navigate to the Preference page.
3.  Create a custom notification.

 Expected behavior: All notifications appear in the drop down list.

 Actual behavior: A complete list of notifications does not appear in the drop down list.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 1 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1703882)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu EA Hotfix 1](xanadu-patch-0-hf-1-PO.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


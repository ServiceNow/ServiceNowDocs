---
title: Configure the Language menu to be a single option
description: Configure the mobile property glide.sg.unify\_language\_settings to unify the Language option in the Settings screen. Use this setting to prevent the need for users to select multiple language options on their mobile device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/mobile/language-unification-config.html
release: australia
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
breadcrumb: [Mobile language menu unification, Localization, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the Language menu to be a single option

Configure the mobile property glide.sg.unify\_language\_settings to unify the Language option in the Settings screen. Use this setting to prevent the need for users to select multiple language options on their mobile device.

## Before you begin

Role required: mobile\_admin

## About this task

For new customers, from version 22.2 and later, the default option of the settings property is set to true. This means that users view the single language account option after selecting the Language menu option. The property can be added manually for existing customers users using client version 22.2 and earlier.

**Note:**

-   Language settings are handled differently depending on your Android OS version:
    -   Android version 12.0, users only see only one language option and can’t change the app language in the Android OS app settings.
    -   Android version 13.0, users can directly set their preferred language directly from the device settings.
-   You must be using one of the following ServiceNow patches:
    -   Brazil Patch 1 and later
    -   Australia Patch 7 and later
    -   Zurich Patch 13 and later

## Procedure

1.  Type  `sys_properties.list ` in the Application Navigator.

2.  Select  **New**, and then enter the following values:

<table id="table_lvg_gzk_tkc"><thead><tr><th>

Field

</th><th>

Inputs

</th></tr></thead><tbody><tr><td>

Name

</td><td>

glide.sg.unify\_language\_settings

</td></tr><tr><td>

Type

</td><td>

true \| false

</td></tr><tr><td>

Value

</td><td>

-   Enter  `true`  to display a unified language option, showing the Account language settings.
-   Enter  `false`  to display additional menu options after selecting Languages. The additional options for configuration are Account language and Preference language.

 For more information on Preferred language and Account language, see [Client-side localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/localization-client.md).

</td></tr></tbody>
</table>3.  Select **Submit**.


**Parent Topic:**[Mobile language menu unification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/mobile/language-menu-unification.md)


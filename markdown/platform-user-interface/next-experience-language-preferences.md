---
title: Configure Next Experience language and region preferences
description: Configure Next Experience language and region preferences to achieve the UI that works best for you.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/next-experience-language-preferences.html
release: brazil
topic_type: task
last_updated: "2026-09-14"
reading_time_minutes: 2
breadcrumb: [Preferences, Use, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure Next Experience language and region preferences

Configure Next Experience language and region preferences to achieve the UI that works best for you.

## Before you begin

Role required: admin

## About this task

From the Brazil release, the **Date format** and **Time format** fields have been relocated from the [User profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/user.md) to **Language &amp; Region** in Preferences. Also from the Brazil release, the values available in the drop-down **Combined date and time format** change to align with **Date format** and **Time format** selections.

## Procedure

1.  Navigate to **User Menu** &gt; **Preferences** &gt; **Language &amp; Region**.

2.  In the Preferences window, select the fields that you want to configure.

<table id="table_d5d_s2f_jqb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Language\[Omitted image "pol-pref-language.png"\] Alt text: Language. This drop-down field contains the example value English.

</td><td>

Sets the language used for your instance when you have access to more than one language. This preference displays only when another language plugin is installed. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateALanguage.md).

</td></tr><tr><td>

Country\[Omitted image "pol-pref-country.png"\] Alt text: Country. This drop-down field contains the example value United States.

</td><td>

Sets the country code used for your instance. When combined with a language selection, this preference sets the user locale, which affects default currency types and number formatting.

</td></tr><tr><td>

Date format\[Omitted image "next-experience-language-preferences-dateformat.png"\] Alt text: Date format field. This drop-down field contains the example value of 2026-08-19.

</td><td>

Available in Language &amp; Region from the Brazil release. Sets the format for displaying the date. Formats include:-   08/19/26
-   19/08/26
-   08-19-2026
-   08/19/2026
-   19-08-2026
-   19/08/2026
-   2026/08/19
-   2026.08.19
-   2026-08-19
If you select a non-default value in this field, the values available in **Combined date and time format** are also updated accordingly.

</td></tr><tr><td>

Time format\[Omitted image "next-experience-language-preferences-timeformat.png"\] Alt text: Time format field. This drop-down field contains the example value 16:30:45

</td><td>

Available in Language &amp; Region from the Brazil release. Sets the format for displaying the time, such as whether to separate segments by colon or period, or whether to use a 24-hour clock.Formats include:

-   16:30:45
-   16.30.45
-   04:30:45 PM
-   04.30.45 PM
-   16:30
-   16.30
-   04:30 PM
-   04.30 PM
If you select a non-default value in this field, the values available in **Combined date and time format** are also updated accordingly.

</td></tr><tr><td>

Combined date and time format\[Omitted image "next-experience-language-preferences-combination.png"\] Alt text: Combined date and time format field. This drop-down field is opened to show the three possible options.

</td><td>

Determines whether to display the amount of time that has passed since a recorded date and time. The options include: 1.  YYYY-MM-DD 09:00:01 5 min ago
2.  YYYY-MM-DD 09:00:01
3.  5 min ago
From the Brazil release, the available options in this field reflect the **Date format** and **Time format** values you previously selected. \(You may need to refresh this Language &amp; Region window after updating the **Date format** and **Time format** fields\). **Note:**

-   Some of the date formats will omit the current year.
-   The option **5 min ago** refers to a relative time format that displays how much time has passed since a specific event has occurred instead of showing the date and time.


</td></tr><tr><td>

Timezone\[Omitted image "pol-pref-timezone.png"\] Alt text: Timezone. This drop-down field contains the example value America/Los Angeles.

</td><td>

Determines the time zone or returns to the default time zone for the current session. At the next login, the time zone setting reverts to either the system default or the [user profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/user.md) setting for time zone.

</td></tr></tbody>
</table>
## What to do next

You can modify the time zone setting in the User profile by navigating to **User Menu** &gt; **Profile**. For information see [The User record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/user.md).

**Related topics**  


[System Localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/system-localization-landing.md)


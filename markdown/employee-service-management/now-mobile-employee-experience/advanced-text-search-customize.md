---
title: Customize AI Search results
description: Customize AI Search results to provide users with a tailored search experience.
locale: en-US
release: xanadu
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [AI Search in mobile, Configuring Now Mobile, Employee Service Management]
---

# Customize AI Search results

Customize AI Search results to provide users with a tailored search experience.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Search** &gt; **Search Configurations.**.

2.  Select the AI Search configuration to customize.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|This field is automatically set to the name of the search context configuration.|
    |Search Engine|This field is automatically set to the selected search engine. For this configuration, the value is AI Search.|
    |Search Profile|The search experience offered to users. This field is automatically set to **NowMobile Default Search Profile**.|
    |Search Results Limit|The number of standard results displayed per page not including Genius results. The default value is 10.|
    |Genius Results Limit|Number of Genius results listed at the top of the results. The default value is 1 and the maximum value is 3.|
    |Enable Typo Handling|Option for replacing misspelled search query terms with auto-correction terms derived from indexed content.|

4.  Modify the display name and the navigation tab filters for the People, Services, and Articles categories.

    These filters display under the search bar.

    1.  Select the **Navigation Tabs** tab.

    2.  Select the information icon ![Information icon.](../../tablet-mobile-ui/image/gac-info-icon.png) next to either **People**, **Articles**, or **Services** and select **Open Record** to open the record for that navigation tab.

    3.  On the form, fill in the fields.

        | | |
        |---|---|
        |Name|Name of the navigation tab category.|
        |Active|Option for determining whether the navigation tab filter displays.|
        |Order|The position in which the navigation tab displays. The lower the order value, the further left it displays.|
        |Label|Label to display for the navigation tab filter in the search application.|
        |Search Context Config|This field is automatically set to the name of the search context configuration.|

    4.  Repeat this process for each category you want to display.

5.  Customize the Autocomplete Suggestions tab, which relates to the display of relevant auto-complete suggestions as the user enters text.

    **Note:** The only options available for mobile applications are the section headers, **Recent searches** and **Popular searches**.

    1.  Select the Autocomplete Suggestions tab.

    2.  Select the information icon \(![Information icon.](../../tablet-mobile-ui/image/gac-info-icon.png)\) next to either **Recent searches** or **Popular searches** and select **Open Record** to open the record for that navigation tab.

    3.  On the form, fill in the fields.

<table id="table_ank_rhb_h4b"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Suggestion Type

</td><td>

Application-specific name for the auto-complete suggestion type. This field is automatically set.

</td></tr><tr><td>

Section Header

</td><td>

Label that displays auto-complete suggestions. Available options are:

 -   **Popular Searches** - Displays search queries commonly submitted by all users searching on this instance.
-   **Recent Searches** - Displays search queries drawn from the user's recent personal search history for the search application.


</td></tr><tr><td>

Order

</td><td>

Position in which the section headers appear. The higher the order value, the lower the section is in the list of suggestions.

</td></tr><tr><td>

Suggestion Limit

</td><td>

The maximum number of suggestions to show at any one time in this section. Default is 5.

</td></tr><tr><td>

Click-in Mode

</td><td>

Option for controlling the section header display.-   If selected, auto-complete suggestions display when the user first taps in the empty application search field.
-   If cleared, auto-complete suggestions display as the user types search query terms into the application search field.


</td></tr></tbody>
</table>    4.  Repeat this process for each section header you want to display.


## What to do next

After you have customized the display of your search results, select the AI Search results to be displayed in an applet launcher. See, [Add AI Search to a launcher screen](aisearch-add-applet-launcher.md).

Consider configuring a customized empty state display to inform users that their search has not produced any results. If you do not customize an empty state, a preconfigured default empty state is displayed. To customize an empty state, see [Configure an empty state for search results](https://www.servicenow.com/docs/access?context=empty-state-search-results&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

**Parent Topic:**[AI Search in mobile](../concept/text-search-advanced-now.md)


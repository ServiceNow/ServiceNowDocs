---
title: Next Experience theme for Now Mobile
description: Next Experience delivers a next generation, intuitive, personalized experience to drive productivity, improve engagement, and surface insights across the ServiceNow AI Platform.
locale: en-US
release: zurich
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring Employee Center for mobile, Now Mobile experience for Employee Center, Now Mobile app, Unified Employee Experience, Employee Service Management]
---

# Next Experience theme for Now Mobile

Next Experience delivers a next generation, intuitive, personalized experience to drive productivity, improve engagement, and surface insights across the ServiceNow AI Platform.

You can configure Next Experience on Now Mobile.

-   Provide a better accessible Next Experience on Now Mobile.
-   Offer consistent experiences across web and Now Mobile.
-   Provide a unified design experience across applications.

## Summary of enhancements

The following list provides a quick summary of the improvements as part of Next Experience.

-   Use the new layout, screens, and card designs for accessibility and intuitive experience.
-   Provide a consistent experience on web and mobile with the updated MESP portal theme that aligns with the next experience theme.
-   Set the value of glide.ui.polaris.experience to true to enable the new color variables. A fallback color hex code is used when the new experience is not enabled.
-   Use the color variables for UI rules, card templates, and icons.
-   Enhance the search and discovery of the content and people.
-   Improve accessibility with the new input form screens for functions instead of UI parameters.
-   Convert the Content section to the Record section \(sys\_sg\_item\_section\) to enable the display of each item as a card \(mobile view\)​.
-   Make the MESP portal record editable. Admin can now configure and apply the custom theme for MESP portal to provide a unified experience across native mobile and MESP.

## Enable AI Search upgrade considerations

From Utah, AI Search is the default search engine on Now Mobile.

For existing customers, when you upgrade to Utah, you continue to use your existing search engine for Now Mobile as it was before the upgrade.

-   Glide fix runs before the plugin upgrade where the current search engine is stored in a system property sn\_me\_search.search\_engine.
-   After plugin upgrade, another glide fix runs to set the value of search engine to sn\_me\_search.search\_engine property value, provided this value is not empty.

## MESP \(Webviews\) upgrade considerations

From Utah, Next Experience is the new theme on the MESP. For the existing customers, when you upgrade to Utah, the theme adoption works in the following manner:

-   When you have not branded the Now Mobile app and enable the Next Experience option, the new theme applies automatically on the MESP portal record.
-   When you have not branded the Now Mobile app and do not turn on the Next Experience option, the new theme is not applicable on the MESP portal record.
-   When you have branded the Now Mobile app; irrespective of the turning on or off the Next Experience option, the new theme is not applicable on the MESP portal record.

    |Upgrade scenario|Description|
    |----------------|-----------|
    |If you are upgrading from Tokyo to Vancouver, when the glide.ui.next\_experience.opt\_out and the glide.ui.polaris.experience are set to true|Update the MESP record manually to use the Next Experience theme.|
    |If you are upgrading from Tokyo to Vancouver, when the glide.ui.next\_experience.opt\_out and the glide.ui.polaris.experience are set to false|Update the MESP record manually to use the Next Experience theme.|


## Now Mobile native upgrade considerations

Here are the Now Mobile upgrade considerations for various Employee Center Applications. When you make changes at the mapping level, the latest changes are not available out-of-the-box.

-   Apps compatible with Utah: Now Mobile, Webviews for mobile, Search configurations for mobile, and Tasks for mobile.
-   Apps compatible with Utah, San Diego, and Tokyo family releases: Employee Center, Employee Center Core, Employee Profile, and Content Publishing.

<table id="simpletable_icc_dcp_tjb"><thead><tr><th>

Upgrade scenario

</th><th>

Description

</th></tr></thead><tbody><tr><td>

For apps compatible with Utah

</td><td>

When you upgrade to Utah, Next Experience is installed without any additional steps.

</td></tr><tr><td>

For apps compatible with Utah San Diego and Tokyo, with Next Experience changes installed and upgraded to Utah

</td><td>

For pre-Utah, Next Experience changes are not applied. -   Use the glide fix to automatically revert Next Experience changes.
-   After the instance is upgraded to Utah, you can manually run the uptake scripts for each app to uptake Next Experience changes.

</td></tr><tr><td>

For apps compatible with Utah San Diego and Tokyo, without Next Experience changes installed and upgraded to Utah

</td><td>

When you upgrade to Utah, Next Experience is installed without any additional steps.

</td></tr></tbody>
</table>Run the following fix scripts manually by setting the **runManually=true** to revert Next Experience changes for each application.

|Fix script|Application|
|----------|-----------|
|Mobile Revert Next Exp - Cont Pub|Content Publishing|
|Mobile Revert Next Exp - EC|Employee Center|
|Mobile Revert Next Exp - EC Core|Employee Center Core|
|Mobile Revert Next Exp - EP|Employee Profile|
|Mobile Revert Next Exp - Now Mobile|Now Mobile|
|Mobile Revert Next Exp - NowMobileSearch|Search Configurations for mobile|

Run the following fix scripts manually by setting the **runManually=true** to uptake Next Experience changes for each application.

|Fix script|Application|
|----------|-----------|
|Mobile Next Exp - Cont Pub|Content Publishing|
|Mobile Next Exp - EC|Employee Center|
|Mobile Next Exp - EC Core|Employee Center Core|
|Mobile Next Exp - EP|Employee Profile|

**Parent Topic:**[Configuring Employee Center for mobile](ec-mobile-configrations.md)


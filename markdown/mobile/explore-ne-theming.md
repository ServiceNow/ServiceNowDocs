---
title: Next Experience theming for mobile
description: Use Next Experience theming to give your mobile apps color scheme consistent with your instance web experience.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Next Experience theming for mobile

Use Next Experience theming to give your mobile apps color scheme consistent with your instance web experience.

## Use colors from your existing Next Experience theme

**Important:** Use Next Experience theming on Utah and later versions of ServiceNow® instances.

<table id="table_u4p_cl5_xvb"><tbody><tr><td>

Next Experience theming makes it easier than ever to present your unique company identity across all platforms.

 You can also use your Next Experience theme to inherit theme colors from your instance's existing web theme.

 For more information on Next Experience themes, see Exploring themes in Next Experience.

</td><td>

![Unified theme in mobile and web interfaces](../image/next-exp-themeing-1.png)

</td></tr></tbody>
</table>## Use color variables to create consistent custom components

<table id="table_ysz_n45_xvb"><tbody><tr><td>

As an admin, you can take advantage of color variables, which replace hard-coded colors. Use these variables to create consistent looking components. Color variables are supported in the following components.

-   UI Rules ​
-   Navigation sections ​
-   Map pins  Navigation​
-   Icons ​
-   View templates ​
-   Mobile View Buttons​
-   Input description field

</td><td>

![Unified theme in mobile and web interfaces](../image/next-exp-themeing-2.png)

</td></tr></tbody>
</table>## Upgrading to Next Experience theming

Whether your instance enables Next Experience theming depends on your existing configuration.

-   **New customers**

    For new customers in the Utah and later releases, Next Experience is active by default.

    -   For versions Utah to Yokohama, Polaris is the applied default theme.
    -   For versions Zurich and above, Coral is the applied default theme.
    These setting can be changed using a system property. For details see Considerations for activating Next Experience

-   **Existing customers with no theme customizations**

    Existing customers upgrading to Utah and later releases have Next Experience active by default unless they have opted-out of Next Experience in a previous release. If you've opted out, you can enable Next Experience theming manually. For details see Considerations for activating Next Experience.

    **Note:** Existing customers upgrading to Zurich who use Polaris as their default Next Experience theme will retain Polaris as their mobile theme unless a different theme is selected. For configuration instruction to change the theme, see [Configure Next Experience theming for mobile](config-ne-theming.md).

-   **Existing customers with custom themes**

    Existing customers upgrading to Utah and later releases have Next Experience disable by default after the upgrade. Your custom themes from the last release remain unchanged. You can manually enable Next Experience themes when you're ready to implement the new features. For details see Considerations for activating Next Experience.

-   **Existing customers using the Mobile Publishing application**

    Mobile Publishing customers who upgrade to Next Experience in Utah should take note of the following:

    -   Starting from Mobile Publishing version 3.2.0, Mobile Publishing integrates Next Experience colors and theming.
    -   The app splash screen displays the existing predefined colors and is not converted into Next Experience themed colors.
    -   Mobile Publishing configuration only affects visuals shown before the login page:

        -   App icon
        -   App name
        -   App splash screen
        Elements displayed after login are determined by the theme applied to your instance.



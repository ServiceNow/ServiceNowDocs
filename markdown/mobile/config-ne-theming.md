---
title: Configure Next Experience theming for mobile
description: Learn how to enable Next Experience theming, and create and apply themes for your mobile apps.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Next Experience theming, Configuring the Mobile Platform, Mobile Platform]
---

# Configure Next Experience theming for mobile

Learn how to enable Next Experience theming, and create and apply themes for your mobile apps.

## Enable Next Experience

**Important:** Use Next Experience theming on Utah and later versions of ServiceNow® instances.

To use Next Experience theming, you must have Next Experience enabled on your instance. For activation instructions and more information on Next Experience, see [Exploring themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-theming.md).

## Available themes for mobile apps

Themes are defined by records in the UX Themes \[sys\_ux\_theme\] table. Your instance includes three base system themes for use in the mobile UI, they are: Coral, Polaris, and mobile legacy.

![Three images side by side show the difference in look-and-feel of the different themes: legacy, Polaris, and Coral.](../image/theming-evolution-1.png "Comparison of the themes legacy, Polaris and Coral")

**Note:**

-   From Zurich versions and above Coral is the default theme with Next Experience enabled.
-   For Utah to Yokohama versions, Polaris is the default theme with Next Experience enabled. You can use either one of these options.
-   Existing customers upgrading to Zurich who use Polaris as their default Next Experience theme will retain Polaris as their mobile theme unless a different theme is selected.

-   **Coral**

    Coral is the default theme for instances with Next Experience enabled for versions Zurich and above. Customers upgrading to the Zurich theme will not automatically have their theme upgraded to Coral. Instead they will manually have to select the theme. For configuration instructions, see [Assign a Next Experience theme in the Mobile App Builder](../task/config-ne-theme-in-mab.md). The Coral theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience.

    A core UX Style \[sys\_ux\_style\] record called **Mobile Colors Default** is included with the **Coral** theme. This record cannot be modified, but, users can create a copy of this record or create a new theme record. Give your new or copied record a higher priority value to override the colors specified in the **Mobile Colors Default** record.

-   **Polaris**

    Polaris is the default theme for instances with Next Experience enabled for the versions Utah through Yokohama.

    **Note:** For customers upgrading to the Zurich theme, Polaris remains your Next Experience theme, unless you manually upgrade to Coral.

    A new core UX Style \[sys\_ux\_style\] record called **Mobile Colors Default** is included with the **Polaris** theme. This record cannot be modified, but, user can create a copy of this record or create a new theme record. Give your new or copied record a higher priority value to override the colors specified in the **Mobile Colors Default** record.

-   **Mobile Legacy**

    Mobile legacy is a fallback theme. Instances with upgraded to Utah or later that do not have Next Experience enabled use this theme.


Under the Polaris or Coral theme is a UX Style \[sys\_ux\_style\] record named **Mobile Colors Default**. This record defines the color variable names and the colors associated with them.

## Create themes and styles

Create Next Experience themes on the UX Theme \[sys\_ux\_theme\] table on your instance. By default, instances with Next Experience enabled use the **Coral** theme. \(From Utah through Yokohama versions, the default is the **Polaris** theme\). Instances without Next Experience enabled use the **Mobile Legacy** theme. These themes can't be modified, but you can copy either of them and change that copy.

Each UX Theme record is linked one or more UX Style \[sys\_ux\_style\] records that define the appearance of the UI when you apply a theme to your instance. As with theme records, the default style records aren't editable, but can be copied.

Learn more about Next Experience theme configuration at [Configuring Next Experience themes and preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/config-next-experience-themes-prefs.md).

**Important:** Mobile apps only use the color elements of a UX style. Elements such as font, shadow, opacity, and other non-color elements in a theme do not change the appearance of the mobile UI.

## Assign a theme to your mobile client

Set a theme for your mobile apps in the Mobile App Builder using the new **Mobile Theme** field.

-   **If the Mobile Theme field is empty**

    Your instance checks the state of whether Next Experience is enabled and determines which UX Theme \[sys\_ux\_theme\] record to use for the mobile app. By default:

    -   For the Zurich version, if Next Experience is enabled, the **Coral** theme is used.
    -   For Utah through Yokohama, if Next Experience is enabled, the **Polaris** theme is used.

        **Note:** You can use different mobile themes for each mobile app, when using Next Experience.

    -   If Next Experience is disabled, the **Mobile Legacy** theme is used.
-   **If the Client Theme field is not empty**

    Your mobile apps always use the theme specified in the field to theme the mobile app.


## Use color variables on your custom mobile components

Use color variables when designing your mobile components to provide a consistent user experience. The following components take advantage of color variables:

-   UI rules
-   Navigation sections
-   Map pins
-   Icons
-   View templates
-   Mobile view buttons
-   Input description fields

How to use color variables varies depending on the component you're building. For information on how to apply color variables on each of these components, see [Color theme considerations for mobile](color-guide-landing.md).


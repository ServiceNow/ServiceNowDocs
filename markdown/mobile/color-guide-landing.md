---
title: Color theme considerations for mobile
description: Learn how to use color in your mobile applications to improve user experience. Using the right colors for your environment can help guide your users through your app and quickly identify important information.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure theming, Next Experience theming, Configuring the Mobile Platform, Mobile Platform]
---

# Color theme considerations for mobile

Learn how to use color in your mobile applications to improve user experience. Using the right colors for your environment can help guide your users through your app and quickly identify important information.

## Using color

Keep consistency in your color decisions throughout the app. Associating specific tasks or workflows with colors helps users know when they’re in not in the right place. Consider using the same, or similar colors for related applets. For example, selecting blue for your incident-related applets and green for work order applets can help your users get to related tasks quickly.

Avoid using too many colors. Simple designs of two to three colors results in a cleaner, more accessible layout.

Color can be used to provide contrast for greater readability. In areas where text appears, ensure that your text and background have a high level of contrast to accommodate both low vision and colorblind users. Web Content Accessibility Guidelines \(WCAG\) 2.0 compliance requires a contrast ratio of at least 3:1. There are several tools online available to help with gauging color contrast.

High contrast, complementary colors can guide your user’s focus. Use these colors to highlight areas of your applications that need your user’s attention.

## General guidelines for color variables

Before you start using color variables, keep the following guidelines in mind.

-   **Next Experience must be enabled**

    Color variables only take effect when Next Experience is enabled. Otherwise, color variables are ignored

-   **Colors available for variables are on the UX Theme Properties table**

    Color variables use colors defined on the UX Theme Properties \[sys\_ux\_theme\_property\] table.

-   **Color variables are additive properties**

    Existing color properties \(using hard-coded colors\) continue to work if the new color variables aren't configured. However, color properties can't dynamically change the color of elements based on the theme​.

-   **Color variables override color properties**

    Color variables override the corresponding non-variable color properties if Next Experience is enabled and the color variable value is found.

    For example, given this UI rule action configuration:

    ```
    {“BackgroundColorVariable”: “--now-color-primary-0", “BackgroundColor”: “#3f2c11”}
    ```

    and a web color map with this configuration:

    ```
    {“--now-color-primary-0": “#22ff00”}
    ```

    The resolved background color for this UI rule action will be `#22ff00`.

-   **Color properties are used if a variable is not found or has no value**

    Color variable will not override if the variable is empty or the color variable value is not found. In these cases, the color property \(HEX\) is used.

    For example, given this configuration:

    ```
    {“BackgroundColorVariable”: “", “BackgroundColor”: “#3f2c11”}
    ```

    The color value is `#3f2c11`.

    Given this configuration:

    ```
    {“BackgroundColorVariable”: “--now-color-primary-0", “BackgroundColor”: “#3f2c11”}
    ```

    and a web color map with this configuration:

    ```
    {“--now-color-primary-1": “#1134a1”}
    ```

    The background color value is `#3f2c11`.

-   **Color variables use a naming convention**

    The naming convention of color variables is to add a `Variable` suffix to existing color properties.​

    For example, `BackgroundColorVariable` is used for `BackgroundColor`

-   **Configure both hex and color variables**

## Color variable support by component

Use these links to learn how to use color variables to change theming in your mobile components.

-   [Color variable support for UI rules](../reference/color-var-ui-rule.md)
-   [Color variable support for icon UI sections](../reference/color-var-ui-section.md)
-   [Color variable support for map icons](../reference/color-var-map-pin.md)
-   [Color variable support for icons](../reference/color-var-mobile-icons.md)
-   [Color variable support for card view templates](../reference/color-var-mobile-template.md)
-   [Color variable support for card view buttons](../reference/color-var-cardview-button.md)
-   [Color variable support for input descriptions](../reference/color-var-input-description.md)


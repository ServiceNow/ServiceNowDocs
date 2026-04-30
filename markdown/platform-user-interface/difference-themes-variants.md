---
title: Core styles, colors, variants, and alternate color palettes
description: You can tailor the look and feel of the Next Experience UI for different users by configuring the core styles, variants, and alternate color palettes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage or edit a theme with Theme Builder, Configuring Next Experience with Theme Builder, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Core styles, colors, variants, and alternate color palettes

You can tailor the look and feel of the Next Experience UI for different users by configuring the core styles, variants, and alternate color palettes.

## Core styles in Theme Builder

A core style is the base version of a style. Core styles include color, shape and form, typography, and imagery.

## Colors in Theme Builder

When editing components, use the color picker to change the background color of the canvas to view how the component colors will render on different backgrounds.

**Note:** Updating the canvas color doesn't apply to the instance. Only hooks specific to components are applied on the instance if you publish an edited theme to the instance.

When editing theme colors, you can view the contrast ratio in the color picker. The value updates when you change the color from the palette or My colors view.

## Variants/Alternate color palettes in Theme Builder

Both variants and alternate color palettes are types of UX style records categorized as Variant.

A variant is an alternate version of an existing theme, usually designed for accessibility, that your users can select in preferences. An example of a variant is the Dark version of the default Polaris theme that is shipped with Next Experience. The Dark variant can be used to enhance accessibility for visually impaired users by replacing light backgrounds with darker ones and contrasting the text colors accordingly.

An alternate color palette is a modification that you can make to a theme's colors and is designed for cosmetic purposes. You can define this palette in the Theme Builder Manager page for any theme, except for the default Polaris theme. When you use an existing theme to create an alternate color palette, the alternate color palette is grouped with that primary theme, and initially shares its logo, color, typography, and shape styles. At first, the only difference from the primary theme is that you assign it a unique name.

Next, you define the primary color for the alternate color palette. This color is used to identify the navigation bar, menus, and other common components. Likewise, define a secondary color, if needed. If your interface doesn't require a secondary color, the primary color is used. Lastly, you define a neutral color to help define divider lines and containers. There are two base palettes available, light and dark.

**Note:** Secondary and neutral colors cannot be edited in the dark alternate color palette.

When the palette is created using the colors you selected, you have the option of renaming it. You can also [preview all the UI assets available on the ServiceNow AI Platform to visualize how they are rendered when you apply them to your instance](../task/tb-preview-components.md).

**Note:** Dark variants don’t apply to the Core UI, previously referred to as UI16. The Core UI is the interface you use if Next Experience is inactive. However, dark variants extend to most aspects of the Next Experience.

**Parent Topic:**[Manage or edit a theme with Theme Builder](../task/tb-edit-theme.md)


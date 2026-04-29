---
title: Working with theme-able empty state images
description: Add theme-able empty state images to customize empty states and improve the user experience. Empty states include guidance or actions for users to add or create content.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Working with theme-able empty state images

Add theme-able empty state images to customize empty states and improve the user experience. Empty states include guidance or actions for users to add or create content.

When a component or a part of your Next Experience web page doesn’t contain data, an empty state image appears. Empty state images are theme-able, and adapt to the theme colors of your instance.

![No data available empty state image.](../image/empty-state-no-data-available.png "Empty state image")

There are 12 empty state image types available, each including a small, medium, and large version. When creating a theme using Theme Builder a UX Styles Imagery record is created however, the record is empty. In this case, your theme defaults to using a base system empty state theme-able images. If you choose to override these images, see [Customize theme-able empty state images for your theme](../task/customize-themeable-empty-state-images.md).

You can insert an empty state image into your custom experience by using the Illustration component in UI Builder. The Illustration component displays all available empty state images. For more information on the Illustration component, see [Horizon Design System Empty State](https://horizon.servicenow.com/components/now-template-message-empty-state).

You can also add custom images using the Custom Illustration component in UI Builder.

## Theme-able empty state image with theme hooks

The following images represent the No Search Results empty state image along with the theme hooks required for each variation.

![No Search Results empty state image, accent solid variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-accent-solid.png "No Search Results (accent solid)")

The theme hook required for this variation is `$now-color_interactive-1`.

![No Search Results empty state image, accent outline variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-accent-outline.png "No Search Results (accent outline)")

The theme hook required for this variation is `$now-color_interactive-3`.

![No Search Results empty state image, subtle outlines variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-subtle-outlines.png "No Search Results (subtle outlines)")

The theme hook required for this variation is `$now-color_border-secondary`.

![No Search Results empty state image, subject dark detail variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-dark-detail.png "No Search Results (subject dark detail)")

The theme hook required for this variation is `$now-color_border-tertiary`.

![No Search Results empty state image, subject light detail variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-light-detail.png "No Search Results (subject light detail)")

The theme hook required for this variation is `$now-color_background-secondary`.

![No Search Results empty state image, subject fill variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-subject-fill.png "No Search Results (subject fill)")

The theme hook required for this variation is `$now-color_background-primary`.

![No Search Results empty state image, subject outline variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-subject-outline.png "No Search Results (subject outline)")

The theme hook required for this variation is `$now-color_border-secondary`.

![No Search Results empty state image, subject shadows variation. For the text description, refer to the theme hook information that follows.](../image/tb-no-search-results-subject-shadows.png "No Search Results (subject shadows)")

The theme hook required for this variation is `$now-color_border-secondary`.

## Empty state light mode tokens

![Main object empty state image. For the text description, refer to the theme hook information that follows.](../image/tb-empty-state-main-object.png "Main Object empty state image")

The theme hooks used to override the main object empty state image.

-   now-illustration--empty-state--main-object--outline
-   now-illustration--empty-state--main-object--fill

![Primary object empty state image. For the text description, refer to the theme hook information that follows.](../image/tb-empty-state-primary-object.png "Primary object empty state image")

The theme hooks used to override the primary object empty state image.

-   now-illustration--empty-state--primary-object--outline
-   now-illustration--empty-state--primary-object--primary-fill
-   now-illustration--empty-state--primary-object--tertiary-fill
-   now-illustration--empty-state--primary-object--main-detail
-   now-illustration--empty-state--primary-object--detail
-   now-illustration--empty-state--primary-object--shadow

![Tertiary object empty state image. For the text description, refer to the theme hook information that follows.](../image/tb-empty-state-tertiary-object.png "Tertiary object empty state image")

The theme hooks used to override the tertiary object empty state image.

-   now-illustration--empty-state--tertiary-object--outline
-   now-illustration--empty-state--tertiary-object--primary-fill
-   now-illustration--empty-state--tertiary-object--tertiary-fill
-   now-illustration--empty-state--tertiary-object--main-detail
-   now-illustration--empty-state--tertiary-object--detail
-   now-illustration--empty-state--tertiary-object--shadow

![Background empty state image. For the text description, refer to the theme hook information that follows.](../image/tb-empty-state-background.png "Background empty state image")

The theme hooks used to override the background empty state image.

-   now-illustration--empty-state--background--lines
-   now-illustration--empty-state--background--tertiary-lines
-   now-illustration--empty-state--background--object-outline
-   now-illustration--empty-state--background--object-detail
-   now-illustration--empty-state--background--object-shadow
-   now-illustration--empty-state--background--object-fill

## Empty state light mode fallbacks

<table id="table_in3_rf2_rcc"><thead><tr><th>

Object

</th><th>

Style declaration

</th></tr></thead><tbody><tr><td rowspan="2">

Main object

</td><td>

```
  .main-object--outline {   fill:rgb(var(--empty-state--main-object--outline),
      var(--main-object--outline), var(--now-color--interactive-3), 51,53,123); }
```

</td></tr><tr><td>

```
  .main-object--fill {   fill:rgb(var(--empty-state--main-object--fill),
      var(--main-object--fill), var(--now-color--interactive-1), 144,146,213); }
```

</td></tr><tr><td rowspan="6">

Primary object

</td><td>

```
  .primary-object--outline {   fill:rgb(var(--empty-state--primary-object--outline),
      var(--primary-object--outline), var(--now-color--border--secondary),
    176,181,191); }
```

</td></tr><tr><td>

```
  .primary-object--primary-fill { 
      fill:rgb(var(--empty-state--primary-object--primary-fill),
      var(--primary-object--primary-fill), var(--now-color--background--primary),
      255,255,255); }
```

</td></tr><tr><td>

```
  .primary-object--tertiary-fill { 
      fill:rgb(var(--empty-state--primary-object--tertiary-fill),
      var(--primary-object--tertiary-fill), var(--now-color--background--secondary),
      246,246,248); }
```

</td></tr><tr><td>

```
  .primary-object--main-detail { 
      fill:rgb(var(--empty-state--primary-object--main-detail), var(--primary-object--main-detail),
      var(--now-color--border--secondary), 176,181,191); }
```

</td></tr><tr><td>

```
  .primary-object--detail {   fill:rgb(var(--empty-state--primary-object--detail ),
      var(--primary-object--detail ), var(--now-color--border--tertiary),
    211,214,220); }
```

</td></tr><tr><td>

```
  .primary-object--shadow {   fill:rgb(var(--empty-state--primary-object--shadow),
      var(--primary-object--shadow), var(--now-color--background--tertiary),
    228,230,234); }
```

</td></tr><tr><td rowspan="6">

Tertiary object

</td><td>

```
  .tertiary-object--outline {   fill:rgb(var(--empty-state--tertiary-object--outline),
      var(--tertiary-object--outline), var(--now-color--border--secondary), 176,181,191); }
      
```

</td></tr><tr><td>

```
  .tertiary-object--primary-fill { 
      fill:rgb(var(--empty-state--tertiary-object--primary-fill),
      var(--tertiary-object--primary-fill), var(--now-color--background--primary),
      255,255,255); }
```

</td></tr><tr><td>

```
  .tertiary-object--tertiary-fill { 
      fill:rgb(var(--empty-state--tertiary-object--tertiary-fill),
      var(--tertiary-object--tertiary-fill), var(--now-color--background--secondary),
      246,246,248); }
```

</td></tr><tr><td>

```
  .tertiary-object--main-detail { 
      fill:rgb(var(--empty-state--tertiary-object--main-detail),
      var(--tertiary-object--main-detail), var(--now-color--border--secondary),
      176,181,191); }
```

</td></tr><tr><td>

```
  .tertiary-object--detail {   fill:rgb(var(--empty-state--primary-object--detail ),
      var(--primary-object--detail ), var(--now-color--border--tertiary),
    211,214,220); }
```

</td></tr><tr><td>

```
  .tertiary-object--shadow {   fill:rgb(var(--empty-state--tertiary-object--shadow),
      var(--tertiary-object--shadow), var(--now-color--background--tertiary),
    228,230,234); }
```

</td></tr><tr><td rowspan="6">

Background object

</td><td>

```
  .background--lines {   fill:rgb(var(--empty-state--background--lines),
      var(--background--lines), var(--now-color--border--tertiary), 211,214,220); }
```

</td></tr><tr><td>

```
  .background--tertiary-lines { 
      fill:rgb(var(--empty-state--background--tertiary-lines), var(--background--tertiary-lines),
      var(--now-color--border--tertiary), 211,214,220); }
```

</td></tr><tr><td>

```
  .background--object-outline { 
      fill:rgb(var(--empty-state--background--object-outline), var(--background--object-outline),
      var(--now-color--border--tertiary), 211,214,220); }
```

</td></tr><tr><td>

```
  .background--object-detail {   fill:rgb(var(--empty-state--background--object-detail),
      var(--background--object-detail), var(--now-color--border--tertiary),
    211,214,220); }
```

</td></tr><tr><td>

```
  .background--object-shadow {   fill:rgb(var(--empty-state--background--object-shadow),
      var(--background--object-shadow), var(--now-color--background--tertiary),
      228,230,234); }
```

</td></tr><tr><td>

```
  .background--object-fill {   fill:rgb(var(--empty-state--background--object-fill),
      var(--background--object-fill), var(--now-color--background--primary),
    255,255,255); }
```

</td></tr></tbody>
</table>-   **[Customize theme-able empty state images for your theme](../task/customize-themeable-empty-state-images.md)**  
Customize default theme-able empty state images for your Next Experience and Theme Builder themes using the theme's Imagery record.

**Parent Topic:**[Working with themes in Next Experience](next-experience-theming.md)


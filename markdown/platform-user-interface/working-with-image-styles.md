---
title: Working with Image styles
description: Image styles enable you to experiment with different color schemes for illustrations and replace default illustrations with your own custom images. The Image styles feature provides flexibility in customizing the visual elements of your theme.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-03-12"
reading_time_minutes: 2
keywords: [theme builder, image, image styles]
breadcrumb: [Manage or edit a theme with Theme Builder, Configuring Next Experience with Theme Builder, Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Working with Image styles

Image styles enable you to experiment with different color schemes for illustrations and replace default illustrations with your own custom images. The Image styles feature provides flexibility in customizing the visual elements of your theme.

## Empty state illustrations

When a component or a part of your Next Experience web page doesn’t contain data, an empty state illustration appears. Empty state illustrations are theme-able, and adapt to the theme colors of your instance.

**Important:** Empty state illustrations apply to Workspaces and are not supported in the Core UI.

![No data available empty state illustration.](../image/empty-state-no-data-available.png "Empty state illustration")

The Image styles feature offers the following types of empty state illustration types, each including a small, medium, and large version:

-   Add attachment
-   Add data
-   Completed tasks
-   Completed tasks
-   Error
-   First time user
-   Interrupted
-   No activities
-   No data
-   Completed tasks
-   No permission
-   Completed tasks
-   No search results
-   Completed tasks
-   Offline
-   Unconfigured

## Custom images

Upload your custom images to Theme Builder to replace the default empty state illustrations.

To override the default empty state illustrations with custom images, upload each image size individually. You can choose to override just one size or all three sizes of an empty state type. The size and format limitations for each of the three file sizes are as follows:

|Field|Description|
|-----|-----------|
|Dimensions limit|w56 x h56 px|
|Format|SVG|
|File size limit|2 MB|

|Field|Description|
|-----|-----------|
|Dimensions limit|w216 x h168 px|
|Format|SVG|
|File size limit|2 MB|

|Field|Description|
|-----|-----------|
|Dimensions limit|w350 x h318 px|
|Format|SVG|
|File size limit|2 MB|

Empty state illustrations are dependent on two design tokens that handle their color:

-   --empty-state--main-object--fill
-   --empty-state--main-object—outline

Custom images don't automatically reflect your theme colors. To make your image theme-able, add these tokens to your code using your preferred text editor before uploading the custom SVG to Theme Builder. After adding these tokens to your image code, the images will adopt your theme colors and enable you to edit the colors when uploaded to Theme Builder.

The following example shows the design tokens applied.

```
<style>
    .main-object--outline {
        fill:rgb(var(--empty-state--main-object--outline, var(--main-object--outline, var(--now-color--interactive-3, 51,53,123))));
    }
    .main-object--fill {
        fill:rgb(var(--empty-state--main-object--fill, var(--main-object--fill, var(--now-color--interactive-1, 144,146,213))));
    }
  </style>

```

-   **[Customize the colors for empty state illustrations and custom images](../task/customize-colors-empty-state.md)**  
Customize and control the colors automatically applied to empty state illustrations and your custom images to keep your visual experience engaging while maintaining brand recognition.
-   **[Override empty state illustrations with custom images](../task/override-empty-state-illustrations.md)**  
Modify or override the default empty state illustrations with your own custom images to ensure that visual elements reflect your company's branding.

**Parent Topic:**[Manage or edit a theme with Theme Builder](../task/tb-edit-theme.md)


---
title: Configure the details for the appearance of cards for a mobile campaign
description: Configure item views to provide the details that define the appearance of cards within a mobile campaign to enhance display options and make your campaign more effective.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Displaying campaigns, Configuring the Mobile Platform, Mobile Platform]
---

# Configure the details for the appearance of cards for a mobile campaign

Configure item views to provide the details that define the appearance of cards within a mobile campaign to enhance display options and make your campaign more effective.

When creating item views for cards for a mobile campaign, you need to construct required JSON code to define the appearance of the cards. You then provide this code in the **Item view JSON** field of the Item view form, as described in [Create appearance templates for cards for a mobile campaign](../task/mobile-campaign-card-type.md)

**Note:** If any of the configurable values are empty or the line of code is removed, the default value is used.

## Item view JSON for text cards

For a text card, copy this sample JSON code and paste it in the **Item view JSON** field within an item view form.

```
{
  "Type": "ViewGroup",
  "Distribution": "Equal",
  "Orientation": "Vertical",
  "Alignment": "Center",
  "Margin": {
    "Left": 0,
    "Right": 0,
    "Top": 0,
    "Bottom": 0
  },
  "Children": [
    {
      "Type": "Text",
      "CellId": "title",
      "TextAlignment": "center",
      "Margin": {
        "Left": 16,
        "Right": 16
      },
      "MaxLines": 3,
      "Font": {
        "Weight": "bold",
        "Size": 36,
        "MinSize": 24
      },
    }
  ],
}
```

The parameters in the sample JSON code are as follows:

-   The **Type** parameter value is not configurable.
-   The **CellId** parameter value in the sample code is based on the value in the default base system version of the Employee Center table \[sn\_cd\_content\_mobile\]. If the value in that table has changed, add the changed value in the sample JSON code.

    **Note:** To access the table to check the values, enter `sn_cd_content_mobile.list` in the navigation filter of your application navigator.

-   The other parameter values in this sample code for text cards are standard setup values that provide a balanced appearance for the cards. You can customize these values.

## Item view JSON for video cards

For a video card, copy this sample JSON code and paste it in the **Item view JSON** field within the item view form.

```
{
  "Type": "Media-Video",
  "CellId": "video_link.url",
  "TitleCellId": "title",
  "SubtitleCellId": "text"
}
```

The parameters in the sample JSON code are as follows:

-   The **Type** parameter value is not configurable.
-   The **CellId**, **TitleCellId**, and **SubtitleCellID** parameter values in the sample code are based on the values from the default base system version of the Employee Center table \[sn\_cd\_content\_mobile\]. If any of the values in that table have changed, add the changed value in the sample JSON code.

    **Note:** To access the table to check the values, enter `sn_cd_content_mobile.list` in the navigation filter of your application navigator.


## Item view JSON code for image cards

For an image card, copy this sample JSON code and set any values that differ from the default values. If you want to use the default values, you can delete that line of code. Once you have set your desired values, paste the JSON code in the **Item view JSON** field within the item view form.

```
{
  "Type": "Media-Image",
  "CellId": "image",
  "TitleCellId": "title",
  "SubtitleCellId": "text",
  "Parallax": <true|false>,
  "DisplayType": "<over|under>",
  "DisplayTheme": "<light|dark>",
  "FocusOnFaces": <true|false>
}
```

The standard parameters in the sample JSON code are as follows:

-   The **Type** parameter value is not configurable.
-   The **CellId**, **TitleCellId**, and **SubtitleCellID** parameter values in the sample code are based on the values from the default base system version of the Employee Center table \[sn\_cd\_content\_mobile\]. If any of the values in that table have changed, add the changed value in the sample JSON code.

    **Note:** To access the table to check the values, enter `sn_cd_content_mobile.list` in the navigation filter of your application navigator.


The custom parameters for the item view for image cards are as follows:

-   **Parallax**

    Determines whether to create an illusion of depth and perspective on the image.

    -   `true` \(the default\): The text at the bottom of the card moves a slower speed than the background image, making the two objects appear as though they are on a different three-dimensional plane.
    -   `false`: The text at the bottom of the card and the image move at the same speed.
-   **DisplayType**

    Determines whether text is displayed under the image \(`under`\) or as an overlay on the image \(`over`\). The text includes the title and the subtitle. For a smooth visual experience, use the same format for all the card types. The default value is **over**.

    |Text displayed under image|Text displayed as overlay|
    |--------------------------|-------------------------|
    |![Text displayed under the image for display type configuration.](../image/campaigns-display-type-under.png)|![Text displayed as overlay within image for display type configuration.](../image/campaigns-display-type-over.png)|

-   **DisplayTheme**

    Determines the color of the text overlay. This option is available only if the display type is `over`. Use `light` for text that is to be displayed over a dark background. The default value is **light**.

    |DisplayTheme set to light|DisplayTheme set to dark|
    |-------------------------|------------------------|
    |![Text displayed in a light color for a display theme configuration.](../image/campaigns-display-theme-light.png)|![Text displayed in a dark color for display theme configuration.](../image/campaigns-display-theme-dark.png)|

-   **FocusOnFaces**

    When set to `true` \(the default\), images on an image card are cropped to where the faces are captured in the frame.



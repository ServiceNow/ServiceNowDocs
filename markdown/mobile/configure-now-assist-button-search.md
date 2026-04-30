---
title: Configure Now Assist button in search
description: Add a conversational chat button to standard catalog search results in mobile. The chat button redirects users to a new Virtual Agent conversation for eligible catalog items.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist, Now Assist for Mobile, Mobile Platform]
---

# Configure Now Assist button in search

Add a conversational chat button to standard catalog search results in mobile. The chat button redirects users to a new Virtual Agent conversation for eligible catalog items.

## Before you begin

Role required: admin

Verify that Now Assist in AI Search and Now Assist Self Service Enhanced Chat are enabled for the catalog items you want to display the chat button on. See [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) and [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US) for more information.

## Procedure

1.  Navigate to the Template 05 card template record at **sys\_sg\_view\_template.do?sys\_id=822e2f530f202010e70a4abec4767eee**.

2.  Open the Template JSON field for editing.

3.  In the Children array of the root cell, add a new button object with the following mandatory fields:

    |Field|Value|
    |-----|-----|
    |Type|`"Button"`|
    |Id|`"menu_01"`|
    |CellId|`"menu_01"`|
    |ContextMenu|`{"Presentation": "SearchMenu"}`|

    Here is an example of a JSON template with the mandatory fields added:

    ```
    {
      "Type": "ViewGroup",
      "Margin": {
        "Top": 12,
        "Bottom": 12,
        "Right": 12,
        "Left": 12
      },
      "Orientation": "Horizontal",
      "Alignment": "Center",
      "Distribution": "Auto",
      "Id": "root",
      "CellId": "root",
      "Children": [
        {
          "Type": "ViewGroup",
          "Id": "container_02",
          "Orientation": "Horizontal",
          "Alignment": "Center",
          "Distribution": "Auto",
          "CellId": "container_02",
          "Children": [
            {
              "Type": "Image",
              "Id": "image_01",
              "Scaling": "Fill",
              "Height": 44,
              "Width": 44,
              "CellId": "image_01",
              "Margin": {
                "Right": 16
              }
            },
            {
              "Type": "ViewGroup",
              "Id": "container_03",
              "Margin": {},
              "Orientation": "Vertical",
              "Alignment": "Left",
              "Distribution": "Equal",
              "CellId": "container_03",
              "Children": [
                {
                  "Type": "Text",
                  "TextColor": "#151920",
                  "TextColorVariable": "--now-color_text--primary",
                  "MaxLines": 2,
                  "CellId": "text_01",
                  "Id": "text_01",
                  "Margin": {},
                  "TextAlignment": "Left"
                },
                {
                  "Type": "Text",
                  "TextColor": "#2C323F",
                  "TextColorVariable": "--now-color_text--secondary",
                  "MaxLines": 1,
                  "Margin": {
                    "Top": 8
                  },
                  "CellId": "text_02",
                  "Id": "text_02",
                  "TextAlignment": "Left"
                }
              ]
            }
          ]
        },
        {
          "Type": "Button",
          "TextAlignment": "Center",
          "Id": "menu_01",
          "CellId": "menu_01",
          "ContextMenu": {
            "Presentation": "SearchMenu"
          },
          "TextColorVariable": "--now-color--primary-1",
          "BorderColorVariable": "--now-color--primary-1",
          "BorderWidth": 0,
          "Height": 24,
          "Width": 24,
          "Margin": {}
        }
      ]
    }
    
    ```

4.  Select **Save**.

5.  Navigate to the card template elements list \(**sys\_sg\_template\_slot.list**\) and select **New** to create a new record.

6.  Complete the following fields in the new card template element:

    |Field|Value|
    |-----|-----|
    |Name|`menu_01`|
    |Type|`Menu`|
    |Card template|Template 05|

7.  Select **Save**.

8.  Create three card template element attributes and associate them with the menu\_01 card template element, using the following:

    |Attribute|Type|Description|Value|
    |---------|----|-----------|-----|
    |Attribute 1|`AdditionalActionType`|`menu_01_type`|`Conversation`|
    |Attribute 2|`Icon`|`menu_01_icon`|`dbc96e63ff523210c63effffffffff8f`|
    |Attribute 3|`TextColorVariable`|`menu_01_TextColorVariable`|`--now-color--primary-1`|


**Parent Topic:**[Configuring Now Assist for Mobile](configuring-now-assist-mobile.md)


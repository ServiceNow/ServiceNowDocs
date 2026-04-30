---
title: Adding voiceover text for buttons defined as icon type within cards
description: Screen reader support provides voiceover text for elements on the screen. However, elements like buttons that are defined as icon type may require additional configuration. Alternative text is added to these elements enabling the screen reader to read the content of the button within cards.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Screen reader support, Configuring the Mobile Platform, Mobile Platform]
---

# Adding voiceover text for buttons defined as icon type within cards

Screen reader support provides voiceover text for elements on the screen. However, elements like buttons that are defined as icon type may require additional configuration. Alternative text is added to these elements enabling the screen reader to read the content of the button within cards.

## Before you begin

Role required: admin

## About this task

You can define alternative text for buttons defined as icon types within both cards and card templates. This topic covers the configuration for cards. For more information about creating buttons defined as icon type, see [Configure an icon UI section](sg-ui-section-config-navig.md).

## Procedure

1.  Navigate to **All**.

2.  In the filter navigator, enter `sys_sg_view_config.list` to open the Cards page.

3.  Select the card that contains a button defined as an icon type.

4.  In the Card page of the selected card, select the **Card elements** tab in the **Related Links** area of the screen.

5.  Select one of the card button elements, where you want to add the alternative text.

    The Card element page displays.

6.  Select **New**, in the **Card element attributes** area.

    The Card element attribute page displays.

7.  In the **Type** field, enter the text `AlternateTextValue`.

8.  In the **Translatable value** field, enter the text to be read out by the screen reader.

9.  Select **Submit**.

10. Select **Update** in the Card element page.



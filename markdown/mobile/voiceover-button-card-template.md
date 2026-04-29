---
title: Adding voiceover text for buttons defined as icon type within card templates
description: Screen reader support provides voiceover text for elements on the screen. However, elements like buttons defined as icon type may require additional configuration. Alternative text is added to these elements enabling the screen reader to read the content of the button within card templates.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Screen reader support, Configuring the Mobile Platform, Mobile Platform]
---

# Adding voiceover text for buttons defined as icon type within card templates

Screen reader support provides voiceover text for elements on the screen. However, elements like buttons defined as icon type may require additional configuration. Alternative text is added to these elements enabling the screen reader to read the content of the button within card templates.

## Before you begin

Role required: admin

## About this task

You can define alternative text for buttons defined as icon types as card elements within both cards and card templates. This topic covers the configuration for card templates. For more information about creating buttons defined as icon type, see [Configure an icon UI section](sg-ui-section-config-navig.md).

## Procedure

1.  Navigate to **All**.

2.  In the filter navigator, enter `sys_sg_view_template.list` to open the Card templates page.

3.  Select the card template that contains a button defined as an icon type.

    The Card template page displays.

4.  In the Card template elements area of the page, select one of the card button element templates, where you want to add the alternative text.

    The Card template element page displays.

5.  Select **New**, in the **Card template element attributes** area.

    The Card template element attribute page displays.

6.  In the **Type** field, enter the text `AlternateTextValue`.

7.  In the **Translatable value** field, enter the text to be read out by the screen reader.

8.  Select **Submit**.

9.  Select **Update** in the Card template element page.



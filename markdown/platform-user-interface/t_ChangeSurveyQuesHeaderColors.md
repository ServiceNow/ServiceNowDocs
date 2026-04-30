---
title: Change survey question header colors
description: The Classic Environment uses a header color from the base color, which allows theming from CSS properties.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing instance appearance, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Change survey question header colors

The Classic Environment uses a header color from the base color, which allows theming from CSS properties.

## About this task

One notable exception is the survey, which has its own CSS. It is possible to change the CSS by adding a property.

## Procedure

1.  Enter `sys_properties.form` into the navigation filter and press the Enter key.

    A new Property form displays.

2.  Name the new property `css.list.row.survey.background.color`.

3.  Enter the hexadecimal value of the desired color into the **Value** field.

4.  Click **Submit**.

    The survey should now use the desired color.


**Parent Topic:**[Customizing instance appearance](../reference/customizing-instance-appearance.md)


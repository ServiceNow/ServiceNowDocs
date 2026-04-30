---
title: Configure chart views for accessibility
description: Give users the option to change chart views from color segments to black and white patterns. This option can be used for accessibility purposes.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Mobile dashboard preview, Launcher screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure chart views for accessibility

Give users the option to change chart views from color segments to black and white patterns. This option can be used for accessibility purposes.

## Before you begin

Role required: admin

## About this task

To grant users the option to view charts in black and white patterns or colored segments, for all chart types. Make the **Enable data visualization patterns for charts** button available so users can select the button to view charts as black and white patterns. Alternatively, users who do not select the button can view charts as colored segments.

To display the **Enable data visualization patterns for charts** button, the system property `glide.sg.chart_accessibility.enabled` must be set to true.

## Procedure

1.  Type `sys_properties.list` in the Filter Navigator.

2.  Click **New**, and then enter the following values:

    |Field|Description|
    |-----|-----------|
    |Name|**glide.sg.chart\_accessibility.enabled**|
    |Type|true \| false|
    |Value|true|


## Result

Users can select the display option best suited for their requirements.



![Comparison of pie charts with colored segments and with black and white patterns.](../image/access-chartlines-compare.png)


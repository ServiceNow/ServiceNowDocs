---
title: Change the number of bubbles displayed on the bubble chart
description: Customize the sn\_apm\_ws.appRationalizationMaximumBubbles system property to change the number of bubbles displayed on the application rationalization bubble chart page.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-12-10"
reading_time_minutes: 1
breadcrumb: [Bubble chart view of application rationalization, Rationalization of business applications, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Change the number of bubbles displayed on the bubble chart

Customize the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property to change the number of bubbles displayed on the application rationalization bubble chart page.

## Before you begin

Role required: sn\_apm.apm\_admin

## About this task

By default, the bubble chart page displays a maximum of 500 bubbles. If you have more than 500 assessed business applications in your application landscape, you can configure the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property to increase this limit and display all assessed applications as bubbles on the bubble chart page.

## Procedure

1.  Select **All** and in the navigation filter enter **sys\_properties.list**.

2.  Navigate to the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property.

3.  Select **here** to update the property details.

    ![System property screen with the here hyperlink highlighted.](../../image/eaw-image/sys-prop-bubble-chart.png)

4.  In the **Value** field, enter the maximum number of bubbles you want displayed on the bubble chart page of application rationalization.

5.  Select **Update**.


## Result

The bubble chart page displays bubbles up to the number that you have defined in the **Value** field.

**Parent Topic:**[Bubble chart view of application rationalization](../../concept/eaw-concept/eaw-bubble-chart-view.md)


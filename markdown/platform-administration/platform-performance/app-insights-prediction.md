---
title: Application Insights p1 prediction model
description: Application Insights enables you to receive a warning when your instance is about to experience a priority 1 \(p1\) event.
locale: en-US
release: yokohama
product: Platform Performance
classification: platform-performance
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Application Insights, Monitoring platform performance, Platform performance, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Application Insights p1 prediction model

Application Insights enables you to receive a warning when your instance is about to experience a priority 1 \(p1\) event.

When the p1 prediction feature is enabled, the system monitors system performance and models it to predict when a p1 condition is likely. If the system determines that a p1 condition is likely, a warning icon \(![Warning icon.](../image/app-insights-warning-icon.png)\) is displayed on the graphs in the Application Insights application.

You must install the Predictive Intelligence \(com.glide.platform\_ml\) plugin and the Application Insights application to enable the p1 prediction feature.

To see the warning message, point your cursor to the warning icon in any graph. A pane is displayed with a message similar to the following:

`P1 Predicted: Entering a p1 alert state. We predicted a p1 might occur within 20 minutes with a confidence of 99.0%. It might be due to exhaustion in the default semaphore set and/or an unusually high number of transactions. <p>Performed on the instance at 2021-07-28 11:12:26</P>`

The warning enables you to take corrective action and avoid a p1 condition from occurring.

After you take corrective action to successfully avoid the p1 condition from occurring, the system displays a second warning indicator to signify the end of the event. Point your cursor to the warning icon. A pane is displayed with a message similar to the following:

`P1 Predicted: Ending current p1 alert state. We no longer predict a p1 might occur. <p>Performed on the instance at 2021-07-16 12:11:26</p>`

The default system properties settings for the p1 prediction model are appropriate for most environments. You can change the properties for your environment. For more information about changing the default settings, see [Application Insights properties](../reference/app-insights-properties.md).

**Parent Topic:**[Application Insights](application-insights.md)


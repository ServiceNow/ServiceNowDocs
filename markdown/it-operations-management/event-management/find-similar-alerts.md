---
title: Find similar alerts
description: You can find alerts similar to the alert currently being investigated. Save troubleshooting time by reviewing similar alerts to see how they were resolved.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Alert similarity, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Find similar alerts

You can find alerts similar to the alert currently being investigated. Save troubleshooting time by reviewing similar alerts to see how they were resolved.

## Before you begin

Ensure that the Predictive Intelligence plugin is activated. To activate this plugin, see [Activate a plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_ActivateAPlugin.md).

Ensure that the `evt_mgmt.similarity_use_ml` property is set to `true`.

Role required: evt\_mgmt\_admin

## About this task

Save time in resolving the current alert by reviewing how similar alerts were resolved. Provide resolution consistency by resolving similar alerts in the same way.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Alerts**.

2.  In the list of alerts, click the alert record that you want to investigate.

3.  In the alert record, click the **Similar Alerts** tab.

    Alerts that are similar to the alert that is being investigated are listed.

    ![Alert similarity](../image/alert-similar-list.png)

    By default, up to 10 similar alerts are listed. You can modify this value by setting the `evt_mgmt.similarity_max_similar_alerts_shown` property.

4.  If you configured a threshold, in the Related links area, click **Show Similarities Details**.

    The Sys ID and confidence level of each similar alert is displayed. The Confidence level is an indication of how the similar alert matches the parameters that you set. As an example, a high confidence percentage value indicates a higher likelihood of similarity of the alerts to the values that you set.

    ![Alert confidence](../image/alert-confidence.png)

    You can modify the value of the threshold by setting the `evt_mgmt.similarity_use_threshold` property.


**Parent Topic:**[Alert similarity](../concept/alert-similarity.md)


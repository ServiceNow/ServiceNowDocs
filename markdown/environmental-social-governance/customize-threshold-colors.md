---
title: Customize threshold colors
description: Customize the available threshold colors by enabling inactive colors in the Color dictionary.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Customize threshold colors

Customize the available threshold colors by enabling inactive colors in the Color dictionary.

## Before you begin

Role required: sn\_esg.admin, sn\_esg.program\_manager, or sn\_esg.metrics\_manager

## About this task

The Color dictionary includes multiple color options. By default, Amber, Red, and Green are active. Other colors are available but marked as inactive. Change the inactive status to make these colors available for threshold levels.

**Note:** The Color dictionary entry is in the GRC: Metrics application scope. If the current application scope is different, change the scope before editing.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Search for and select sn\_grc\_metric\_threshold.

3.  In the Columns section, select **Color**.

4.  Review the colors in the Choices related list.

5.  For each color to make available, change the Inactive value from true to false.

6.  Save the form and refresh.


## Result

The selected colors are now available in the **Color** field when creating thresholds for a metric.

**Parent Topic:**[Configuring GRC: Metrics](configuring-grc-metrics.md)


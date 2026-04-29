---
title: Set up page-level monitoring
description: Set up monitoring of the application performance at a specific page level. When collected, you can view the performance metrics data in the Metrics analyzer and device or application view.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Application monitoring setup, Configure, Digital End-User Experience, IT Service Management]
---

# Set up page-level monitoring

Set up monitoring of the application performance at a specific page level. When collected, you can view the performance metrics data in the Metrics analyzer and device or application view.

## Before you begin

DEX browser extension must be installed on the end-user devices.

The application must be already in the list of monitored applications in **Application Management**.

Role required: admin, dex\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the DEX Administration icon \(![](../image/icon-administration.png)\).

3.  On the Application management card, select **Configure applications**.

    The list of monitored applications appears.

4.  On the DEX Application Management screen, select a web application from the list.

5.  In the Edit web application form, select **Configure** under **Enable page-level monitoring**.

6.  On DEX Application Pages, select **New**.

7.  Complete the new record form as follows:

<table id="table_cxh_rpx_zgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Page Name

</td><td>

Application page name.

</td></tr><tr><td>

Domain

</td><td>

Web address that is used to launch the application and access its features and functions.

</td></tr><tr><td>

Application

</td><td>

Name of the application being monitored.

</td></tr><tr><td>

Pattern Type

</td><td>

The page URL pattern type: **Exact** or **Wildcard**.Using a wildcard, you can include not just a specific page but also its nested pages. For example, `/github.com/pricing/*`. Use a single-segment wildcard \(`*`\) for predictable one-level variations, and a multi-segment wildcard \(`**`\) when the structure beneath a path can vary widely.

</td></tr><tr><td>

Page Path

</td><td>

The URL for the page or pages using exact path or single-segment or multi-segment wildcard.

</td></tr><tr><td>

Full URL

</td><td>

The full URL automatically populated from the **Domain** and **Page Path** fields.

</td></tr><tr><td>

Metric Monitoring

</td><td>

Check box to initiate monitoring the page.This check box is selected by default.

</td></tr></tbody>
</table>8.  Select **Submit**.


## Result

When the metrics for the page are collected, you can see them from the Metrics analyzer. See [View collected metrics with Metrics analyzer](../task/view-dex-metrics.md) for more details.

**Parent Topic:**[DEX application monitoring](dex-application-monitoring.md)


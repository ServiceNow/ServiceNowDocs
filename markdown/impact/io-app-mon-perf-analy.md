---
title: Analyze user experience and monitor application performance in Instance Observer
description: Get visibility into the operational metrics of applications and their performance. You can find out the number of applications per instance, the number of pages within each application, page-level response time, user interaction frequency with each application, and page access frequency by users within each application.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analytics, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Analyze user experience and monitor application performance in Instance Observer

Get visibility into the operational metrics of applications and their performance. You can find out the number of applications per instance, the number of pages within each application, page-level response time, user interaction frequency with each application, and page access frequency by users within each application.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer** &gt; **Analytics** &gt; **User Experience**.

2.  In the **Overview** tab of the User Experience page, select an instance from the **Instance** field.

3.  Select a **Date Range** and click **Get Snapshot** to get the information related to the user experience with respect to the instance for the selected time frame.

4.  Select the **Application Monitoring** tab.

5.  Select any order to sort \(![sorting icon.](../../../reuse/icons/product-icons/sort-descending-fill-24.svg)\) and change the representation as you would like it to appear in the table.

6.  To search an application, enter the name of the application in the **Search** field.

7.  Select an application in the list and click to view its details.

    A slider opens with the details of the selected application. You can view the average response time for the selected application for the selected duration.

8.  Select any point in the graph to view the details for that particular duration.

    ![Average response time details of the selected application in a slider view.](../image/io-app-monit-slider-view.png)

    Selecting a point in the graph gives you the details of the maximum average response time.

9.  Select the **Platform Performance Analyzer** button in the slider view to get the granular details of the server transactions from the customer instance.

    On selecting the **Platform Performance Analyzer** button, and followed by validation, the user is directed to the Performance Analyzer Page of the customer instance.

    The Platform Performance Analyzer provides comprehensive details about the user interactions linking with server transactions such as schema or API name in Graph QL, Batch, and Databroker. To resolve front-office application performance-related issues, this information is essential.

    ![Waterfall model of Platform Performance Analyzer.](../image/io-platform-performance-anlyzer.png "Waterfall model of Platform Performance Analyzer")

10. Scroll down further to view the total number of pages for the application in the **Pages** section.

11. Select any link in the **Page** column to view the page-level details.

    In the page-level view, you can get the count of user interaction with the page for the selected duration and the average page response time. Additionally, you can comprehend the pages that require more time when there are contents to be downloaded in each of those pages.

12. Select the **Slowest Interactions** tab and **Fastest Interactions** tab to view the Interaction ID, Transaction type, Response time, and the Total semaphore wait time.

    The response time in the **Pages** section isn’t the same as average response time. Total semaphore wait time is the key performance metric. For more information on the performance metrics, see .

13. Select any link in the **Interaction ID** column to view the details of either the slowest or fastest instance details.


**Parent Topic:**[Analytics](../concept/io-analytics.md)


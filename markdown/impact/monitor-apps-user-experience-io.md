---
title: Track the response time of applications to monitor their performance
description: Track the response time of applications to gauge their performance. You can drill down to the transaction ID of each application to learn the slowest and fastest interactions in each instance.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Analytics, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Track the response time of applications to monitor their performance

Track the response time of applications to gauge their performance. You can drill down to the transaction ID of each application to learn the slowest and fastest interactions in each instance.

## Before you begin

Role required: admin

## About this task

With application monitoring, you can view the number of applications in each instance, the number of pages in each application, and the response time behavior of each of these pages. You can also learn the number of times a user is interacting with each application, and the number of times a user is opening a page in that application.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer** &gt; **Analytics** &gt; **User Experience**.

    In the **Overview** tab of the User Experience page, you can select an instance from the **Instance** field, a **Date Range**, and click **Get Snapshot**, to get the information related to the user experience with respect to the instance for the selected time frame.

2.  Scroll down the page to view the applications in the form of a bubble chart.

    ![Bubble chart illustrating the application's average response time.](../image/io-bubble-chart-user-exp.png)

    The default view of the bubble chart is by Average Response Time. The application's performance is indicated by the color of the bubbles and they’re color coded:

    -   Green: The response time of the application is 0–5 seconds, which indicates normal performance.
    -   Yellow: Response time is &gt;5 but ≤10 seconds that indicates poor performance.
    -   Red: &gt;10 seconds that categorizes the performance as worst.
3.  To filter the number of applications that you would like to view based on the response time in seconds, slide the **Interaction Count** slider.

4.  To view the data by **Interaction Count**, select the option in the **View by** list.

    ![Interaction counts within the bubbles.](../image/io-bubble-chart-interact-count.png)

5.  To view the user experience in the **Node** and **Transaction** charts, scroll down and select either **Transaction Count** or **Response Time** option in the **View by** list.

6.  Select the **Application Monitoring** tab to view the same data represented by bubbles but in a tabular format listed by application names with their average response time, interaction count, maximum response time, and network latency.

    ![Application monitoring in Instance Observer.](../image/io-app-monitoring-user-exp.png)

    By default, the list of applications appear in descending order of the Average Response Time in seconds.

7.  Select any order to sort \(![sorting icon.](../../../reuse/icons/product-icons/sort-descending-fill-24.svg)\) and change the representation as you would like it to appear in the table.

8.  To search an application, enter the name of the application in the **Search** field.

9.  Select an application in the list to view its details.

    A slider opens with the details of the selected application. You can view the average response time for the selected application for the selected duration.

10. Select any point in the graph to view the details for that particular duration.

    ![Average response time details of the selected application in a slider view.](../image/io-app-monit-slider-view.png)

    Selecting a point in the graph gives you the details of the maximum average response time.

11. Scroll down further to view the total number of pages for the application in the **Pages** section.

12. Select any link in the **Page** column to view the page-level details.

    In the page-level view, you can get the count of user interaction with the page for the selected duration and the average page response time. Additionally, you can comprehend the pages that require more time when there are contents to be downloaded in each of those pages.

13. Select the **Slowest Interactions** tab and **Fastest Interactions** tab to view the Interaction ID, Transaction type, Response time, and the Total semaphore wait time.

    The response time in the **Pages** section is not the same as average response time. Total semaphore wait time is the key performance metric.

14. Select any link in the **Interaction ID** column to view the details of either the slowest or fastest instance details.



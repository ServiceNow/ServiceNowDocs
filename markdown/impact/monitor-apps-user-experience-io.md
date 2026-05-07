---
title: Track the response time of applications to monitor their performance
description: Track the response time of applications to gauge their performance. You can drill down to the transaction ID of each application to learn the slowest and fastest interactions in each instance.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analytics, Monitoring instance health with Instance Observer, Platform Health, Using Impact, Impact]
---

# Track the response time of applications to monitor their performance

Track the response time of applications to gauge their performance. You can drill down to the transaction ID of each application to learn the slowest and fastest interactions in each instance.

## Before you begin

Role required: admin

## About this task

With application monitoring, you can view the number of applications in each instance, the number of pages in each application, and the response time behavior of each page. You can also learn the number of times a user is interacting with each application, and the number of times a user is opening a page in that application.

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer** &gt; **Analytics** &gt; **User Experience**.

2.  In the **Overview** tab of the User Experience page, select an instance from the **Instance** field.

3.  Select a **Date Range** and click **Get Snapshot** to get the information related to the user experience with respect to the instance for the selected time frame.

4.  Scroll down the page to view the applications in the form of a bubble chart.

    ![Bubble chart illustrating the application's average response time.](../image/io-bubble-chart-user-exp.png)

    The default view of the bubble chart is by Average Response Time. The application's performance is indicated by the color of the bubbles and they’re color coded:

    -   Green: The response time of the application is 0–5 seconds, which indicates normal performance.
    -   Yellow: Response time is &gt;5 but ≤10 seconds that indicates poor performance.
    -   Red: &gt;10 seconds that categorizes the performance as worst.
5.  To filter the number of applications that you would like to view based on the response time in seconds, slide the **Interaction Count** slider.

6.  To view the data by **Interaction Count**, select the option in the **View by** list.

    ![Interaction counts within the bubbles.](../image/io-bubble-chart-interact-count.png)

7.  To view the user experience in the **Node** and **Transaction** charts, scroll down and select either **Transaction Count** or **Response Time** option in the **View by** list.

8.  Select the **Application Monitoring** tab to view the same data represented by bubbles.

    The data that you view here is in a tabular format, listed by application names with their average response time, interaction count, maximum response time, and network latency.

    ![Application monitoring in Instance Observer.](../image/io-app-monitoring-user-exp.png)

    By default, the list of applications appear in descending order of the Average Response Time in seconds.

    For more information on application monitoring, see [Analyze user experience and monitor application performance in Instance Observer](io-app-mon-perf-analy.md).


**Parent Topic:**[Analytics](../concept/io-analytics.md)


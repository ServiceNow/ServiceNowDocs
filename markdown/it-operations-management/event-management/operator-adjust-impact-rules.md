---
title: Adjust alert impact while triaging an alert
description: As an Event Management operator, you might need to modify the impact that an alert has on an application service and on the CIs in a service. Do this when you think that the impact does not accurately represent what you see in your network environment so other operators and administrators see the correct impact information.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced operator responsibilities, Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Adjust alert impact while triaging an alert

As an Event Management operator, you might need to modify the impact that an alert has on an application service and on the CIs in a service. Do this when you think that the impact does not accurately represent what you see in your network environment so other operators and administrators see the correct impact information.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

Role required: evt\_mgmt\_operator

## About this task

Before you make any modifications to impact calculations, make sure that you understand how the application services and the CIs actually function. You might need to perform tests on network infrastructure or contact someone who can.

## Procedure

1.  Navigate to **Event Management** &gt; **Operators Workspace**.

2.  Double click the name of the application service that has the alerts you want to modify.

3.  On the Details tab, click **Service Map**.

4.  On the **Service Map** tab, click **Full Map** Tree.

5.  On the map, click **Impact Tree**.

6.  Analyze the application service to see whether the impact tree accurately reflects the impact of the alerts based on what you know about the CIs involved.

    In this example, a critical alert indicates a serious issue with a Linux server that is part of a Web portal application service.

    ![Impact rules](../image/operator-impact-rules-biz-service.png)

    Notice that the impact on the Web portal itself is red, meaning critical, even though only one of the Linux servers that it relies upon actually has a critical alert. The other Linux Server does is not impacted by the alert. Assume for this example that the Linux servers perform different roles for the web service, and that even though **PS LinuxApp02** has a critical alert, the **PS LinuxApp01** server can adequately provide all the necessary services to keep the application service operational.

7.  Click the **PS Apache03** CI, and then click **Impact** to display the impact rules for the CI.

    By default, the CI impact rule appears, showing you this information:

    ![Impact tab](../image/ci-impact-rule.png)

    -   The **Impact On** and **Influence** columns show you that the CI \(**PS Apache03**\) should inherit 100% of the impact of all child CI impacts, which in this case includes the critical impact on the **PS LinuxApp02** server. This setting is why the **PS Apache03** web server, and the application service as a whole, inherits the impact 100%.
    -   The **Critical** column shows you that a critical alert \(red\) is inherited as critical alert \(red\).
8.  Change the **Influence** value to `0` since the web server is still operational, and then change the **Critical** column to indicate that a critical impact status \(red\) should be inherited as a non-impact \(green\).

9.  Wait for the dashboard to update automatically, or click **Event Management** &gt; **Service Operations Workspace** and double-click the same application service to get an updated application service map.

    Notice that the influence on the Apache web server is 0% and the impact status is green. Also notice that the critical alert status \(red\) remains unchanged, even though the impact changed to green.

    ![Impact](../image/operator-adjust-impact-rules.png)

10. Navigate back to the Service Operations Workspace dashboard.

    Notice that the application service is now green, indicating that the overall application service is operational. The critical alert still displays at the bottom in the Alerts list, indicating that there is still an issue that you or other operators can address.


## What to do next

Your administrator might configure additional impact rules that display when you click a CI in the application service map. You can make adjustments to the **Influence** fields on any impact rule to get the most accurate impact tree.

**Parent Topic:**[Advanced tasks for the Event Management operator](../concept/operator-advanced-tasks.md)


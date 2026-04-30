---
title: Bind alerts to application CIs
description: Create an event rule to bind alerts to the host CI and also to the application CI. An incoming event from an application CI can bind to an alert based on event rule transform information.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Alert binding to CIs with event rules, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Bind alerts to application CIs

Create an event rule to bind alerts to the host CI and also to the application CI. An incoming event from an application CI can bind to an alert based on event rule transform information.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

For example, you can bind alerts to an SQL server application when the CPU on sqlServer.exe is over 90%:

-   Make sure that the event includes the host name.
-   Create an event rule with an Event Match Field entry that maps the process name to the **sa\_process\_name** mapping variable. In this case, do not use the **CI type**.
-   Use the Process to CI Type Mapping module to add custom patterns.

In the binding process, the following steps occur:

-   Identify the host.
-   If the host is found, find the application on the host. An application is considered to be running on the host if it has a "Runs on:Runs" relationship from the application to the host CI in the cmdb\_rel\_ci table.
-   If the event rule for the transform **CI type** is defined, find an application CI on that host in the CMDB.
-   If all the alert **additional\_info** about the CI matches CMDB CI fields, bind the alert to the application CI.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Rules** &gt; **Event Rules**.

2.  Click **New** and fill in the appropriate fields of the event rule.

3.  In the **Event Filter** tab, select **Node**, select an operator, and then enter the CI name, FQDN, IP, or MAC address values for the host binding.

    For example, you can specify that the node is `FQDN`.

    ![Event field binding value](../image/event-filter-binding.png)

4.  Click **Submit**.


**Parent Topic:**[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)

**Related topics**  


[Alert binding to CIs with event rules](../reference/r_EMHowAlertsBindCI.md)


---
title: DevOps log levels
description: DevOps log levels allow you to filter logs by level as well by a particular tool or application. Log levels in the DevOps application let you decide the extent of log detail you need for debugging.
locale: en-US
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, DevOps Change Velocity, IT Service Management]
---

# DevOps log levels

DevOps log levels allow you to filter logs by level as well by a particular tool or application. Log levels in the DevOps application let you decide the extent of log detail you need for debugging.

The flexibility to set log levels allows you to select the right log level information that is appropriate for your organizational needs. You can select custom log levels based on the log levels or categories that you need and as an application or tool currently supports. In previous versions of DevOps, the default log level was set to debug, and the \[sn\_devops.enable\_debug\] property that you could either enable or disable. You can select any of the following log levels for the DevOps application using the DevOps sn\_devops.devops\_log\_level property:

-   Error
-   Warning
-   Information
-   Debug
-   Trace

**Note:**

-   The base system log level is set to Warning. You must modify the base system value from DevOps properties.
-   By default, if you have different log levels for connected apps and for the DevOps application, the log level with more information is printed. For example, if you set up the log level for an app at Error, and for the DevOps application at Trace, the log levels are printed with the most information \(Trace\).

Multiple flows for in the DevOps application now use the new logging framework to collect log data during the flow execution. The following flows currently support the new log levels:

-   Artifact &amp; Package registration flows
-   Self Service Onboarding
-   Self-Service Catalog — App Onboarding
-   Change Traceability flow
-   Notification flow for plan, code, and orchestration capabilities

**Parent Topic:**[DevOps Change Velocity reference](devops-change-velocity-reference.md)


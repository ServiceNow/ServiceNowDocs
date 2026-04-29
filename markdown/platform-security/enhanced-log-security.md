---
title: Enhanced logging security
description: Explore the Attribution field in the node log lines to identify the script or component that generated the log message. Transaction start lines include the new field to identify the type of request made.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [System logs, Logs, Platform Security]
---

# Enhanced logging security

Explore the **Attribution** field in the node log lines to identify the script or component that generated the log message. Transaction start lines include the new field to identify the type of request made.

Achieve the following using the new enhancements:

-   Trace the source originator of each of the log lines
-   In case the originator info is not available, print the Java class name and an attribution
-   At the start of each transaction line, it contains the transaction ID and transaction type

Use the transaction ID of each log line to understand the information given at each log line. Once you identify the transaction type, you get the originator information of each log line. Both the transaction type and originator information of each log line together gives you the required source info of each node log line.

**Note:** SYS\_UI\_MACRO and SERVICE\_PORTAL\_WIDGET script types in attribution are not reported.

## Transaction types

The following is the list of transaction types:

-   List
-   Form
-   XMLHttp
-   Report
-   SOAP
-   Export
-   Scheduler
-   TextSearch
-   Other
-   REST
-   JSON
-   AMB
-   Archive
-   Batch REST
-   Instance Scan

## System properties

The following are the system properties required for the feature:

-   Glide.log.append.attribution: This property is enabled by default. It turns on/off the attribution information of each node line
-   Glide.db.log.append.classname.attribution: This property is enabled by default. It turns on/off logging java class name attribution


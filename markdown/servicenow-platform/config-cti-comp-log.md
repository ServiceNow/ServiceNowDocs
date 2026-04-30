---
title: Configuring CTI component logging
description: Configure CTI component logging to enable component logging to the system logs.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up ServiceNow Voice, ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configuring CTI component logging

Configure CTI component logging to enable component logging to the system logs.

## Before you begin

Role required: admin

## About this task

You can create logs for the following components:

-   Operation handler
-   Provider component
-   Provider configuration
-   Provider message transformer

**Note:** Do not leave the log configurations on in a production instance, since this can impact performance.

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Voice Core** &gt; **Log Configuration** &gt; **New**.

2.  Select the component, component table, and log level you want to configure.

3.  Choose the log level option.

    Options include the following:

    -   Off
    -   Error
    -   Warn
    -   Info
    -   Debug
4.  Click **Submit**.

5.  Create a separate record for each type of component table you want to log.

    If there are multiple logging configurations, the final log level is the selected component's log level, based on the following prioritization:

    1.  Operation handler
    2.  Provider message transformer
    3.  Provider component
    4.  Provider configuration
6.  To view the logs, navigate to **All** &gt; **System Logs** &gt; **System Log** &gt; **All**.

    You can see the logs from the invoked `sn_cti` modules, including the date created, log level, log message, and source. In the system logs, the message log level is always **info**. For basic logs from `sn_cti_core` without any logging configuration, the log level varies.


For an entry on `sn_cti_log_cfg.list` for an operation handler with **warn** log level logger located in the operation handler, the code is as follows:

```
var log= ctx.getLogger();
log.warn("CTX Logger Demo from Operation Handler");
```

Sample output:

```
cti_core:: P:c4bae70xxxxf6a9a|C:bxxxx44|T:793cxxxx7b|O:6fb1xxxx4006dabb45vc::CTX Logger Demo from Operation Handler
```

-   P: Provider
-   C: Component
-   T: Transformer
-   O: Operation handler

**Parent Topic:**[Setting up ServiceNow Voice](../concept/ccc-setup.md)


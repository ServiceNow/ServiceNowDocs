---
title: View a historical domain message
description: View historical domain messages in the log file to troubleshoot domain separation issues.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enable verbose domain logging and debug messages, Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# View a historical domain message

View historical domain messages in the log file to troubleshoot domain separation issues.

## Before you begin

Role required: admin

## Procedure

1.  Enable verbose domain logging: Navigate to **All** &gt; **Domain Admin** &gt; **Domain Separation Center** &gt; **Configure Domain Center** &gt; **Enables detail domain logging** &gt; **Yes** \(or set property `glide.sys.domain.verbose` to **True**\).

2.  Navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Enable All**.

3.  Let the debug session run for a time period, such as a day, before checking the log files.

4.  Navigate to **System Logs** &gt; **Utilities** &gt; **Node Log File Download**.

5.  Open the record for the day you want to view.

    Log files use the naming format `localhost_log.<yyyy-mm-dd>.txt`.

6.  Click the **Download** log related link.

7.  Open the downloaded log file in a text editor and search for log messages with the following format:

    Query against table incident restricted by domain values `[global, Software[8a4dde73c6112278017a6a4baf547aa7]]`

    In this example, a user only saw records from the Incident table that matched the global and Software domains.



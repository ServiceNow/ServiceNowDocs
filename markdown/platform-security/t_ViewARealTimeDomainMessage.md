---
title: View a real-time domain message
description: You can view real-time domain messages from the system logs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Enable logging and debug messages, Setup and administration, Domain separation for service providers, Access Management]
---

# View a real-time domain message

You can view real-time domain messages from the system logs.

## Before you begin

Role required: admin

## Procedure

1.  Enable verbose domain logging: Navigate to **All** &gt; **Domain Admin** &gt; **Domain Separation Center** &gt; **Configure Domain Center** &gt; **Enables detail domain logging** &gt; **Yes** \(or set property `glide.sys.domain.verbose` to **True**\).

2.  Navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Enable All**.

    Because this is a real time review, there is no need to let the debug session run prior to checking the log files.

3.  Navigate to the session debug console to view the detailed system domain logs.

4.  Search for the text Query against table.

    This query finds log messages in this format:

    ```
    08:36:43.974: [Domain Paths] Query against table incident restricted by domain values [Database Atlanta[db53580b0a0a0a6501aa37c294a2ba6b], 
    Database[287ee6fea9fe198100ada7950d0b1b73], 
    Database San Diego[db53a9290a0a0a650091abebccf833c6], global, NY DB[5f74727dc0a8010e01efe33a251993f9]]
    ```

    In this example, the user viewing the Incident table only saw records that matched the Database Atlanta, Database, Database San Diego, global, and NY DB domains.



---
title: Manually start, stop, and restart a MID Server
description: If you did not start the MID Server at the end of the installation procedure, you can manually start the MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t\_InstallMIDServerAsWinService.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Manually start, stop, and restart a MID Server

If you did not start the MID Server at the end of the installation procedure, you can manually start the MID Server.

## Before you begin

Role required: MID Server Service account user or a Windows Admin account

This procedure is only for users who install the MID Server using the ZIP file. The Windows MID Server installer completes the installation automatically.

## Procedure

1.  Open the agent directory in the directory you created for the MID Server installation files.

    For example, the path might be `C:\ServiceNow\MID Server1\agent`.

2.  Start the MID Server by executing the `start.bat` file.

3.  To stop the MID Server, execute the `stop.bat` file.

4.  To restart a stopped MID Server, either:

    -   If the MID Server is stopped, execute the `start.bat` file.
    -   If the MID Server is running, execute the `restart.bat` file.

**Parent Topic:**[MID Server reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-reference-information.md)

**Related topics**  


[MID Server system requirements]()

[MID Server upgrades]()

[Resolving MID Server issues]()

[MID Server dashboard]()

[MID Server properties]()

[MID Server parameters]()

[MID Server Configuration Parameter settings and priority]()

[MID Server File Cleaner]()

[MID Server protected records and reserved characters]()

[MID Server privileged commands]()

[MIDSystem methods]()

[MID Server heartbeat]()

[Set the MID Server JVM memory size]()

[Pause the MID Server]()


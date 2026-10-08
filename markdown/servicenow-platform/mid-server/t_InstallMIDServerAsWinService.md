---
title: Manually start, stop, and restart a MID Server
description: Start, stop, or restart a MID Server manually when needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/mid-server/t\_InstallMIDServerAsWinService.html
release: brazil
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [MID Server reference, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Manually start, stop, and restart a MID Server

Start, stop, or restart a MID Server manually when needed.

## Before you begin

Role required: MID Server Service account user or an Admin account

This procedure is only for users who install the MID Server using the ZIP file. For Windows, the Windows MID Server installer completes the installation automatically.

## Procedure

1.  Open the agent directory in the directory you created for the MID Server installation files.

    For example, the path might be:

    -   Windows: `C:\ServiceNow\MID Server1\agent`
    -   Linux: `/ServiceNow/MID Server1/agent`
2.  To start the MID Server:

    -   Windows: Execute the `start.bat` file.
    -   Linux: Run `./start.sh`
3.  To stop the MID Server:

    -   Windows: Execute the `stop.bat` file.
    -   Linux: Run `./stop.sh`
4.  To restart the MID Server:

    -   Windows: Execute the `restart.bat` file.
    -   Linux: Run `./restart.sh`

**Parent Topic:**[MID Server reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/mid-server/mid-server-reference-information.md)

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


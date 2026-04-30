---
title: Configure Osqueryd logs for SAM total usage metrics
description: By default, Osquery supports log rotation based on size. To enable it for SAM total usage metrics and to configure the log size and rotation, you need to add specific flags for Osqueryd service.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Using push-based Discovery and SAM together, ACC Discovery, ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Configure Osqueryd logs for SAM total usage metrics

By default, Osquery supports log rotation based on size. To enable it for SAM total usage metrics and to configure the log size and rotation, you need to add specific flags for Osqueryd service.

## Before you begin

Role required: admin

**Note:** SAM with Osqueryd consumes memory and CPU cycles. For example, with the Agent installed on a Windows Machine having 2 CPU core, 8 GB RAM, 1000 software installations, and 500 running processes, the following was observed:

-   Average CPU usage for the Agent and Osqueryd was less than 10 % CPU and maximum of 30% CPU. This will only occur when the SAM background policy is triggered. By default, the trigger happens every 480 seconds.
-   Average Memory usage for Agent and Osqueryd was less than 10 MB and maximum of 26 MB was consumed.

To store the data for a single running process for two days, the log file size on an average should be 52429 bytes. The log file size must be increased if the number of running processes on the machine is higher. For example, with 500 running processes the log size would be on average 25 MB which is 26214400 bytes.

## Procedure

1.  Navigate to **Osqueryd installation folder**.

2.  Find and edit the osquery.flags file.

3.  Add the below flags with these sizing guidelines:

    **Note:** Modification of the log file size should be done as per the Osqueryd Log file sizing guidelines.

    For Windows:

    -   --logger\_rotate=true
    -   --logger\_rotate\_size=26214400
    -   --logger\_rotate\_max\_files=1
    -   --watchdog\_level=1
    For macOS:

    -   --logger\_rotate=true
    -   --logger\_rotate\_size=26214400
    -   --logger\_rotate\_max\_files=1
    -   --watchdog\_level=1
    -   --logger\_mode=0644
4.  Save the file.


## Result

Once the Osqueryd schedule and Osqueryd logs are configured the Osqueryd service can start.

The schedule runs the Osquery: Select name, pid, elapsed\_time, start\_time, user\_time, system\_time, username from processes p JOIN users u ON u.uid = p.uid where p.elapsed\_time != -1 AND u.type !='special';" runs every 5 minutes \(300 seconds\) on the target machine. This logs the results into the log file. The log file contains snapshot entries of all the queries configured to run by the Osqueryd . This query contains all the processes attributes.

**Note:**

A temporary file `marker.json` is created in a temporary local folder on your machine in the directory:

For Windows `: <userprofile>\\AppData\\Local\\AgentClientCollector\\SAM`.

For macOS: `/Library/Application\ Support/servicenow/agent-client-collector`.

This file has read/write permissions and contains the marker data: **Data and Last Read Unix Time stamp**.

The Osqueryd can also be configured to write its logs to a custom directory path instead of the default directory. If you choose a custom directory, modify the check definition \[samadvanced-background-log-check\].


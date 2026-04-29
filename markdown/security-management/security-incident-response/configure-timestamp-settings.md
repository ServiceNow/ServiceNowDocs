---
title: Configuring Timestamp Settings for Triage Acquisition
description: Configure and verify the timestamp settings before the installation procedure.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [FireEye Endpoint Security integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configuring Timestamp Settings for Triage Acquisition

Configure and verify the timestamp settings before the installation procedure.

## Before you begin

Role required: NowPlatform Security incident administrator \(sn\_si.admin\)

Before installing the FireEye application, there are some pre-requisites that need to be performed on FireEye.

Triage Acquisition can be requested with an input of 'Around Timestamp' field or 'Standard' field. Around timestamp requests information collected during a specified amount of time before the timestamp until a specified amount of time after the timestamp. The timestamp is the time the event that generated the alert occurred. If you select Standard, the Endpoint Security appliance requests information from the host for all data around an event.

When an Endpoint Security user requests a triage collection based on a specific date and time the agent returns information for a specified window of time before and after the alert. The timestamp settings control the length of the window for the triage collection. Timestamp settings apply only to agent URL events \(URL Monitor Events\) and registry key events \(Reg Key Events\).

You can use the Timestamp Settings tab to specify the length of time before and after the timestamp during which information is collected. Timestamp Settings can range from 0- 86400 seconds. The default for both settings is 600 seconds.

You can use the Timestamp Settings tab on the Automatic Triage Settings page to specify the length of time before and after the timestamp during which information is collected. The timestamp is the time when the event that triggered the alert occurred.

## Procedure

1.  Navigate to **Endpoint Security Web UI**.

2.  Select **Admin** &gt; **Triage Settings**.

3.  Click **Timestamp Settings** tab on the **Automatic Triage Settings** page.

4.  Specify the length of time before and after the timestamp for which the information is needed.

5.  Enter the number of seconds before the specified timestamp for which the information is needed.

6.  Enter the number of seconds after the timestamp for which the information is needed.

7.  Click **Save**.

    **Note:** You can change all values on the page back to the default settings by clicking **Reset to Defaults**, and clicking Save.

    -   **Acquisition Space Area**: The Acquisitions page shows how much disk space is remaining for acquisitions.
    -   **Setting Disk Utilization Limits for Acquisitions:**

        -   Triages, file acquisitions, and data acquisitions can accumulate over time and use an increasing amount of disk space. To control this, you can allot a set amount of disk space for them. Ten percent of the disk space you specify is reserved for automatic triage acquisitions. When the total allotted acquisition space is exceeded, the oldest automatic triages are deleted.
        -   When the total disk size of completed acquisitions exceeds a specified limit, the Endpoint Security appliance deletes the oldest completed acquisitions until enough disk space is cleared to bring the total under the specified limit. Acquisitions that are not yet completed are not affected.
        -   The Endpoint Security appliance automatically deletes acquisitions if an Administrator, Analyst, or Investigator uses the Endpoint Security Web UI to manually delete the associated agent.
        To set disk utilization limits for complete acquisitions using the Web UI:

    -   Navigate to **Endpoint Security Web UI**.
    -   Select **Disk Utilization Limits** from the **Admin** menu.
    -   In the **Acquisition space limit** area, specify the maximum amount of disk space \(in GB\) that can be used to store triage, file and data acquisitions. Valid values and defaults vary based on your Endpoint Security appliance model. The values appropriate for your model are shown on the Disk Utilization Limits page.
    -   Click **Save**.
    **Note:** All the mentioned settings are honoured and in case of any failures or errors, ServiceNow AI Platform just returns those errors.



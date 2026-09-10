---
title: Run Certificate Discovery via URL scans in Discovery Admin Workspace
description: Create a certificate Discovery schedule in the Discovery Admin Workspace to collect certificates from specific URLs rather than from ports found during IP-based Discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/daw-discover-certs-url.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Visibility to TLS certificates, Configure, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Run Certificate Discovery via URL scans in Discovery Admin Workspace

Create a certificate Discovery schedule in the Discovery Admin Workspace to collect certificates from specific URLs rather than from ports found during IP-based Discovery.

## Before you begin

Confirm the following:

-   Discovery Admin Workspace v1.20.0 is installed.
-   Certificate Inventory and Management v4.2.4 is installed.
-   The ServiceNow AI Platform is running on the Brazil, Australia, or Zurich release starting with Patch 8.

Role required: discovery\_admin

## About this task

URL scan discovery visits each URL that you list and collects the certificate served at that URL. Use this method when you need to collect certificates from specific endpoints rather than from ports found during IP-based Discovery.

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

2.  Select **New Discovery** from the header of any tab on the Schedules page.

3.  Select **Certificate discovery** and select **Continue**.

4.  Select **Discover via URL scans**, then select **Continue**.

5.  Enter a name for the Discovery schedule.

6.  Choose your MID Server.

    |Option|Description|
    |------|-----------|
    |**Use a cluster of MID servers**|Select an existing MID Server cluster from the drop-down list. Clusters provide failover protection and load balancing between MID Servers. See [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/t_ConfigureAMIDServerCluster.md) for more information.|
    |**Automatically select a MID server**|An available MID Server is automatically selected when the Discovery schedule runs. See [Automatic MID Server selection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/agent-client-collector/acc-auto-mid-selection.md) for more information.|
    |**Search for a MID server**|Select an existing MID Server from the drop-down list. Only MID Servers that are validated and up are displayed.|

7.  Select **Next**.

8.  Choose the URLs to scan for certificates.

    1.  From **Available URLs**, select the check box for each URL to scan.

    2.  To add a URL that isn't listed, select **Add URL** and enter the URL.

        Select **Add more** to add multiple URLs. Then select **Add URLs**.

9.  Confirm your selections appear under **Selected URLs**.

10. Select **Next**.

11. Configure the Discovery schedule.

    |Option|Description|
    |------|-----------|
    |**Run on demand**|The schedule only runs when triggered manually. Trigger the schedule by selecting **Finish and run** at the end of this setup, or by navigating to the schedule in the Schedules table and selecting **Discover Now**.|
    |**Run at a scheduled time**|The schedule runs at a scheduled date and time. Use the fields to define when the schedule runs.|
    |**Run after series**|The schedule runs after another existing Discovery schedule completes, staggering or chaining them together. Selecting an existing schedule displays a relationship map of all associated schedules.|
    |**Cancel discovery if longer than maximum runtime**|If the schedule exceeds the maximum runtime, it's canceled. After the option is toggled on, configure the runtime threshold.|
    |**Finish and run**|After you select this option, all the information you provided is validated. Then, a Discovery schedule is created in the background, a Discovery status is created, and the schedule is run. You're redirected to the Status Details page for the schedule.|
    |**Finish**|After you select this option, all the information you provided is validated. A Discovery schedule is created and you're redirected to its entry in the Discovery Schedules \[discovery\_schedule\] table. You can edit the schedule information or run it by selecting **Discover Now**.|

    -   If you selected **Finish and Run**, Discovery visits each selected URL and collects its certificate. You're redirected to the [Status details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/daw-disco-status-details.md) page for the schedule.
    -   If you selected **Finish**, you're redirected to the [Schedule details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/c_daw-disco-schedule-details.md) page for the schedule.


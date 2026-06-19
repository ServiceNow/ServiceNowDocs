---
title: Install Agent Client Collector on a non-persistent VDI reference device
description: Install Agent Client Collector \(ACC\) on the reference device used to create the non-persistent VDI golden image. The mid-less installation method, combined with the LOCALUSERNAME="SYSTEM" parameter and a non-persistent setting in acc.yml, configures the agent to operate correctly across copied VDI sessions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/install-acc-on-np-vdi-golden-image.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 1
breadcrumb: [Non-persistent VDI monitoring configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Install Agent Client Collector on a non-persistent VDI reference device

Install Agent Client Collector \(ACC\) on the reference device used to create the non-persistent VDI golden image. The mid-less installation method, combined with the `LOCALUSERNAME="SYSTEM"` parameter and a non-persistent setting in `acc.yml`, configures the agent to operate correctly across copied VDI sessions.

## Before you begin

Verify that the reference device has the following before creating the golden image:

-   Digital End-User Experience Application and Device Health 3.2.3 or higher.
-   Access to create and configure the non-persistent VDI golden image.
-   Administrator access on the reference device.
-   Network access from the reference device to your Agent Client Collector gateway and your ServiceNow instance.

Role required: sn-dex-admin

## Procedure

1.  From your ServiceNow instance, navigate to **Agent Client Collector** &gt; **Agent Download** and copy the mid-less installation command.

2.  Download the Agent Client Collector MSI installer to the reference device.

3.  Append `LOCALUSERNAME="SYSTEM"` to the MID-less installation command.

    The `LOCALUSERNAME="SYSTEM"` parameter configures the agent to run as the local `SYSTEM` account, which is required for non-persistent VDI monitoring.

    For the full MID-less installation command syntax, parameters, and an example, see [Non-persistent VDI parameters, scripts, and settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/non-persistent-vdi-scripts.md).

4.  Run the command on the reference device to install Agent Client Collector.

5.  Stop the Agent Client Collector service from Services.

    Open Services as an administrator before stopping the service.

6.  Update the `acc.yml` file at `C:\ProgramData\ServiceNow\agent-client-collector\` to set the agent to non-persistent mode.

    ```
    persistence_type: non_persistent
    ```

7.  Start the Agent Client Collector service from Services.

8.  Wait for host data collection to complete and for policies to synchronize to the agent.

9.  Verify that assets are synced by checking the contents of the cache folder at `C:\ProgramData\ServiceNow\agent-client-collector\cache\`.


## What to do next

Install the DEX browser extension on the reference device. See [Enable DEX browser extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/enable-dex-browser-extension.md).

Prepare the reference device for copying. See [Prepare non-persistent VDI reference device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/prepare-np-vdi-golden-image.md).


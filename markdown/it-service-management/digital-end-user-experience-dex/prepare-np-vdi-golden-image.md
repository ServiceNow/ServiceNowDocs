---
title: Prepare non-persistent VDI reference device
description: Remove the registration certificate, agent identifier, cached databases, and logs from the reference device before sealing it as a golden image. This cleanup confirms that each VDI duplicated from the image registers with a unique identity on first start.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/prepare-np-vdi-golden-image.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 2
breadcrumb: [Non-persistent VDI monitoring configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Prepare non-persistent VDI reference device

Remove the registration certificate, agent identifier, cached databases, and logs from the reference device before sealing it as a golden image. This cleanup confirms that each VDI duplicated from the image registers with a unique identity on first start.

## Before you begin

Complete the following tasks before you prepare the golden image:

-   [Install Agent Client Collector on a non-persistent VDI reference device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/install-acc-on-np-vdi-golden-image.md)
-   [Enable DEX browser extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/enable-dex-browser-extension.md)

Role required: sn\_dex.admin and administrator access on the reference device

**Important:** If you skip the cleanup steps in this task, every VDI cloned from the golden image inherits the same certificate and agent identifier. Cloned VDIs cannot register correctly when this happens.

## About this task

This task removes the artifacts that the Agent Client Collector generated during installation and initial registration on the reference device. After cleanup, you set `disable-asset` to `true` in `acc.yml` so that each cloned VDI generates its own asset record on first start. After you complete this task, the reference device is ready to be sealed as the golden image used to clone the VDI pool.

## Procedure

1.  Stop the Agent Client Collector service from **Services**.

    Open **Services** as an administrator before stopping the service.

2.  Set the Agent Client Collector service **Startup type** to **Manual**.

    The cloned VDIs start the service through the logon script rather than at boot.

3.  Navigate to `C:\ProgramData\ServiceNow\agent-client-collector\config\cert\cnc\` and delete both `cnc_chain` and `private_key`.

4.  Navigate to `C:\ProgramData\ServiceNow\agent-client-collector\cache\` and delete `agent_now_id`.

5.  Empty the contents of the `databases` and `log` folders under `C:\ProgramData\ServiceNow\agent-client-collector\`.

6.  Open `acc.yml` at `C:\ProgramData\ServiceNow\agent-client-collector\` and update the file as follows.

    1.  Remove the line that begins with `agent-key-id`.

    2.  Add the registration key again.

    3.  Uncomment `disable-asset` and set its value to `true`.

        ```
        disable-asset: true
        ```

7.  Save and close `acc.yml`.


## Result

The reference device is ready to be sealed as a golden image. The Agent Client Collector service does not start automatically, no certificate or agent identifier carries forward, and each cloned VDI generates its own asset record on first start.

## What to do next

Configure the VDI pool to use the golden image. See [Manage logon and logoff scripts for non-persistent VDIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/configure-np-vdis.md).


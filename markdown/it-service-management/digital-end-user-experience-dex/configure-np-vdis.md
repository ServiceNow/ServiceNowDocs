---
title: Manage logon and logoff scripts for non-persistent VDIs
description: Configure logon and logoff scripts in a non-persistent VDI pool to control how the MID Server starts and stops during virtual desktop sessions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/digital-end-user-experience-dex/configure-np-vdis.html
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Non-persistent VDI monitoring configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Manage logon and logoff scripts for non-persistent VDIs

Configure logon and logoff scripts in a non-persistent VDI pool to control how the MID Server starts and stops during virtual desktop sessions.

## Before you begin

Complete the following tasks before you prepare the golden image:

-   [Install Agent Client Collector on a non-persistent VDI reference device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-end-user-experience-dex/install-acc-on-np-vdi-golden-image.md)
-   [Enable DEX browser extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-end-user-experience-dex/enable-dex-browser-extension.md)
-   [Prepare non-persistent VDI reference device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-end-user-experience-dex/prepare-np-vdi-golden-image.md)

Role required: sn-dex-admin

## Procedure

1.  Configure your persistent storage to be accessible from all VDIs in the pool, and verify that the VDIs have read and write access to the certificate storage location.

    This storage backs up and restores VDI certificates across sessions. It must remain accessible throughout the VDI lifecycle.

2.  Place the logon script in your VDI management tool's session-start or post-synchronization script configuration, and place the logoff script in the session-end or power-off script configuration.

    The logon script runs at the start of each session to restore the certificate from your persistent storage to the VDI. The logoff script runs at the end of each session to push any remaining metrics to the ServiceNow instance before the session disconnects.

    For more information, see [Non-persistent VDI parameters, scripts, and settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-end-user-experience-dex/non-persistent-vdi-scripts.md).

3.  Depending on the tool your organization uses for authentication, modify the authentication steps in the logon and logoff scripts to connect to your persistent storage location.

4.  Create the golden image from the reference device and configure the VDI pool to use it.



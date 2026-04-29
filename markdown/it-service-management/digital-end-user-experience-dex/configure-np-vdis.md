---
title: Configure monitoring non-persistent VDIs
description: Learn how to start non-persistent Virtual Desktop Infrastructure \(VDI\) monitoring by creating a golden image on the base instance. This process enables DEX Service Desk agents to collect and view non-persistent data from VDIs.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitoring non-persistent VDIs, Configure, Digital End-User Experience, IT Service Management]
---

# Configure monitoring non-persistent VDIs

Learn how to start non-persistent Virtual Desktop Infrastructure \(VDI\) monitoring by creating a golden image on the base instance. This process enables DEX Service Desk agents to collect and view non-persistent data from VDIs.

## Before you begin

Make sure you have the following on the reference device:

-   Installed DEX plugin
-   Installed Agent Client Collector plugin
-   Retrieved login and logout scripts provided by ServiceNow
-   Persistent storage accessible from all VDIs in the pool, such as a network drive or a secrets vault, to store and manage VDI certificates

**Note:** DEX supports monitoring non-persistent VDIs on VMware.

**Note:** Non-persistent VDIs with multi-user sessions are not currently supported.

Role required: admin

## About this task

When a VDI starts for the first time, the standard registration process is completed and a certificate is downloaded from the ServiceNow instance. The certificate is then backed up to your persistent storage for future sessions.

A golden image is a preconfigured reference device that serves as the base for all VDIs in a pool.

Your persistent storage holds the certificates that VDIs use to authenticate with ServiceNow. On first initialization, a VDI downloads and backs up its certificate to your storage. Subsequent sessions restore the certificate from storage, eliminating re-registration.

Logon scripts run at session start as a post-synchronization or session logon script. Restores the certificate from your persistent storage to the VDI, enabling authentication without downloading a new certificate.

Logoff scripts run at session end as a session logoff or power-off script. Pushes residual metrics from the Agent Client Collector to the ServiceNow instance before the session disconnects.

## Procedure

1.  On the reference device, update the `acc.yml` file as follows:

    `persistence_type : non_persistent`

2.  Configure your persistent storage to be accessible from all VDIs in the pool, and verify that the VDIs have read and write access to the certificate storage location.

    This storage backs up and restores VDI certificates across sessions. It must remain accessible throughout the VDI lifecycle.

3.  Place the logon script in your VDI management tool's session-start or post-synchronization script configuration, and place the logoff script in the session-end or power-off script configuration.

    The logon script runs at the start of each session to restore the certificate from your persistent storage to the VDI. The logoff script runs at the end of each session to push any remaining metrics to the ServiceNow instance before the session disconnects.

4.  Depending on the tool your organization uses for authentication, modify the authentication steps in the logon and logoff scripts to connect to your persistent storage location.

5.  Create the golden image from the reference device and configure the VDI pool to use it.



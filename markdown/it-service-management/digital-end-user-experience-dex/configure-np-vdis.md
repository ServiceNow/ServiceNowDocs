---
title: Configure non-persistent VDIs monitoring
description: Learn how to start non-persistent Virtual Desktop infrastructure \(VDI\) monitoring by creating a golden image on the base instance. This process enables DEX Service Desk agents to collect and view non-persistent data from VDIs.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 1
breadcrumb: [Monitoring non-persistent VDIs, Configure, Digital End-User Experience, IT Service Management]
---

# Configure non-persistent VDIs monitoring

Learn how to start non-persistent Virtual Desktop infrastructure \(VDI\) monitoring by creating a golden image on the base instance. This process enables DEX Service Desk agents to collect and view non-persistent data from VDIs.

## Before you begin

Make sure you have the following on the reference device:

-   Installed DEX plugin
-   Installed Agent Client Collector plugin
-   Retrieved login and logout scripts provided by ServiceNow

Role required: admin

## About this task

When a VDI starts for the first time, the standard registration process is completed and a certificate is downloaded from the ServiceNow cloud. The certificate is then backed up to the persistent storage for future sessions.

## Procedure

1.  On the reference device, update the `acc.yml` file as follows:

    `persistence_type : non_persistent`

2.  Create a golden image and configure the VDI pool with post-synchronization and power-off scripts.

3.  Depending on the tool your organization uses for authentication, modify authentication steps in the login and logout scripts.



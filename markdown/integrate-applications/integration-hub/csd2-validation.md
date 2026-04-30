---
title: CSD 2.0 validation process
description: After Microsoft Endpoint Configuration Manager deploys software to a target computer, CSD 2.0 detects the installation and validates its status.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# CSD 2.0 validation process

After Microsoft Endpoint Configuration Manager deploys software to a target computer, CSD 2.0 detects the installation and validates its status.

**Note:** This is applicable only if you are using SAM.

CSD 2.0 uses the following methods for detecting software installed on the target machine:

-   Discovery: CSD 2.0 is configured to leverage Discovery to detect software installations. You can run Discovery manually at any time, or by a scheduled job.
-   Microsoft Endpoint Configuration Manager Integration: You can import provider data into the CMDB using the features in the Integration - Microsoft Endpoint Configuration Manager plugin if Discovery is not active on the instance.

The instance uses the data gathered by Discovery or the Microsoft Endpoint Configuration Manager integration plugin to populate the Software Installation \[cmdb\_sam\_sw\_install\] table. To validate installations using this data, CSD 2.0 runs a scheduled job called Reconcile Requested Software that uses [CSD property](../../integrationhub/reference/csd-prop-installed.md) settings. This process reconciles the software installation data accumulated in the CMDB and makes these status updates:

-   **Not installed** or **Not Synced** to **Installed**: The user has installed the requested software within the time limit configured in the **sn\_csd.softwareInstallExpDays** property.
-   **Not installed** or **Not Synced** to **Status check expired**: The time limit has expired for the user to install the requested software. The system stops checking for installation when the time limit expires.

**Parent Topic:**[Client Software Distribution 2.0 application](csd-app-2.md)


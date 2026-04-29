---
title: Client software distribution validation process
description: After SCCM deploys software to a target computer, client software distribution \(CSD\) detects the installation and validates its status.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client software distribution from SCCM, Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Client software distribution validation process

After SCCM deploys software to a target computer, client software distribution \(CSD\) detects the installation and validates its status.

Client software distribution uses the following methods for detecting software installed on the target machine:

-   **Discovery**: CSD is configured to leverage Discovery to detect software installations. You can run Discovery manually at any time, or by a scheduled job.
-   **Microsoft SCCM Integration**: You can import SCCM data into the CMDB using the features in the Integration - Microsoft SCCM plugin if Discovery is not active on the instance.

The instance uses the data gathered by Discovery or the SCCM integration plugin to populate the Software Installation \[cmdb\_sam\_sw\_install\] table. To validate installations using this data, CSD runs a scheduled job called Reconcile Requested Software that uses [Properties installed](https://www.servicenow.com/docs/access?context=csd-prop-installed&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) settings. This process reconciles the software installation data accumulated in the CMDB and makes these status updates:

-   **Not installed** to **Installed**: The user has installed the requested software within the time limit configured in the **sn\_client\_sf\_dist.softwareInstallExpDays** property.
-   **Not installed** to **Status check expired**: The time limit has expired for the user to install the requested software. The system stops checking for installation when the time limit expires.

**Parent Topic:**[Client software distribution from SCCM](c_CSDFromAnSCCMHost.md)


---
title: How Agent Client Collector for Visibility Content works
description: Agent Client Collector for Visibility Content \(ACC-VC\) requires installation of ServiceNow Agent Client Collector \(ACC\) on the target host. ACC is a derivative of Sensu-Go, an open-source software.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/how-acc-v-works.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-11-04"
reading_time_minutes: 4
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Exploring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# How Agent Client Collector for Visibility Content works

Agent Client Collector for Visibility Content \(ACC-VC\) requires installation of ServiceNow Agent Client Collector \(ACC\) on the target host. ACC is a derivative of Sensu-Go, an open-source software.

## ACC-VC use cases

ACC-VC applies Checks and Policies to schedule and collect host data. ACC-VC is triggered in the following cases:

-   Periodic scheduling: A policy-based approach where Discovery is triggered on a periodic basis.
-   On CI delete: When the computer or server CI record is deleted.
-   MID Server cycle: When the MID Server goes down and comes back up.
-   Target host cycle: When the target host goes down and comes back up.
-   Network break: When there is a break in the network link to the target.

**Note:** Discovery is triggered for those agents whose hosts are already present. Agents whose hosts are not present are discovered through ACC-F.

## ACC-VC checks and policies

The ACC-VC assets are stored as Agent plugins with the main entry point \[acc\_visibility\_main\] and other modules for OS families. There is one main system Discovery Check definition, called **Enhanced Discovery**, which is used by the **Enhanced Discovery Policy**. This ACC-VC policy runs off a schedule, which is defaulted to 24 hours \(86,400 seconds\). This policy configuration is synced to all agents as defined in the ACC-VC policy.

When the payload is returned from the MID Server to the instance, the ACC-VC Check Type, **EnhancedDiscovery**, delegates tasks to the EnhancedDiscoveryHandler script include provided by ACC-VC. The script contains logic to process the data from the check and handles tasks such as:

-   Data transformation into an identification and reconciliation engine \(IRE\) compatible payload
-   Non-CI data reconciliation \(cmdb\_running\_processes, cmdb\_tcp\_connections, and so on\)

The ACC-VC Check Definition, **Enhanced Discovery**, is initiated by the ServiceNow Instance. Then, an ECC Queue record with topic, MonitoringProbe, is created on the output queue with relevant Check information. The MID Server then processes the check by sending a message to the ACC via WebSocket over TLS.

During this time, the MID Server also serves any relevant Assets or Plugins that the ACC requests. The MID Server ensures the Assets and Plugins are relevant to the particular Operating System, platform, OS version, and architecture on which the ACC is running.

You can edit and modify all parts of the ACC-VC application including check type, policy, and check definition. See [Checks and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/agent-client-collector/checks-policies.md) for more information.

## ACC-VC CI status updates

Each time the **Enhanced Discovery** check returns data for a host, ACC-VC updates the **Install Status** field on the host CI and on its related network adapter and IP address CIs. The **Enhanced Discovery Policy** schedule determines the frequency. The default is every 24 hours.

When ACC-VC creates a host CI, ACC-VC sets **Install Status** to Installed and **Operational Status** to Operational. After that, ACC-VC changes the install status and operational status of CIs only as described in the following table.

|CI type|Condition|Resulting status|
|-------|---------|----------------|
|Host CI \(**Install Status**\)|The current install status is Retired, Stolen, or Absent.|Installed|
|Host CI \(**Operational Status**\)|The current operational status is Retired.|Operational|
|Network adapter \(**Install Status**\)|The adapter name and macOS address match an adapter in the latest data.|Installed|
|Network adapter \(**Install Status**\)|The CI has the adapter, but the adapter is not in the latest data.|Absent|
|IP address \(**Install Status**\)|The IP address is in the latest data for its network adapter.|Installed|
|IP address \(**Install Status**\)|The network adapter is still reported, but the IP address is no longer reported for it.|Absent|

**Note:**

-   The host CI rules apply to the Computer \[cmdb\_ci\_computer\] table only.
-   Customers set the Retired, Stolen, and Absent states on a host CI. ACC-VC doesn't set these states. If a host stops reporting, ACC-VC does not change the install status or operational status of its CI.
-   ACC-VC marks network adapters and IP addresses as Absent only when the data includes network adapter information. ACC-VC deletes DNS name and OS user records that are no longer reported instead of setting them to Absent.

## Supported operating systems

ACC-VC collects the system attributes and related lists normally collected by the OS pattern. ACC-VC currently supports the following operating systems on x86\_64 architecture:

-   Linux
    -   Rocky Linux 10
    -   Red Hat Enterprise Linux \(RHEL\) 7, 8, 9, and 10.
    -   Oracle Linux \(OL\) 7, 8, 9, 10
    -   CentOS 7
    -   CentOS Stream 8 and 9
    -   SLES 12, 15
    -   Ubuntu 18.04, 20.04, 22.04 LTS and 24.04 LTS
    -   Amazon Linux 2, Amazon Linux 2023
    -   Debian 9, 10, 11, 12 and 13
-   Microsoft Windows
    -   Windows Server 2012, 2012r2, 2016, 2019, 2022, 2025
    -   Windows 10 Enterprise Edition
    -   Windows 11 Enterprise and Professional Editions
-   macOS
    -   10.15- Catalina
    -   11- Big Sur
    -   12- Monterey
    -   13- Ventura
    -   14- Sonoma
    -   15- Sequoia
    -   26- Tahoe

ACC-VC also supports the following operating systems on ARM64 architecture:

-   macOS:
    -   12- Monterey
    -   13- Ventura
    -   14- Sonoma
    -   15- Sequoia
    -   26- Tahoe
-   Linux: Ubuntu 22.04 LTS

## Virtual machines and cloud instances

ACC-VC associates a target, discovered via Discovery, with a pre-existing virtual machine \(VM\) Instance CIs. ACC-VC associates the discovered CI record with any pre-existing VM Instance record or Cloud Server Instance record with appropriate CMDB relationships.

The following variants of virtualization and cloud server vendors are supported for ACC-VC:

-   vCenter
-   Amazon AWS Cloud
-   Google \(GCP\)
-   Microsoft Azure


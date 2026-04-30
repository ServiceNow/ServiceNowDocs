---
title: How Agent Client Collector for Visibility works
description: Agent Client Collector for Visibility \(ACC-V\) requires installation of ServiceNow Agent Client Collector \(ACC\) on the target host. ACC is a derivative of Sensu-Go, an open-source software.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Agent Client Collector for Visibility, Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# How Agent Client Collector for Visibility works

Agent Client Collector for Visibility \(ACC-V\) requires installation of ServiceNow Agent Client Collector \(ACC\) on the target host. ACC is a derivative of Sensu-Go, an open-source software.

## ACC-V use cases

ACC-V applies Checks and Policies to schedule and collect host data. ACC-V is triggered during the following cases:

-   Periodic scheduling: A policy-based approach where Discovery is triggered on a periodic basis.
-   On CI delete: When the computer or server CI record is deleted.
-   MID Server cycle: When the MID Server goes down and comes back up.
-   Target host cycle: When the target host goes down and comes back up.
-   Network break: When there is a break in the network link to the target.

**Note:** Discovery is triggered for those agents whose hosts are already present. Agents whose hosts are not present are discovered through ACC-F.

## ACC-V checks and policies

The ACC-V assets are stored as Agent plugins with the main entry point \[acc\_visibility\_main\] and other modules for OS families. There is one main system Discovery Check definition, called **Enhanced Discovery**, which is used by the **Enhanced Discovery Policy**. This ACC-V policy runs off a schedule, which is defaulted to 24 hours \(86,400 seconds\). This policy configuration is synced to all agents as defined in the ACC-V policy.

When the payload is returned from the MID Server to the instance, the ACC-V Check Type, **EnhancedDiscovery**, delegates tasks to the EnhancedDiscoveryHandler script include provided by ACC-V. The script contains logic to process the data from the check and handles tasks such as:

-   Data transformation into an identification and reconciliation engine \(IRE\) compatible payload
-   Non-CI data reconciliation \(cmdb\_running\_processes, cmdb\_tcp\_connections, and so on\)

The ACC-V Check Definition, **Enhanced Discovery**, is initiated by the ServiceNow Instance. Then, an ECC Queue record with topic, MonitoringProbe, is created on the output queue with relevant Check information. The MID Server then processes the check by sending a message to the ACC via WebSocket over TLS.

During this time, the MID Server also serves any relevant Assets or Plugins that the ACC requests, making sure it is relevant to the particular Operating System, platform, OS version, and architecture on which the ACC is running.

You can edit and modify all parts of the ACC-V application including check type, policy, and check definition. See [Checks and policies](checks-policies.md) for more information.

## Virtual machines and cloud instances

ACC-V associates a target, discovered via Discovery, with a pre-existing virtual machine \(VM\) Instance CIs. ACC-V associates the discovered CI record with any pre-existing VM Instance record or Cloud Server Instance record with appropriate CMDB relationships.

The following variants of virtualization and cloud server vendors are supported for ACC-V:

-   vCenter
-   Amazon AWS Cloud
-   Google \(GCP\)
-   Microsoft Azure


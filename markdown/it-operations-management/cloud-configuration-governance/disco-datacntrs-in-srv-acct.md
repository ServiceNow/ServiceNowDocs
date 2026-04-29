---
title: Discover all datacenters in a service account on-demand
description: After you set up a service account, run Discovery to populate the datacenters in the account.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional Cloud Provisioning and Governance setup on day 2, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Discover all datacenters in a service account on-demand

After you set up a service account, run Discovery to populate the datacenters in the account.

## Before you begin

-   A cloud account must exist with service accounts and associated datacenters. You must run on-demand Discovery to discover datacenters before you can schedule Discovery.
-   Use the Cloud Discovery Workspace, and at least version 1.15 of Discovery and Service Mapping Patterns from the ServiceNow Store.

Role required: sn\_cmp.cloud\_admin

## About this task

Cloud providers often use different names for accounts, regions, and credential settings. Because the ServiceNow application supports several cloud providers, the app uses general-purpose names for the settings. In the Google Cloud Platform, the region-specific containers for virtual resources are called regions. In ServiceNow cloud data model, regions are called datacenters or logical datacenters \(LDCs\). The term logical is used to reinforce the idea that Cloud Provisioning is provider-agnostic. All infrastructure or applications that are deployed using Cloud Provisioning are associated with a datacenter.

You can run Discovery on-demand.

**Important:** Use Cloud Discovery Workspace \(CDW\) to run the discovery schedule. The discover datacenter UI action is legacy and the preferred approach is to setup schedules from CDW.

## Procedure

1.  Navigate to the Cloud Service Accounts \[cmdb\_ci\_cloud\_service\_account\_list\] table.

    For more information on directly navigating to a table, see [Navigate directly to a table](https://www.servicenow.com/docs/access?context=t_NavigateDirectlyToATable&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

2.  Select the service account whose LDCs you want to discover.

3.  Select the **Create Discovery Schedule** related link.

4.  Select **Next**.

5.  Select **Refresh Datacenters**.

6.  Select **Cancel**.

7.  Select the service account whose LDCs you tried to discover.

    On successful datacenter discovery, the Datacenter Discovery status field is set to `YYYY-MM-DD HH:MM:SS: Completed … Reload this form to see an updated datacenter list`.


## Result

The discovered datacenters appear in the Logical Datacenters related list.

**Related topics**  


[Logs for horizontal discovery](../../discovery/reference/r_DiscoveryLog.md#)


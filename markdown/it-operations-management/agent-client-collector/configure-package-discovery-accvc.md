---
title: Configure portable software discovery in Agent Client Collector for Visibility Content
description: Configure portable software the Agent Client Collector for Visibility Content \(ACC-VC\) agent discovers by updating the config table. This ensures that only portable software that was configured is searched for and discovered.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/configure-package-discovery-accvc.html
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Discover portable software installed by package managers, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure portable software discovery in Agent Client Collector for Visibility Content

Configure portable software the Agent Client Collector for Visibility Content \(ACC-VC\) agent discovers by updating the config table. This ensures that only portable software that was configured is searched for and discovered.

## Before you begin

Ensure that you have access to the ACC-VC scoped app in your ServiceNow instance.

Role required: discovery\_admin

## About this task

Software discovery is governed by the Portable Software Package Discovery \(**sn\_acc\_vis\_content\_process\_based\_sw\_config**\) table. When you add or remove entries from this table, the changes are delivered to ACC agents on their next check cycle, and an agent rebuild is not needed.

## Procedure

1.  Enter **sn\_acc\_vis\_content\_process\_based\_sw\_config.list** into the navigation panel.

    The **Process Based Software Discovery Configurations** page opens.

2.  Configure the following fields for each software name you want the system to discover.

    |Field|Description|
    |-----|-----------|
    |Software name|The name to match. This is either the process's own name, or the script/package name that shows up in the interpreter's command line \(for example, openclaw\). Not case-sensitive.|
    |Description|Enter descriptive text indicating why you're searching for the software.|
    |Active|Select the check box for the software to be pushed to the agent.|

3.  Select **Update**.

4.  Activate the **Software DIscovery via Running Process** policy.

    The discovered software displays in the Software installation \(**cmdb\_sam\_sw\_install**\) table with the following fields discovered:

    |Field|Description|
    |-----|-----------|
    |Name|The name of the software you configured in the Process Based Software Config \(**sn\_acc\_vis\_content\_process\_based\_sw\_config**\) table.|
    |Version|The software version. If not discoverable during initial detection, the agent tries again every 5 minutes.|
    |Vendor/Publisher|The vendor/publisher of the software. If not discoverable during initial detection, the agent tries again every 5 minutes.|
    |Install location|The directory that the discovered software resides in.|
    |Status|When software is successfully discovered, value is **install ok installed**.|


**Parent Topic:**[Discover portable software installed by package managers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/accvc-package-discovery.md)

**Related topics**  


[Discover portable software installed by package managers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/agent-client-collector/accvc-package-discovery.md)


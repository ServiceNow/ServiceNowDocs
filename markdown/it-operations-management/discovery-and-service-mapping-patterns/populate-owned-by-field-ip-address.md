---
title: Reference the main CI on discovered IP addresses
description: Populate the Owned By Configuration Item field on discovered IP address records with a direct reference to the main CI, instead of requiring a dot-walk through the network adapter. Populating the reference is supported only for AIX Server discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/populate-owned-by-field-ip-address.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-08-18"
reading_time_minutes: 1
keywords: [IP address discovery, cmdb\_ci\_ip\_address, owned by configuration item, AIX discovery]
breadcrumb: [Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Reference the main CI on discovered IP addresses

Populate the **Owned By Configuration Item** field on discovered IP address records with a direct reference to the main CI, instead of requiring a dot-walk through the network adapter. Populating the reference is supported only for AIX Server discovery.

## Before you begin

Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.

Role required: discovery\_admin

## About this task

By default, the relationship between a discovered IP address and its main CI is available only through a dot-walk via the Network Adapter \[cmdb\_ci\_network\_adapter\] table \(nic.configuration\_item\). When the **add.owned.by.attribute** system property is set to true, the **Owned By Configuration Item** field on the IP Address \[cmdb\_ci\_ip\_address\] table is populated with a direct reference to the main CI. The default value is false. When enabled, any existing **Owned By Configuration Item** references are cleared and recreated for the discovered IP addresses.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** column, search for `add.owned.by.attribute`.

3.  Select the **add.owned.by.attribute** system property.

4.  In the **Value** field, enter `true`.

    To revert to the default behavior and leave the **Owned By Configuration Item** field unpopulated, set the value to `false`.

5.  Select **Update**.


## What to do next

Run Discovery again to apply the change.

**Parent Topic:**[Discovery patterns used by ITOM Visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/c_MappingPatternsCustomization.md)

**Previous topic:**[Enable Oracle Wallet authentication for discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/enable-oracle-wallet-authentication.md)

**Next topic:**[AI Agent Topology Mapping reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/ai-agent-topology-mapping-reference.md)

**Related topics**  


[AIX server discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/itom-visibility/r_DataCollDiscoAIXComputers.md)


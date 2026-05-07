---
title: Configure Cisco Meraki allowlists
description: Configure connector definitions to limit polling to specific Cisco Meraki Organizations.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Configure Cisco Meraki SGC, Configure Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure Cisco Meraki allowlists

Configure connector definitions to limit polling to specific Cisco Meraki Organizations.

## Before you begin

Role required: tsom\_visibility\_admin

## About this task

You can now configure an allowlist of Cisco Meraki Organizations on each connector instance to limit polling to specific entities. Use multiple connector instances with disjoint allowlists to distribute collection across MID Servers and avoid polling interval overruns in large-scale deployments. An empty allowlist preserves existing behavior. When populated, only listed entities are included in the polling scope; all others are silently excluded.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Definitions**.

2.  Search for Meraki in the search box.

3.  Select the desired connector from the list, then the desired Connector Instance.

4.  Enter the organization names in the **organizationsToWhitelist** field in the**Connector Instance Values** section.

    The following table describes the **organizationsToWhitelist** field.

    |Field|Description|
    |-----|-----------|
    |Field Name|organizationsToWhitelist|
    |Field Type|Single-line text field|
    |Format|Comma-separated list of organization names, for example: \[ABC, DEF\]|
    |Matching|Exact string match against the name returned by the source system API|
    |Default|Empty \(connector polls all organizations\)|

    ![Screenshot showing organizationsToWhitelist field in connector configuration](../images/whitelist.png)

5.  Select **Update** to save.

    The connector applies these values at each polling cycle.



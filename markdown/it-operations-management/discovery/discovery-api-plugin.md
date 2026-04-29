---
title: Discovery API plugin
description: The Discovery API plugin provides APIs for scoped applications and is loaded when the Discovery plugin is activated.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery API plugin

The Discovery API plugin provides APIs for scoped applications and is loaded when the Discovery plugin is activated.

Details about these [Discovery API methods](https://developer.servicenow.com/app.do#!/api_doc?v=paris&id=c_DiscoveryAPIScopedAPI) are available on the ServiceNow® Developer Site. They are listed here by class.

**Note:** Java API methods are not customizable.

-   **DiscoveryAPI - Scoped**

    The methods in this class launch a quick Discovery of a single IPv4 address and return summaries of previously launched Discovery statuses for a single CI or for all scanned CIs. A MID Server is selected automatically, based on the IP address provided or the application specified.

    -   **discoverIpAddress\(\)**: Discovers a single IPv4 address.
    -   **reportCiIpAddressStatus\(\)**: Returns a summary of a configuration item's Discovery status given the specific status sys\_id and IPv4 address.
    -   **reportCiStatus\(\)**: Returns a summary of a CI Discovery status given a specific Discovery Status sys\_id.
-   **ReportCiStatusOutputJS**

    The methods are getters that return specific object properties for the DiscoveryAPI **reportCiIpAddressStatus** method and then convert the information into a JSON string.

    -   **getCiOperationStatus\(\)**: Used to return the state of the scanned CI.
    -   **getCmdbCI\(\)**: Used to return the value in the cmdb\_ci field from the discovery\_device\_history table for the CI being scanned.
    -   **getDiscoveryState\(\)**: Used to return the value from the **State** field in the Discovery Status \[discovery\_status\] table.
    -   **getIpAddress\(\)**: Used to return the value from the source field in the discovery\_device\_history table for the CI being scanned.
    -   **getIssues\(\)**: Used to return the value from the issues field in the discovery\_device\_history table for the CI being scanned.
    -   **getIssuesLink\(\)**: Used to return the value from the issues\_link field in the discovery\_device\_history table for the CI being scanned.
    -   **toJson\(\)**: Used to serialized the **ReportCiStatusOutputJS** object.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)


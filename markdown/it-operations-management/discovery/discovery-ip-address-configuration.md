---
title: Discovery IP address configuration
description: Use one or more of these methods in any combination to define the network or network segment for Discovery to query. You can include or exclude specific IP ranges from your query.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/discovery-ip-address-configuration.html
release: australia
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2026-07-25"
reading_time_minutes: 4
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery IP address configuration

Use one or more of these methods in any combination to define the network or network segment for Discovery to query. You can include or exclude specific IP ranges from your query.

**Note:** If you don't know the IP addresses in the network, run [Network discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_NetworkDiscovery.md) first to determine the IP networks. Then, convert the IP networks into IP address range sets.

If you have integrations which populate sys\_metadata and sys\_update\_xml tables, make sure to clear the update and metadata records after the discovery\_range\_item or discovery\_range\_item\_ip import occurs.

**Important:** IPv6 addresses aren't supported for IP address range or IP network.

There are three types of IP collections:

<table id="table_qqv_ll3_1y"><thead><tr><th>

IP collection type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP address list

</td><td>

Use IP address lists to add individual addresses to query. These addresses aren't included in any existing IP range or IP network. You can enter the IP address of the device or a host name \(DNS name\). If you enter a host name, it must be [mapped to an IP address](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_MapIPAddressToDNSName.md).

</td></tr><tr><td>

IP address range

</td><td>

You can define arbitrary ranges of IP addresses to query. This process is a good way to include selected segments of a network or subnet. However, Discovery has no way of knowing if the IP range includes addresses for private networks or broadcast addresses, and scans all the addresses in the range. If the network and broadcast addresses are included, then the results are inaccurate. Discoveries configured to detect IP networks are more accurate than discoveries configured for IP address ranges. Only those IP addresses in your range that are reserved for manageable devices on the public network should be included.

 **Note:** To avoid performance issues, limit Discovery schedules to a maximum range of /16 \(approximately 65,536 IPs\). For better performance, consider splitting the range into smaller segments.

</td></tr><tr><td>

IP network

</td><td>

You can also scan an entire IP network. [An IP network](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_NetworkDiscovery.md) includes the range of available IP addresses in that network. The scan also includes the network address \(the lowest address in the range\) and the broadcast address \(the highest address in the range\). After you [run network discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_NetworkDiscovery.md), [convert the IP networks that were found into range sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/c_NetworkDiscovery.md)for use in discovering other devices.

 IP networks are represented in CIDR notation. Examples of CIDR notation include:

-   192.168.0.0/24
-   10.11.128.192/26

 Discovery will not scan the network or broadcast addresses for a network. The equivalent ranges for the two networks are:

-   192.168.0.1 – 192.168.254
-   10.11.128.193 – 10.11.128.254

 To avoid introducing errors from broadcast addresses, configure Discovery to exclude them by using IP network definitions in CIDR notation. Discovery automatically avoids scanning network and broadcast addresses when using IP networks.

 Including broadcast addresses in Discovery scans can lead to significant errors in the data, such as redundant or invalid device entries. By excluding broadcast addresses, Discovery helps prevent these errors.

 This built-in control makes IP networks the best method of defining which IP address ranges to query.

</td></tr></tbody>
</table>After you define your IP collections, use Discovery generic attributes to automatically set field values on CIs discovered within a schedule, range set, or IP address range. For example, assign different locations to CIs based on the IP range they were discovered in. For more information, see [Define CI field attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/define-ci-attributes.md).

For more information about viewing and managing your IP collections, see [Discovery Admin Workspace IP inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-ip-inventory.md).

**Related topics**  


[IP address selection properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r_CIIPAddressSelection.md)

[Add IP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-add-ip-data.md)

[Add IP data to a range set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/daw-add-ip-range-set.md)

[Create a Quick IP range for a Discovery schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_CreateAQuickRange.md)

[Import IP ranges into Discovery schedules with import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/t_ImportIPRanges.md)

[Exclude IP ranges from a Discovery range set](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/exclude-ip-ranges.md)

[Use Global Excludes List for IP addresses and ranges](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/global-exlude-list.md)


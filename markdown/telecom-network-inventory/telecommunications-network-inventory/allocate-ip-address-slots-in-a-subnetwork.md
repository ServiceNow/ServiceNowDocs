---
title: Allocate IP address slots in a subnetwork
description: Allocate IP address slots in bulk from an IP Subnetwork. The system creates one allocated IP record for each address in the subnetwork’s CIDR. Reserved addresses \(the first and last for IPv4, or the first for IPv6\) are flagged automatically and cannot be promoted to IP Address records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 3
breadcrumb: [Manage IP addresses, Inventory number allocation, Define inventory records, Use, Telecommunications Network Inventory]
---

# Allocate IP address slots in a subnetwork

Allocate IP address slots in bulk from an IP Subnetwork. The system creates one allocated IP record for each address in the subnetwork’s CIDR. Reserved addresses \(the first and last for IPv4, or the first for IPv6\) are flagged automatically and cannot be promoted to IP Address records.

## Before you begin

Before you begin:

-   Install all required Telecommunications Network Inventory plugins.
-   Role required: `core.dc_ops_agent, sn_ni_core.inventory_agent`
-   The IP Subnetwork must be in an active state \(Life Cycle Stage = Operational and Life Cycle Stage Status = In Use\).
-   The subnetwork must not already have allocated IP records. To re-allocate, delete the existing allocated IP records first.
-   The subnetwork’s CIDR must contain at most 64 addresses. This means the prefix length must be /26 or longer for IPv4, or /122 or longer for IPv6. To learn more, see [Bulk allocation limits for allocated IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/bulk-allocation-limits-for-allocated-ip-addresses.md).

## About this task

Allocating IP address slots creates one Allocated IP Address record for every address in the subnetwork's CIDR. Each record carries an Is Reserved flag, set automatically for protocol-reserved addresses. It also carries an Is Managed flag, set automatically once an IP Address record is created from the slot. The slot records form the inventory you draw from when creating individual IP Address records using the from allocated IPs method.

This task is the first step of the per-host allocation method. If you instead want to create a single IP Address record representing the subnetwork as a whole \(the at-subnet-level method\), do not run this task. See [Create an IP Address record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace** or **Service Operations Workspace**.

2.  Open the IP Subnetwork record.

    \(**Inventory Number Allocation** &gt; **IP Network Subnets** &gt; select the subnetwork.\)

3.  Select the **Allocated IP Address** tab.

4.  Open the three-dot menu in the top-right corner and select **Create Allocated IP Address Record**.

5.  In the confirmation dialog, review the number of addresses that will be created.

6.  Select **OK** to confirm.

    The system creates the allocated IP records and displays a confirmation banner.

7.  Review the allocated IP records on the **Allocated IP Address** tab.

    The tab count updates to reflect the number of records created. Each record displays the following fields:

    |Field|Description|
    |-----|-----------|
    |Name|The address value.|
    |IP Address|The address value.|
    |Is Reserved|True for addresses that cannot be promoted to IP Address records \(first and last for IPv4; first only for IPv6\). False otherwise.|
    |Is Managed|False until an IP Address record is created from this slot. Not user-editable.|
    |Managed Network|Inherited from the parent subnetwork.|


## What to do next

Create IP Address records from one or more of the allocated IP slots. See [Create IP Address records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md).

**Parent Topic:**[Manage IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.md)

**Related topics**  


[Create IP Address records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)

[Bulk allocation limits for allocated IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/bulk-allocation-limits-for-allocated-ip-addresses.md)

[Allocated IP Address form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/allocated-ip-address-form.md)

[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)


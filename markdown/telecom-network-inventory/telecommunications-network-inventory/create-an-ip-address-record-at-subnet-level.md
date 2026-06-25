---
title: Create an IP Address record at subnet level
description: Create a single IP Address record that represents an entire IP Subnetwork as one Configuration Item. The IP Address record uses the subnetwork’s CIDR as its value, rather than a single host address. This method is used when the subnetwork is bound to a service, port, customer, or interface as a single entity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 3
breadcrumb: [Manage IP addresses, Inventory number allocation, Define inventory records, Use, Telecommunications Network Inventory]
---

# Create an IP Address record at subnet level

Create a single IP Address record that represents an entire IP Subnetwork as one Configuration Item. The IP Address record uses the subnetwork’s CIDR as its value, rather than a single host address. This method is used when the subnetwork is bound to a service, port, customer, or interface as a single entity.

## Before you begin

Before you begin:

-   Install all required Telecommunications Network Inventory plugins.
-   Role required: `core.dc_ops_agent, sn_ni_core.inventory_agent`
-   The IP Subnetwork must be in an active state \(Life Cycle Stage = Operational and Life Cycle Stage Status = In Use\).
-   The IP Subnetwork must not have any existing IP Address records created from allocated IPs. If it does, delete those records first, or use this method on a different subnetwork.

## About this task

This task is the at-subnet-level allocation method. The system creates one IP Address record whose value is the subnetwork’s CIDR \(for example, 10.10.1.0/26\). The record represents the subnetwork as a single CMDB Configuration Item and is linked to the subnetwork through a Contains relationship.

The two IP allocation methods \(from allocated IPs and at subnet level\) are mutually exclusive on a given subnetwork. Once the first IP Address record is created by either method, the other method is locked for that subnetwork until all IP Address records are deleted. To learn more, see [CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md).

This method does not require the subnetwork’s allocated IP records to be created first. The IP Address record is bound directly to the subnetwork, not to any individual address slot.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace** or **Service Operations Workspace**.

2.  Open the IP Subnetwork record.

    \(**Inventory Number Allocation** &gt; **IP Network Subnets** &gt; select the subnetwork.\)

3.  Open the three-dot menu in the top-right corner of the record.

4.  Select **Create IP Address Record**.

    **Note:** This menu item is separate from the Create IP Address Records button on the Allocated IP Address tab.

5.  In the confirmation dialog, review the subnetwork details.

6.  Select **OK** to confirm.

    The system creates the IP Address record and displays a confirmation banner:

    ```
    IP Address record created: {Name} ( {CIDR} )
    ```

7.  Review the new IP Address record on the **IP Address** tab.

    The tab count updates to 1. The IP Address record’s fields:

    |Field|Value|
    |-----|-----|
    |Name|The subnetwork’s CIDR \(for example, 10.10.1.0/26\).|
    |IP Address|The subnetwork’s CIDR.|
    |IP version|IPv4 or IPv6, matching the subnetwork’s protocol.|


## Result

Effect on the data model for an IP Address record created by this task, the system writes one CMDB relationship: IP Subnetwork → Contains → IP Address — links the IP Address record to the parent subnetwork. The system does not write a Manages relationship, because the IP Address record is not bound to a specific allocated IP slot. To learn more, see.

## What to do next

Bind the IP Address record to the service, port, customer, or interface it represents by populating the Owned By Configuration Item field on the record.

**Parent Topic:**[Manage IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.md)

**Related topics**  


[Create IP Address records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)

[CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md)

[IP Address form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-address-form.md)

[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)


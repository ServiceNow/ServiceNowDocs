---
title: Create IP Address Records from allocated IPs
description: Create one or more IP Address records by selecting allocated IP slots and promoting them to active CMDB Configuration Items.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.html
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 4
breadcrumb: [Manage IP addresses, Inventory number allocation, Defining inventory records, Use, Telecommunications Network Inventory]
---

# Create IP Address Records from allocated IPs

Create one or more IP Address records by selecting allocated IP slots and promoting them to active CMDB Configuration Items.

## Before you begin

Install all required [Model your workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-workflow.md) plugins.

The IP Subnetwork must contain allocated IP records. If it does not, see [Allocate IP Address Slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md).

The IP Subnetwork must not have an existing subnet-level IP Address record. If it does, delete that record first, or use the From allocated IPs method on a different subnetwork.

Role required: `core.dc_ops_agent, sn_ni_core.inventory_agent`

## About this task

This task is the per-host allocation method. The system creates one IP Address record for each selected allocated IP that is not reserved. Reserved addresses in the selection are skipped automatically and reported in the result banner.

The two IP allocation methods \(from allocated IPs and at subnet level\) are mutually exclusive on a given subnetwork. Once the first IP Address record is created by either method, the other method is locked for that subnetwork until all IP Address records are deleted. To learn more, see [CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace** or **Service Operations Workspace**.

2.  Open the IP Subnetwork record.

    \(**Inventory Number Allocation** &gt; **IP Network Subnets** &gt; select the subnetwork.\)

3.  Select the **Allocated IP Address** tab.

4.  Select the allocated IP records you want to promote to IP Address records:

    1.  Select the check box at the start of each row to select individual records.

5.  Select **Create IP Address Records**.

    The button is enabled only when one or more allocated IP records are selected.

6.  In the confirmation dialog, review the selection:

    ```
    Create IP Addresses for {N} selected Allocated IP(s)? (Reserved IPs will be skipped)
    ```

    The dialog confirms the number of records selected and notes that reserved addresses will be skipped automatically.

7.  Select **OK** to confirm.

    The system processes the selection and displays a result banner. The banner format depends on the outcome.

8.  Review the created IP Address records on the **IP Address** tab.

    The tab count updates to reflect the number of new records. Each IP Address record displays the following fields on its detail page:

    |Field|Description|
    |-----|-----------|
    |Name|The address value \(matches the IP Address field\).|
    |IP Address|The address value.|
    |IP version|IPv4 or IPv6, inherited from the parent subnetwork.|
    |Owned By Configuration Item|Optional reference to the CI that owns this address.|
    |Netmask|Optional.|

9.  Review the corresponding allocated IP records on the **Allocated IP Address** tab.

    The **Is Managed** flag on each promoted record is now selected.


## Result

The system writes two CMDB relationships for each IP Address record created by this task. The Manages relationship links the new record to its source allocated IP slot. The Contains relationship links it to the parent subnetwork.

The corresponding allocated IP record's **Is Managed** flag is set to selected automatically. If you later delete the IP Address record, both relationships are removed and the allocated IP slot's **Is Managed** flag is cleared. The slot itself is preserved and can be promoted again. For more information, see [CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md).

**Parent Topic:**[Manage IP addresses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/manage-ip-addresses.md)

**Related topics**  


[Create an IP Address Record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md)

[Allocate IP Address Slots in a subnetwork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/allocate-ip-address-slots-in-a-subnetwork.md)

[IP Address form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/ip-address-form.md)

[CMDB relationships for IP address records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.md)


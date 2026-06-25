---
title: Hierarchy rules for IP Subnetworks
description: These rules apply only when creating or updating an IP Subnetwork \(which always has a parent — either an IP Address Block or another IP Subnetwork\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/hierarchy-rules-for-ip-subnetworks.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Hierarchy rules for IP Subnetworks

These rules apply only when creating or updating an IP Subnetwork \(which always has a parent — either an IP Address Block or another IP Subnetwork\).

|Rule|Whats checked|Rejected example|Error message|
|----|-------------|----------------|-------------|
|Subnetwork falls within parent|The subnetwork’s CIDR is a strict subset of the parent’s range.|Parent 20.0.0.0/24, child 30.0.0.0/24|"Invalid CIDR: The current CIDR \( 30.0.0.0/24 \) is not within the parent range \( 20.0.0.0/24 \)"|
|Subnetwork more specific than parent|The subnetwork’s prefix is longer than the parent’s. The subnetwork can't be identical to the parent.|Parent 10.10.0.0/16, child 10.10.0.0/16|"IP Subnetwork cannot be identical to the Parent \( 10.10.0.0/16 \)"|
|Unique under same parent|No other subnetwork under the same parent has the same CIDR.|Sibling 10.0.0.0/26 already exists under parent 10.0.0.0/20; new subnetwork attempts 10.0.0.0/26|"Subnet CIDR 10.0.0.0/26 already exists under the same Parent \( 10.0.0.0/20 \)"|

## Overlap advisory

When a subnetwork’s CIDR overlaps with — but is not identical to — an existing sibling under the same parent, the system displays a warning but does not block the save. The user can acknowledge the warning and continue.

Warning text:

```
Subnet CIDR ( {new CIDR} ) overlaps with existing CIDR ( {existing CIDR} ) under the same Parent ( {parent CIDR} ). Do you want to continue ?
```

## Uniqueness at top level — IP Address Blocks

The hierarchy rules above apply to IP Subnetworks. An IP Address Block is a top-level record without a parent block, and its uniqueness is scoped by Managed Network rather than by a parent.

-   If the IP Address Block has a Managed Network value, the CIDR must be unique within that Managed Network. The same CIDR may exist in different Managed Networks.
-   If the IP Address Block has no Managed Network, the CIDR must be unique across all IP Address Blocks that have no Managed Network.

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[CIDR validation rules for IP Address Blocks and IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.md)

[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)

[IP Subnetwork form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-subnetwork-form.md)

[IP Address Block form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-address-block-form.md)


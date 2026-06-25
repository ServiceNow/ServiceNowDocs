---
title: CMDB relationships for IP address records
description: When an IP Address record is created, the system writes one or two relationship records to the CMDB relationship table \(cmdb\_rel\_ci\). The relationships created depend on which allocation method was used to create the IP Address record. The relationships are visible on the IP Address record’s Related Items panel and in the Dependency View.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/cmdb-relationships-for-ip-address-records.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [IP address management, Inventory number allocation, Explore, Telecommunications Network Inventory]
---

# CMDB relationships for IP address records

When an IP Address record is created, the system writes one or two relationship records to the CMDB relationship table \(cmdb\_rel\_ci\). The relationships created depend on which allocation method was used to create the IP Address record. The relationships are visible on the IP Address record’s Related Items panel and in the Dependency View.

## Relationships created by each allocation method

**From allocated IPs \(per-host method\).** When an IP Address record is created from a selected allocated IP, the system writes two relationships:

|Relationship type|Parent|Child|
|-----------------|------|-----|
|Manages :: Managed by|IP Address record|Allocated IP Address record|
|Contains :: Contained by|IP Subnetwork record|IP Address record|

The Manages relationship links the new IP Address record to the allocated IP slot it was created from. The Contains relationship links the IP Address record to the subnetwork it belongs to.

**At subnet level \(subnetwork-as-a-CI method\).** When a single IP Address record is created for the subnetwork as a whole, the system writes one relationship:

|Relationship type|Parent|Child|
|-----------------|------|-----|
|Contains :: Contained by|IP Subnetwork record|IP Address record|

No Manages relationship is created because the IP Address record is not linked to any specific allocated IP slot.

## Effect of deletion

When an IP Address record is deleted, the relationships it participated in are also removed:

-   For records created from allocated IPs, the deletion removes both the Manages relationship and the Contains relationship. The allocated IP slot’s Is Managed flag flips back to False automatically. The slot itself is preserved and remains available for reuse.
-   For records created at subnet level, the deletion removes the Contains relationship.

## Where relationships appear in the workspace

-   **Related Items panel.** Each IP Address record displays its parent records under Related Items on the record’s detail page.
-   **Dependency View.** From the IP Address record’s three-dot menu, selecting Dependency View opens a graphical visualisation showing the IP Address record and its parent records as nodes connected by their relationship types.

**Related topics**  


[Create IP Address records from allocated IPs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-ip-address-records-from-allocated-ips.md)

[Create an IP Address record at subnet level](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-record-at-subnet-level.md)

[IP address inventory management data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-address-inventory-management-data-model.md)


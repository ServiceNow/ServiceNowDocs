---
title: CIDR validation rules for IP Address Blocks and IP Subnetworks
description: The CIDR value entered on an IP Address Block or IP Subnetwork record is validated when the record is saved. Invalid CIDR values are rejected with an inline error message; the record cannot be saved until the value passes all rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/cidr-validation-rules.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2026-06-25"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# CIDR validation rules for IP Address Blocks and IP Subnetworks

The CIDR value entered on an IP Address Block or IP Subnetwork record is validated when the record is saved. Invalid CIDR values are rejected with an inline error message; the record cannot be saved until the value passes all rules.

The same validation applies to both IPv4 and IPv6, with the protocol-specific differences noted in each rule.

## Format and value rules

These rules apply to every CIDR value, whether on an IP Address Block or an IP Subnetwork.

|Rule|What’s checked|Rejected example|Error message|
|----|--------------|----------------|-------------|
|Valid CIDR format|The value is well-formed CIDR notation: an IP address, a slash, and a prefix length.|192.168.1.0 \(no prefix\)|"Invalid CIDR format: Valid CIDR should contain exactly one slash" equivalent message for IPv6.|
|Valid prefix range|IPv4 prefix is 0–32. IPv6 prefix is 0–128.|10.0.0.0/55|"Invalid CIDR. Format prefix must be a number between 1 and 32 inclusive"|
|Valid IP address|The address portion is a syntactically valid IPv4 or IPv6 address.|192.168.1.300/24 \(octet &gt; 255\)|"IP address is not valid"|
|Host bits zero|The address portion is the network address — all host bits are zero relative to the prefix.|172.16.5.10/24 \(should be 172.16.5.0/24\)|"Invalid CIDR format: Must be a valid IPv4/IPv6 network address matching the prefix"|

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Hierarchy rules for IP Subnetworks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/hierarchy-rules-for-ip-subnetworks.md)

[Create an IP Address Block record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-address-block-record.md)

[Create an IP Subnetwork record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/create-an-ip-subnetwork-record.md)

[IP Address Block form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-address-block-form.md)

[IP Subnetwork form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/ip-subnetwork-form.md)


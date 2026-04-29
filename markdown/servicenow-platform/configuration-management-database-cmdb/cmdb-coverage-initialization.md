---
title: CMDB Coverage initialization
description: The initialization activity processes historical IP address data from your existing CMDB CIs and IPAM sources. Initialization establishes baseline coverage metrics before ongoing monitoring begins.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, CMDB Coverage, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Coverage initialization

The initialization activity processes historical IP address data from your existing CMDB CIs and IPAM sources. Initialization establishes baseline coverage metrics before ongoing monitoring begins.

## Initialization process

The initialization activity processes existing IP addresses from all configured CMDB CI classes \(as defined in the sn\_cmdb\_ip\_cov\_ci\_config table\). All IPv4 addresses are converted to binary format for faster matching, and IPv6 addresses are processed as is. Subsequently, the allocated IP addresses \(IPAM IP addresses\) are matched with the discovered CIs to determine the CMDB coverage status. Finally, relationships are created between the IPAM IP addresses and the discovered CIs.

The time required for the initialization process to finish depends on the volume of your data. The percentage of completion is displayed in the real-time progress tracker.

**Parent Topic:**[CMDB Coverage reference](../concept/cmdb-coverage-reference.md)


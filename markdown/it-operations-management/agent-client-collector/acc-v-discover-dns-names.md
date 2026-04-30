---
title: Discovering DNS names using push-based discovery
description: CMDB owners need CIs to contain all domain system names \(DNS\) associated with their system. Starting in ACC-V version 2.3.0, ACC-V can discover DNS name lists for Windows and Linux CIs.
locale: en-US
release: xanadu
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Agent Client Collector for Visibility, Agent Client Collector for Visibility, Agent Client Collector, IT Operations Management]
---

# Discovering DNS names using push-based discovery

CMDB owners need CIs to contain all domain system names \(DNS\) associated with their system. Starting in ACC-V version 2.3.0, ACC-V can discover DNS name lists for Windows and Linux CIs.

When discovering DNS names associated with systems, the following occurs.

-   network\_adapters.rb is used to populate the DNS name for all the IP addresses using OSquery. \(There is no limit.\)
-   Nslookupcommand is used to get the DNS name for all IP addresses.

    **Note:** Nslookup must be configured on the target.


This creates a relationship of **Owns::Owned by** between the CI and the DNS names.

This information is then populated into the \[cmdb\_ci\_dns\_name\] table.

**Parent Topic:**[Using Agent Client Collector for Visibility](acc-v-using-agent-client-collector-for-visibility.md)


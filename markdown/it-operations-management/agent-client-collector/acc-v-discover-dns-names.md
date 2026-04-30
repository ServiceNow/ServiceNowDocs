---
title: Discovering DNS names using push-based discovery
description: CMDB owners need CIs to contain all domain system names \(DNS\) associated with their system. Starting in Agent Client Collector for Visibility - Content \(ACC-VC\) version 2.3.0, ACC-VC can discover DNS name lists for Windows and Linux CIs.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Agent Client Collector, Agent Client Collector for Visibility, ACC for Visibility]
breadcrumb: [Using Agent Client Collector for Visibility - Content, Agent Client Collector for Visibility - Content, Agent Client Collector, IT Operations Management]
---

# Discovering DNS names using push-based discovery

CMDB owners need CIs to contain all domain system names \(DNS\) associated with their system. Starting in Agent Client Collector for Visibility - Content \(ACC-VC\) version 2.3.0, ACC-VC can discover DNS name lists for Windows and Linux CIs.

When discovering DNS names associated with systems, the following occurs.

-   network\_adapters.rb is used to populate the DNS name for all the IP addresses using OSquery. \(There is no limit.\)
-   Nslookupcommand is used to get the DNS name for all IP addresses.

    **Note:** Nslookup must be configured on the target.


This creates a relationship of **Owns::Owned by** between the CI and the DNS names.

This information is then populated into the \[cmdb\_ci\_dns\_name\] table.

**Parent Topic:**[Using Agent Client Collector for Visibility - Content](acc-v-using-agent-client-collector-for-visibility.md)


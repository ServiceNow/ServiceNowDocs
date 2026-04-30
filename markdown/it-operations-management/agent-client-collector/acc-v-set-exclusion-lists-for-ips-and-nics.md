---
title: Setting exclusion lists for IPs and NICs
description: Agent Client Collector for Visibility - Content \(ACC-VC\) version 1.3.0 supports exclusion list for IPs and Network Interface Controllers \(NICs\) with a flexible mechanism for filtering out values for IPs and or NICs when creating or updating the host CI and related items.
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

# Setting exclusion lists for IPs and NICs

Agent Client Collector for Visibility - Content \(ACC-VC\) version 1.3.0 supports exclusion list for IPs and Network Interface Controllers \(NICs\) with a flexible mechanism for filtering out values for IPs and or NICs when creating or updating the host CI and related items.

The property \[**sn\_acc\_visibility.network\_adapter\_exclusion\_list**\] contains the list of regular expressions for the names and IP addresses that are excluded in the Network Adapter and IP Address tables. The value of this property is comma-separated regular expressions. Make sure that there is no comma in the regex and nic and ip\_addr should be in different lines.

Sample format of the value should be:

-   nic = nameRegex1, nameRegex2, nameRegex3
-   ip\_addr = IPRegex1, IPRegex2

**Parent Topic:**[Using Agent Client Collector for Visibility - Content](acc-v-using-agent-client-collector-for-visibility.md)


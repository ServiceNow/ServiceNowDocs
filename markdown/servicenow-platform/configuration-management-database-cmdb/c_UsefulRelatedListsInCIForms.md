---
title: Useful related lists in CI forms
description: By default, the forms that display manageable configuration items \(CI\) - computers, printers, network gear, uninterruptible power supplies \(UPS\), and power distribution units \(PDU\) - provide a number of related lists for the form.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Useful related lists in CI forms

By default, the forms that display manageable configuration items \(CI\) - computers, printers, network gear, uninterruptible power supplies \(UPS\), and power distribution units \(PDU\) - provide a number of related lists for the form.

The following related lists are common to all forms for manageable CIs.

-   Network Adapters - Displays all the NICs installed on a CI.
-   CI IPs - Displays all the IP addresses on this CI:
    -   Computers \(workstations, laptops using various macOS and Windows operating systems\)
    -   Windows servers
    -   Linux servers
    -   AIX servers
    -   Solaris servers
    -   Devices discovered through SNMP.
-   DNS Names for CIs - Displays all the DNS names on a CI.

The IP version information appears in all IP address related lists and forms.

**Note:** Since all paths here click into the **IP Address to DNS Names** list that associates an IP address with a DNS name, this part of the common flow was not added to the tree structure.

## Discovery source

A table called Source \[sys\_object\_source\] stores information identifying the source of a discovery \(by ServiceNow Discovery or another product\), the ID of that source, and the date/time of the last scan. To view this information, [configure a CI form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and add the **Sources** related list.

This table is populated automatically when the [Discovery plugin](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) is enabled.


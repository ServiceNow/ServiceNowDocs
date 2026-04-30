---
title: Block list entry exceptions for the Check Point NGTP integration
description: There are restrictions for adding Block List entries to Block Lists. If duplicate, compatibility, or CIDR \(Classless Inter-Domain Routing\) conflicts exist when you try to add Block List entries to Block Lists, error messages are displayed that help you resolve these errors.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with block lists, Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Block list entry exceptions for the Check Point NGTP integration

There are restrictions for adding Block List entries to Block Lists. If duplicate, compatibility, or CIDR \(Classless Inter-Domain Routing\) conflicts exist when you try to add Block List entries to Block Lists, error messages are displayed that help you resolve these errors.

## Compatibility exception

Each Block List only accepts entries that are compatible with its observable type. If you create a Domain Block List and you try to attach an IP address observable to it, an incompatible error message is displayed. For example, a domain Block List can only accept domain observables, as illustrated in the following figure.

![Compatibility exception](../image/list-entry-exceptions.png "Block List form with compatibility errors")

## Duplication exception

An observable cannot be activated on multiple Block Lists of the same observable type. If a URL observable is already activated on a URL Block List, and you try to activate the same observable on a Phishing URL Block List, a duplication error message is displayed.

![Duplication exception](../image/duplication-exception.png)

## CIDR \(Classless Inter-Domain Routing\) exception

If you attempt to attach a single IP address to an allow list, and this IP address is part of a CIDR observable already on a Block list/Allow list, a CIDR conflict error is displayed. This error indicates that the single IP address is already included on the Block list or allow list as part of the CIDR observable. For example, 192.168.24.25 is part of the CIDR block 192.168.0.0/22.

![CIDR exception](../image/cidr-exception.png)


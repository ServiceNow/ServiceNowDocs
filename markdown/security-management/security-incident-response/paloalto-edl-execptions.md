---
title: EDL entry exceptions for Palo Alto Networks Next-Generation Firewall
description: There are restrictions for adding External Dynamic List \(EDL\) entries to EDLs. If duplicate, compatibility, or CIDR \(Classless Inter-Domain Routing\) conflicts exist when you try to add EDL entries to EDLs, error messages are displayed that help you resolve these errors.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# EDL entry exceptions for Palo Alto Networks Next-Generation Firewall

There are restrictions for adding External Dynamic List \(EDL\) entries to EDLs. If duplicate, compatibility, or CIDR \(Classless Inter-Domain Routing\) conflicts exist when you try to add EDL entries to EDLs, error messages are displayed that help you resolve these errors.

## Compatibility exception

Each EDL only accepts entries that are compatible with its observable type. If you create a Domain EDL and you try to attach an IP address observable to it, an incompatible error message is displayed. For example, a domain EDL can only accept domain observables, as illustrated in the following figure.

![EDL entry Compatibility error message.](../image/4-30-ip-incompatible-error.png "Compatibility error")

## Duplication exception

An observable cannot be activated on multiple EDLs of the same observable type. If a URL observable is already activated on a URL EDL, and you try to activate the same observable on a Phishing URL EDL, a duplication error message is displayed.

![EDL entry duplicate error message.](../image/4-30-url-alreadyexists.png "Duplication error")

## CIDR \(Classless Inter-Domain Routing\) exception

If you attempt to attach a single IP address to an EDL, and this IP address is part of a CIDR observable already on an EDL, a CIDR conflict error is displayed. This error indicates that the single IP address is already included on the EDL as part of the CIDR observable. For example, `192.168.24.25` is part of the CIDR block `192.168.0.0/22`.



![EDL entry CIDR conflict message.](../image/4-30-cidr-ip.png)

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Approve EDL entries for Palo Alto Networks Next-Generation Firewall](../task/paloalto-apprv-edl-entries-sncr.md)

**Next topic:**[\(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall](../task/paloalto_edit_sectag_name.md)


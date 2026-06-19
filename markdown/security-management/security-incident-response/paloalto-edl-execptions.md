---
title: EDL entry exceptions for Palo Alto Networks Next-Generation Firewall
description: There are restrictions for adding External Dynamic List \(EDL\) entries to EDLs. If duplicate, compatibility, or CIDR \(Classless Inter-Domain Routing\) conflicts exist when you try to add EDL entries to EDLs, error messages are displayed that help you resolve these errors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/paloalto-edl-execptions.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# EDL entry exceptions for Palo Alto Networks Next-Generation Firewall

There are restrictions for adding External Dynamic List \(EDL\) entries to EDLs. If duplicate, compatibility, or CIDR \(Classless Inter-Domain Routing\) conflicts exist when you try to add EDL entries to EDLs, error messages are displayed that help you resolve these errors.

## Compatibility exception

Each EDL only accepts entries that are compatible with its observable type. If you create a Domain EDL and you try to attach an IP address observable to it, an incompatible error message is displayed. For example, a domain EDL can only accept domain observables.

## Duplication exception

An observable can't be activated on multiple EDLs of the same observable type. If a URL observable is already activated on a URL EDL, and you try to activate the same observable on a Phishing URL EDL, a duplication error message is displayed.

## CIDR \(Classless Inter-Domain Routing\) exception

If you attempt to attach a single IP address to an EDL, and this IP address is part of a CIDR observable already on an EDL, a CIDR conflict error is displayed. This error indicates that the single IP address is already included on the EDL as part of the CIDR observable. For example, `192.168.24.25` is part of the CIDR block `192.168.0.0/22`.

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto_integration.md)

**Previous topic:**[Approve EDL entries for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto-apprv-edl-entries-sncr.md)

**Next topic:**[\(Optional\) Edit the security tag name for Palo Alto Networks Next-Generation Firewall](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/paloalto_edit_sectag_name.md)


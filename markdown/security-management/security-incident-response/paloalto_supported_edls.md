---
title: Supported External Dynamic Lists for Palo Alto Networks Next-Generation Firewall
description: The ServiceNow Palo Alto Networks Next-Generation Firewall integration supports External Dynamic Lists \(EDLs\) that accept IP, URL, and domain observables.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Palo Alto Networks Next-Generation Firewall integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Supported External Dynamic Lists for Palo Alto Networks Next-Generation Firewall

The ServiceNow Palo Alto Networks Next-Generation Firewall integration supports External Dynamic Lists \(EDLs\) that accept IP, URL, and domain observables.

## Supported EDLs and observables

An External Dynamic List is a text file that is hosted on an external web server, which for this integration is the ServiceNow AI Platform instance. The Palo Alto Networks Next-Generation Firewall can then import objects — IP addresses, URLs, domains — included in the list and enforce policy. To enforce policy on the EDL entries, the list is referenced in a policy rule or profile.

This integration supports three types of EDLs:

-   IP \(This includes a single IP Address, as well as CIDR blocks \(ranges\) of addresses\).
-   URL
-   Domain

The following table lists descriptions of the observables supported by this integration and example formats for each type.

<table id="table_chs_vzf_5db"><thead><tr><th>

Observable

</th><th>

Example formats

</th><th>

Description

</th></tr></thead><tbody><tr><td>

IP Address

</td><td>

-   95.153.103.54 \(IPv4\)
-   \(IPv6\): 2001:00B8:130F:FE03:0000:09C0:080F:130B

</td><td>

Represents a single, distinct interface address.The integration supports IPv4, IPv6, and CIDR formats.

 Support for IP address observables includes CIDR \(Classless Inter-Domain Routing\) ranges, for example, 95.153.100.0/22.

 Note: An error message is displayed when you try to attach a single IP address to an EDL that you have already blocked as a part of a CIDR range. For example, the single address 95.153.103.54 is part of the CIDR range represented by 95.153.100.0/22 \(95.153.100.0-95.153.103.255\).

</td></tr><tr><td>

URL

</td><td>

-   www.example.com
-   www.example.com/article.html
-   example.com
-   \*.example.com

</td><td>

Wildcards are supported. The ServiceNow AI Platform reformats URL entries to comply with Palo Alto Networks EDL format requirements.

</td></tr><tr><td>

Domain

</td><td>

-   www.example.com
-   example.com
-   mail.example.com

</td><td>

Wildcards are not supported.

</td></tr></tbody>
</table>For more information about formatting guidelines and EDLs, see ["Formatting Guidelines for an External Dynamic List" in the PAN-OS 10.0 Administrator's Guide](https://docs.paloaltonetworks.com/pan-os/10-0/pan-os-admin/policy/use-an-external-dynamic-list-in-policy/formatting-guidelines-for-an-external-dynamic-list.html) on the Palo Alto Networks website.

**Parent Topic:**[Palo Alto Networks Next-Generation Firewall integration](../concept/paloalto_integration.md)

**Previous topic:**[Create the API account role for Palo Alto Networks Next-Generation Firewall](../task/paloalto-create-snrole.md)

**Next topic:**[Create an EDL for Palo Alto Networks Next-Generation Firewall](../task/palo_alto_config_edl.md)


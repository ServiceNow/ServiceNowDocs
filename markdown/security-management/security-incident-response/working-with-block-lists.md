---
title: Working with block lists
description: The ServiceNow Check Point Next Generation Threat Prevention Integration supports Block Lists that accept IP, URL, and Domain observables.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Check Point Next Generation Threat Prevention integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Working with block lists

The ServiceNow Check Point Next Generation Threat Prevention Integration supports Block Lists that accept IP, URL, and Domain observables.

ServiceNow configured block list is a csv file that is hosted on an external web server, which for this integration is the ServiceNow AI Platform instance. Custom Intelligence Feed is configured on the Check Point Gateway, which pulls the IP addresses, URLs, and domains from the ServiceNow AI Platform at pre-configured interval.

This integration supports three types of Block Lists:

-   IP Address \(This includes an individual IP Address \(IPv4 only\) for block list, and CIDR blocks \(ranges\) of addresses for allow list\).
-   URL
-   Domain

## Observables supported by the Check Point NGTP integration

The section lists descriptions of the observables supported by this integration and example formats for each type.

<table id="table_zyj_ssb_qgb"><thead><tr><th>

Observable Type

</th><th>

Examples

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain

</td><td>

-   example.com
-   mail.example.com

</td><td>

Wildcards are not supported.

</td></tr><tr><td>

IP Address

</td><td>

95.153.103.54 \(IPv4\)

</td><td>

Represents a single, distinct interface address. The integration supports only IPv4 and CIDR formats \(CIDR format is only supported for allow listing purpose\).For allow list purpose, integration has support for IP address observables includes CIDR \(Classless Inter-Domain Routing\) ranges, for example, 95.153.100.0/22.

**Note:** An error message is displayed when you try to attach a single IP address to a Block List that you have already allowed listed as a part of a CIDR range. For example, the single address 95.153.103.54 is part of the CIDR range represented by 95.153.100.0/22 \(95.153.100.0-95.153.103.255\).

</td></tr><tr><td>

URL

</td><td>

-   https://www.example.com
-   http://www.example.com

</td><td>

Description - The HTTPS URL are formatted by the application to trim the path from the URL and retain the domain name only. Check Point NGTP relies on HTTP CONNECT request to evaluate the web traffic and enforce blocking. For HTTPS CONNECT request, the entire URL isn’t visible in the request and only domain name is visible. When a user blocks any HTTPS URL with specific path \(example; https://www.example.com/path\), the application trims the path automatically \(www.example.com\). The application maintains the relationship between original observable and the formatted URL. Below is the screenshot of Block List Entry which shows the formatted URL and the original observable.

</td></tr></tbody>
</table>![Block list entry](../image/block-request-list-entries.png)

For HTTP URLs with a specific path \(for example, http://www.example.com/path\), Check Point would block the specified URL as the entire URL is visible in CONNECT request.

![Block list entries for HTTP URLs](../image/block-request-list-entries2.png)


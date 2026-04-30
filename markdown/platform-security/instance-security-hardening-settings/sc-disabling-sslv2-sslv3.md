---
title: Disable outbound SSLv2/SSLv3 connections \[Updated in Security Center 1.3 and 2.0\]
description: Use the glide.outbound.sslv3.disabled property to force the MID Server to use TLS when making outbound connections, such as REST and SOAP requests. Normally, outbound connections from an instance are forced to use TLS instead of SSL.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Disable outbound SSLv2/SSLv3 connections \[Updated in Security Center 1.3 and 2.0\]

Use the **glide.outbound.sslv3.disabled** property to force the MID Server to use TLS when making outbound connections, such as REST and SOAP requests. Normally, outbound connections from an instance are forced to use TLS instead of SSL.

Ensure the Glide Property **glide.outbound.sslv3.disabled** exists and is set to the value true. If the property does not appear in the sys\_properties table, add a new record.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.outbound.sslv3.disabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Purpose

</td><td>

To enforce the use if TLS during all outbound connections from ServiceNow instance.

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

false**Important:** The value for the **glide.outbound.sslv3.disabled** property is a safe override and cannot be altered once changed.

</td></tr><tr><td>

Security risk rating

</td><td>

6.5

</td></tr><tr><td>

Functional impact

</td><td>

This remediation enforces the usage of TLS protocol version when communicating on HTTPS. If there are devices that customer/users of the instance are using that do not support TLS communication, there may be a potential outage.

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Legacy versions of SSL were proven to be insecure when utilized for HTTP secure shell implementation, due to client-side attacks, including BEAST and SSL heart-bleed.

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Communications](sc-communications.md)


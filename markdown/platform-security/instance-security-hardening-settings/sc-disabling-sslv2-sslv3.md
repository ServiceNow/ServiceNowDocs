---
title: Disable outbound SSLv2/SSLv3 connections
description: Use the glide.outbound.sslv3.disabled property to force the MID Server to use TLS when making outbound connections, such as REST and SOAP requests. Normally, outbound connections from an instance are forced to use TLS instead of SSL.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-13"
reading_time_minutes: 1
breadcrumb: [Communications, Hardening settings, Platform Security]
---

# Disable outbound SSLv2/SSLv3 connections

Use the **glide.outbound.sslv3.disabled** property to force the MID Server to use TLS when making outbound connections, such as REST and SOAP requests. Normally, outbound connections from an instance are forced to use TLS instead of SSL.

The **glide.outbound.sslv3.disabled** system property controls the desired transport encryption protocol. If **glide.outbound.sslv3.disabled** is not set to the recommended value of **true**, then outbound MID server connections such as REST and SOAP requests will use SSL as the transport protocol. SSL was proven to be insecure in 2014.

Ensure that the **glide.outbound.sslv3.disabled** system property exists in the System Properties \[sys\_properties\] table and is set to the value **true**. If the property does not appear in the System Properties \[sys\_properties\] table, add a new record.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.outbound.sslv3.disabled**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

Boolean

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Default value

</td><td>

&lt;none&gt;

</td></tr><tr><td>

Fallback value

</td><td>

false

</td></tr><tr><td>

Category

</td><td>

[Communications](sc-communications.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 6.5
-   CVSS rating: Medium
-   Security risk details: SSLv3 has been proven insecure since 2014 due to vulnerabilities like POODLE, making it susceptible to man-in-the-middle attacks and data interception. Allowing SSLv3 undermines transport encryption and exposes sensitive data in transit, violating modern security standards.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see Add a system property.

**Parent Topic:**[Communications](sc-communications.md)


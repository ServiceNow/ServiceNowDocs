---
title: Set Xframe options to prevent embedding third-party websites \[Updated in Security Center 1.3\]
description: Configure this property to prevent the content of a web-application from being embedded in a third-party site.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-02-01"
reading_time_minutes: 1
breadcrumb: [Configuration, Hardening settings, Platform Security]
---

# Set Xframe options to prevent embedding third-party websites \[Updated in Security Center 1.3\]

Configure this property to prevent the content of a web-application from being embedded in a third-party site.

If **com.glide.cs.embed.xframe\_options** is not set to the recommended value of DENY or SAMEORIGIN, then content of the web application could be embedded in a third-party site using an ALLOW-FROM uri. Allowing untrusted third-party sites could enable attacks such as clickjacking.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.glide.cs.embed.xframe\_options**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

sameorigin

</td></tr><tr><td>

Default value

</td><td>

sameorigin

</td></tr><tr><td>

Category

</td><td>

[Configuration](sc-configuration.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.1
-   CVSS score: Low
-   Security risk details: Not setting this property to the recommended value could enable the content of a web application to be embedded in a third-party site enabling attacks such as click-jacking.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Configuration](sc-configuration.md)


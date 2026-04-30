---
title: Enforce credential alias usage \[New in Security Center 1.3 and updated in 1.5\]
description: Learn how to secure your credentials from unauthorized use by configuring the MID Server property.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-03-20"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce credential alias usage \[New in Security Center 1.3 and updated in 1.5\]

Learn how to secure your credentials from unauthorized use by configuring the MID Server property.

The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on your local network. MID Server properties are listed in the \[ecc\_agent\_property\] table. You can access them in your instance by navigating to **MID Server** &gt; **Properties**. Credential aliases allow an administrator to use specific credentials on Discovery schedules. Credential aliases provide more granular control over which credential a Discovery table is allowed to use. To remediate this security vulnerability, set **alias\_filtering\_behavior** to strict to prevent unnecessary exposure of credentials with elevated privileges. See [MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for more details.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**alias\_filtering\_behavior**

</td></tr><tr><td>

Configuration type

</td><td>

MID Server Properties \(/ecc\_agent\_property\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

string

</td></tr><tr><td>

Recommended value

</td><td>

strict

</td></tr><tr><td>

Default value

</td><td>

loose

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 2
-   CVSS score: Low
-   Security risk details: When this hardening setting is not set to strict, then all credentials are used regardless of their aliases for Discovery tables which increases the chance of unauthorized access.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Credential aliases for Discovery](../../../product/credentials/concept/discovery-credential-alias.md#)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


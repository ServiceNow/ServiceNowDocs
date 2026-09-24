---
title: Enforce credential alias usage
description: Learn how to secure your credentials from unauthorized use by configuring the MID Server property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enforce-credential-alias-usage.html
release: brazil
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-09-20"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce credential alias usage

Learn how to secure your credentials from unauthorized use by configuring the MID Server property.

The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on your local network. MID Server properties are listed in the \[ecc\_agent\_property\] table. You can access them in your instance by navigating to **MID Server** &gt; **Properties**.

The MID Server property **alias\_filtering\_behavior** defines the behavior of Discovery aliases. When the behavior is not `strict`, then all credentials are used regardless of their aliases for Discovery schedules. This behavior might not be desirable in some circumstances, particularly for credentials with elevated privileges. Credential aliases provide more control over which credentials a Discovery schedule is allowed to use and helps prevent the unnecessary exposure of credentials with elevated privileges.

See [MID Server properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/r_MIDServerProperties.md) for more details.

**Important:** This property has been deprecated and will be removed from future baselines.

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

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

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

-   [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/mid-server-landing.md)
-   [Credential aliases for Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/connections-and-credentials/discovery-credential-alias.md)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)


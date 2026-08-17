---
title: Restrict MID Server Users from Authenticating via the UI
description: Reduce risk from a compromised MID Server account by disallowing UI authentication
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/restrict-mid-server-users-from-authenticating-via-the-ui.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-27"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Restrict MID Server Users from Authenticating via the UI

Reduce risk from a compromised MID Server account by disallowing UI authentication

MID Server service accounts are automated system accounts that facilitate secure communication between the ServiceNow instance and resources behind your organization's firewall. These accounts should operate under the principle of least privilege, meaning they should only possess the minimum permissions necessary to perform their designated functions. Allowing UI authentication for MID Server accounts creates an unnecessary attack surface.

For each MID Server user record in the User \[sys\_user\] table, confirm that the **web\_service\_access\_only** field is set to "true".

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

User \[sys\_user\] table and mid\_server\_user.web\_service\_access\_only

</td></tr><tr><td>

Configuration type

</td><td>

User \[sys\_user\] table \(/sys\_user\_list.do\)

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

true

</td></tr><tr><td>

Fallback value

</td><td>

N/A

</td></tr><tr><td>

Category

</td><td>

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.8
-   CVSS rating: Low
-   Security risk details: If a MID Server account is compromised, an attacker with UI access could use the web interface to modify configurations or access sensitive data within the ServiceNow environment. By restricting these accounts to web service access only \(setting **web\_service\_access\_only** to true for MID Server users\), organizations help ensure that MID Server credentials can only be used for their intended purpose of service to service communication.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)


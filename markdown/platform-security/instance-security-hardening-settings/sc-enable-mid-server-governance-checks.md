---
title: Enable MID Server Governance Checks
description: Use an inactivity timeout on your MID Servers to reduce exposure to potential attackers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-enable-mid-server-governance-checks.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-27"
reading_time_minutes: 1
breadcrumb: [Session management, Hardening settings, Platform Security]
---

# Enable MID Server Governance Checks

Use an inactivity timeout on your MID Servers to reduce exposure to potential attackers.

Unused MID Servers that remain active create bidirectional security risk. Their credentials can still authenticate to the ServiceNow instance, giving an attacker a valid entry point. While active, the instance can still issue commands to them, extending the attack surface of instance compromise into infrastructure no one is monitoring.

With MID Server governance you can keep track of the last usage of each MID Server and create a policy to decommission it after a period of inactivity. The default inactivity timeout for MID Servers is 30 days.

Confirm that the **mid.inactivity.timeout.enabled** property exists in the System Properties \[sys\_properties\] table and is set to **true**.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**mid.inactivity.timeout.enabled**

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

true

</td></tr><tr><td>

Fallback value

</td><td>

true

</td></tr><tr><td>

Category

</td><td>

[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.6
-   CVSS rating: Medium
-   Security risk details: An attacker with access to an active MID Server could compromise the credential or impersonate the server and add output records to the ECC queue. An attacker wouldn't be able to use these credentials to horizontally traverse to other MID servers by inserting commands for them inside of ECC queue due to role restrictions on each MID Server user.

</td></tr><tr><td>

Functional impact

</td><td>

Inactive MID Servers are decommissioned on purpose.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Session management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-session-management.md)


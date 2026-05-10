---
title: Enforce scoped ACL access for information request playbooks \[New in Security Center 1.3 and updated in 1.5\]
description: Use the glide.enforce\_security\_scope.sn\_gsm\_info\_req property to control access to playbook data for the Information Request playbooks feature.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce scoped ACL access for information request playbooks \[New in Security Center 1.3 and updated in 1.5\]

Use the **glide.enforce\_security\_scope.sn\_gsm\_info\_req** property to control access to playbook data for the Information Request playbooks feature.

The Information Request Playbook application enables public sector end users to submit and track public record requests and provides government agents with a pre-defined process for handling and resolving these requests. If **glide.enforce\_security\_scope.sn\_gsm\_info\_req** is not set to true, unexpected access could be granted to playbook data for the Information Request playbooks application. Set this property to true to only consider ACLs from the sn\_gsm\_info\_req scope when granting access.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**glide.enforce\_security\_scope.sn\_gsm\_info\_req**

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

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 4.3
-   CVSS score: Medium
-   Security risk details: If this property is set to false, then ACLs from all scopes are considered when granting access to playbook data in the scope master table. This would expose information request playbook data.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr><tr><td>

References

</td><td>

-   [Using Information Request Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/psds-using-ir-playbooks.md)
-   [Configure Information Requests service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/awa-psds-overview.md)

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


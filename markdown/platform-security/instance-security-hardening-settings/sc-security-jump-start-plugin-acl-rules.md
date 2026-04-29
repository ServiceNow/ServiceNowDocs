---
title: Enable security jump start plugin \(ACL Rules\)
description: Activate the Security Jump Start \(ACL Rules\) \(com.snc.system\_security\) plugin to create several important ACLs that validate the Access Controls on some of the key system tables within the ServiceNow AI Platform.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable security jump start plugin \(ACL Rules\)

Activate the Security Jump Start \(ACL Rules\) \(com.snc.system\_security\) plugin to create several important ACLs that validate the Access Controls on some of the key system tables within the ServiceNow AI Platform.

Security Jump Start \(ACL Rules\) \(com.snc.system\_security\) plugin creates several important ACLs that validate the Access Controls on some of the key system tables within the Now Platform. These rules provide a jump-start on securing many system tables, making it easier for an organization to get an instance into production. The Security Jump Start \(ACL Rules\) plugin is installed automatically on all new instances.

Ensure that the Security Jump Start \(ACL Rules\) \(com.snc.system\_security\) plugin is activated.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.system\_security**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

N/A

</td></tr><tr><td>

Recommended value

</td><td>

N/A

</td></tr><tr><td>

Default value

</td><td>

N/A

</td></tr><tr><td>

Fallback value

</td><td>

N/A

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 8.1
-   CVSS rating: High
-   Security risk details: Gaps in access control can allow unauthorized users to view, modify, or delete sensitive data, undermining data integrity, confidentiality, and compliance with organizational security policies.

</td></tr><tr><td>

Functional impact

</td><td>

None

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](sc-access-control.md)


---
title: Configure Unique MID Server Users
description: Use unique user account for each of your MID Servers to promote auditability and security controls as well as least privilege access.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/instance-security-hardening-settings/sc-configure-unique-mid-server-users.html
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-27"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Configure Unique MID Server Users

Use unique user account for each of your MID Servers to promote auditability and security controls as well as least privilege access.

MID Server users authenticate MID Servers to the ServiceNow instance and enable communication to the instance. Configure each MID Server with a unique user account to promote auditability and security controls. Assigning a unique user account to each MID Server follows the principle of least privilege and enables proper identity and access management for your service accounts.

Configure each MID Server with a unique user account that has been assigned the **mid\_server** role:

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.
2.  Create a user for each MID Server \(for example, `mid_server_prod_01`, `mid_server_dev_01`\).
3.  In the **Roles** section, assign the **mid\_server** role to each user account.

    **Note:** Roles cannot be assigned until after the record is saved.

4.  Configure each MID Server to authenticate with its dedicated user account.
5.  Verify no duplicate **Logged in user** values exist in MID Server \[ecc\_agent\] table records.

For existing shared user accounts:

1.  Identify all MID Servers sharing the same user account. \(Records in the MID Server \[ecc\_agent\] table that have identical **Logged in user** field values\).
2.  Create unique user accounts \(User \[sys\_user\] records\) for each MID Server.
3.  Update each MID Server's configuration to use its dedicated account.
4.  Test connectivity before decommissioning the shared account.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

User \[sys\_user\] and MID Server \[ecc\_agent\] table records.

</td></tr><tr><td>

Configuration type

</td><td>

User \[sys\_user\] and MID Server \[ecc\_agent\] table records.

</td></tr><tr><td>

Data type

</td><td>

Table record

</td></tr><tr><td>

Recommended value

</td><td>

Each MID Server \[ecc\_agent\] record should have a unique User \[sys\_user\] record in it's **Logged in user** field. This user should have the **mid\_server** role.

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

[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 3.8
-   CVSS rating: Low
-   Security risk details: When multiple MID Servers share the same user account, it is difficult to perform the following:
    -   Determine which specific MID Server performed an action
    -   Trace the source of suspicious or malicious activity
    -   Implement granular access controls per MID Server
    -   Investigate security incidents or operational issues
    -   Comply with security logging and attribution requirements

</td></tr><tr><td>

Functional impact

</td><td>

Creating unique user accounts for each MID Server has no functional impact on MID Server capabilities or performance. All MID Servers will continue to operate normally with the **mid\_server** role permissions.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[Access control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/instance-security-hardening-settings/sc-access-control.md)


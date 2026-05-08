---
title: Define cross-scope access to an application resource
description: Track cross-scope requests for access to an application resource and approve or deny requests.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Restricted caller access privilege settings, Application access settings, Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Define cross-scope access to an application resource

Track cross-scope requests for access to an application resource and approve or deny requests.

## Before you begin

If you enable application administration for the target application, only application administrators of the target application can set access to an application. If application administration is not enabled, an admin user can set access to an application.

Role required: admin or application admin

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](../concept/ACL-access-checks.md) and [Delegated development and deployment](../concept/c_DelegatedDevelopment.md).

## Procedure

1.  To define access to an application resource, navigate to the application resource record.

    Available application resources include these options.

    -   Table
    -   Script Include
2.  Set the **Accessible from** field to **All application scopes**.

    If set to **This application scope only**, no other application scopes can access the resource.

3.  Select the appropriate access level in the **Caller Access** field.

<table id="choicetable_h1t_jtg_n1b"><tbody><tr><td id="d158590e128">

**None**

</td><td>

Cross-scope calls to the resource are approved or denied based on the value of the **Accessible from** field.

</td></tr><tr><td id="d158590e140">

**Caller Restriction**

</td><td>

Calls to the resource must be manually approved. Access requests are tracked in the Restricted Caller Access table with a status of Requested.

</td></tr><tr><td id="d158590e149">

**Caller Tracking**

</td><td>

Calls to the resource are automatically approved. Calls are tracked in the Restricted Caller Access table with a status of Allowed.

</td></tr></tbody>
</table>4.  Allow or deny an access request from a calling application.

    When a cross-scope application attempts to access a resource set to Caller Restriction, the system denies access to the resource and creates a record in the Restricted Caller Access table with a status of Requested. An admin user or application administrator must allow or deny the request. When access is allowed, all future access attempts gain access to the restricted resource.

    If a calling resource changes \(such as when a business rule’s script changes\), the restricted caller access record status changes to Invalidated. An admin user or application administrator must update the status to Allowed or Denied.

    1.  In the application record, navigate to the **Restricted Caller Access Privileges** tab.

    2.  Review records that have a Status of Requested.

        Each Restricted Caller Access Privilege record lists the operation performed, information about the calling source, and information about the target resource requested.

    3.  In the **Status** column, set the value from **Requested** to **Allowed** or **Denied**.

    Once a calling source is allowed, all subsequent calls are allowed.


**Parent Topic:**[Restricted caller access privilege settings](../concept/restricted-caller-access-privilege.md)


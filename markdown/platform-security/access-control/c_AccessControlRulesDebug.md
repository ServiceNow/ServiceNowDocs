---
title: ACL debugging tools
description: Field level debugging and access ACL rule output messages are available to help you troubleshoot and debug ACLs. The ACL configuration watcher lets you know what related ACLs exist when you modify one.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Advanced ACL configuration, Access Control List Rules, Access Management]
---

# ACL debugging tools

Field level debugging and access ACL rule output messages are available to help you troubleshoot and debug ACLs. The ACL configuration watcher lets you know what related ACLs exist when you modify one.

## Field level debugging

When debugging is enabled, a small bug icon \(![Debug icon](../image/Debug.png)‎\) appears beside each field with an ACL rule. Clicking the icon lists the ACL rules that apply for the field and the evaluation results. Enable debugging by navigating to **System Security** &gt; **Debugging** &gt; **Debug Security Rules**.

![Field level security on an incident](../../security/image/field_level_debugging.png "Field level security on an incident")

After enabling ACL debugging, you can impersonate another user to see what ACL rules the user passes and fails. When you impersonate a user, you can only see what that user is allowed to see. For example, you cannot view a record that an ACL prevents the user from seeing. To make debugging easier, read-only access to certain ACL-related tables is enabled by default, even when impersonating a user that does not have read access to the tables. To change this functionality, set the following property to **false**.

To enable ACL rule debugging, navigate to **System Security** &gt; **Debug Security Rules**.

<table id="table_bx2_rvk_yy"><thead><tr><th>

System property

</th><th>

Description

</th><th>

Default setting

</th></tr></thead><tbody><tr><td>

**glide.security.access\_acl\_as\_impersonator**

</td><td>

Allows read access to the following tables while impersonating a user: sys\_security\_acl, sys\_security\_operation, sys\_security\_type, and sys\_user\_role. As a result, the impersonating user can read data that the impersonated user cannot read.

</td><td>

true**Note:** When the property is set to false, the impersonated user might be prevented from reading ACL-related data. In this case, a second session logged in as admin or security\_admin might be required to debug ACLs.

</td></tr></tbody>
</table>## ACL rule output messages

ACL debugging displays ACL rule output messages at the bottom of each list and form. The output message displays the following:

<table id="table_obc_gcf_2r"><thead><tr><th>

Message element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TIME

</td><td>

The total time used to process this ACL rule.

</td></tr><tr><td>

PATH

</td><td>

Information that uniquely identifies each ACL rule in the format: `<ACL rule type>/<ACL rule name>/<Operation>`.

</td></tr><tr><td>

CONTEXT

</td><td>

The object being evaluated by the ACL rule.

</td></tr><tr><td>

RC

</td><td>

The return code of the ACL rule. A true value passes the ACL rule. A false value fails the ACL rule.

</td></tr><tr><td>

RULE

</td><td>

A brief summary of processors and scripts, followed by ACL results for each table-level and field-level ACL evaluation. Most ACL evaluations show an overall pass or fail result followed by a breakdown of the results for each type of ACL criteria:-   iAccessHandler: An internal system check using hidden source code on the platform. This is a system security check that you cannot modify. IAccessHandler can grant or deny access to a resource without evaluating ACLs. If IAccessHandler is ignored, then the ACLs are evaluated. You cannot modify the IAccessHandler checks in any way. For example, an IAccessHandler implementation is used for access checks on application resources and this cannot be changed.

This is available starting with the Istanbul release.

-   Roles: Verification that the user has the correct role.
-   Condition: Verification that the user passed the condition specified on the ACL rule \(if any\).
-   Script: Verification that the user passed the script specified on the ACL rule \(if any\).

</td></tr></tbody>
</table>The icons that appear show how the ACL was evaluated:

|Icon|Description|
|----|-----------|
|A green checkmark \(![Green checkmark](../image/GreenCheckmark.png)‎\)|Indicates the table or field passed the criteria.|
|A red x icon \(![Red x icon](../image/RedX.png)\)|Indicates the table or field did not pass.|
|An empty gray circle icon \(![Grey circle icon](../image/GrayCircle.png)‎\)|Indicates the ACL evaluation did not need to be performed.|
|A blue checkmark, x, or empty circle|Indicates that the ACL was taken from a cached result of a previous ACL check. The icons mean the same as the above.|

You can perform these actions on the ACL debug output:

-   Select or clear these check boxes at the top of the debug output:
    -   **Security rules**: Show or hide the results of the ACL checks.
    -   **Others**: Show or hide other warnings or messages.
-   Click the name of the ACL next to any of the output messages to open that ACL record.

    ![Click the ACL link](../../security/image/ACL_name_link.png)

-   Hover the cursor over any of the icons for the four ACL checks to see more information.

    ![Hover over an ACL check mark](../../security/image/ACL-hover.png)



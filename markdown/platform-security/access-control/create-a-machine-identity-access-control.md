---
title: Create a machine identity access control
description: Enable administrators to define and enforce granular control for integration users by introducing User Access Profiles. This feature provides an additional layer of security and control, allowing admins to specify the exact resources \(REST APIs and SOAP APIs\) that an integration user can access, ensuring tighter governance and minimizing security risks.
locale: en-US
release: australia
product: Access Control
classification: access-control
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Machine identity access controls, Access Management]
---

# Create a machine identity access control

Enable administrators to define and enforce granular control for integration users by introducing User Access Profiles. This feature provides an additional layer of security and control, allowing admins to specify the exact resources \(REST APIs and SOAP APIs\) that an integration user can access, ensuring tighter governance and minimizing security risks.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Machine Identity Access Controls**.

2.  Select the **New** button.

3.  Fill in the fields of the form.

<table id="table_mmy_wnz_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the access control record.

</td></tr><tr><td>

Application

</td><td>

Application containing the record.

</td></tr><tr><td>

Description

</td><td>

Description of the record.

</td></tr><tr><td>

Active

</td><td>

Determines if the policy is active

</td></tr><tr><td>

REST API Policy

</td><td>

Select the target REST API policy. **Note:** Select the ![Lock](../../security/image/machine-acl-lock-icon.png) and the ![Search](../../security/image/machine-acl-search-icon.png) icon to add a policy.

</td></tr><tr><td>

SOAP API Policy

</td><td>

Select the target SOAP API policy. **Note:** Select the ![Lock](../../security/image/machine-acl-lock-icon.png) and the ![Search](../../security/image/machine-acl-search-icon.png) icon to add a policy.

</td></tr><tr><td>

Tables

</td><td>

Select the tables this policy applies to

</td></tr><tr><td>

Applies to Child Table

</td><td>

Check this to apply the policy to child tables of the **Tables** field

</td></tr></tbody>
</table>4.  Select the `Insert a row below` prompt and add users to apply the control to.

    You can add multiple users to the access control.

    **Note:** You can only select users with Web Service Access.

5.  Select **Submit**.


## Result

The following is an example of a machine identity access control form that has been filled out:

![An example of a machine identity access control form filled out.](../../security/image/machine-acl-example.png)

A user with an machine identity access control cannot access any other APIs \(REST or SOAP\) and will only be able to access the resources explicitly stated in the access control, even if they have the required roles.


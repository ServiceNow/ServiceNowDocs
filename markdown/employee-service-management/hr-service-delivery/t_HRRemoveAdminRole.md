---
title: Remove HR Administrator role from IT System Administrators
description: After system configuration, remove the HR Administrator role \(sn\_hr\_core.admin\) from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive HR information via forms, lists and UI.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage HR roles, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Remove HR Administrator role from IT System Administrators

After system configuration, remove the HR Administrator role \(sn\_hr\_core.admin\) from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive HR information via forms, lists and UI.

## Before you begin

Role required: admin with sn\_hr\_core.admin

Make sure that you have at least two users with the HR Administrator role. If you assign only one person with the role and that person is deactivated, you will not have a user to perform the HR admin duties.

## Procedure

1.  Log in as admin.

2.  From **User Administration**, go to **Roles** \(left navigation menu\).

3.  Click **admin**.

4.  From the **Contains Roles** tab, click **Edit**.

5.  From the **Contains Roles List** column, highlight and move **sn\_hr\_core.admin** to the **Collection** column.

    **Note:** Also, remove other scoped HR Admin roles, such as sn\_hr\_le.admin.

6.  Click **Save**.

7.  Log out.


## What to do next

After removing the HR administrator role from IT System Administrator role, log out and log back for the changes to take effect.

**Note:** Ensure that you have completed the setup before you [Remove HR Administrator role from IT System Administrators](t_HRRemoveAdminRole.md).

All the default HR scheduled jobs will run as usual even after the HR Administrator role is removed from the IT System Administrator role.

**Note:** System user inherits the IT System Administrator role \(admin\). When you remove HR administrator role from the IT System Administrator role, System user will no longer have the HR administrator role. Validate all your customizations that are running in the context of System user.

**Parent Topic:**[Manage HR roles](../concept/c_ManageRoles.md)


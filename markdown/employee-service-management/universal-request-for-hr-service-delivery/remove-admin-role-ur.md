---
title: Remove UR administrator role from system administrator
description: After system configuration, remove the Universal Request \(UR\) administrator \[sn\_uni\_req.ur\_admin\] role from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive information via forms, lists and UI.
locale: en-US
release: zurich
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure service to use Universal Request, Configure, Universal Request, Employee Service Management]
---

# Remove UR administrator role from system administrator

After system configuration, remove the Universal Request \(UR\) administrator \[sn\_uni\_req.ur\_admin\] role from IT System Administrator role \(admin\) to help prevent IT System Administrators from viewing sensitive information via forms, lists and UI.

## Before you begin

Role required: admin with sn\_uni\_req.ur\_admin

## About this task

By default, a System Administrator also has a UR admin role and can access the UR information. Add UR Admin role to specific users who would work on the UR configuration for their respective services. The user with this role can make another user a UR admin based on the roles and responsibilities. After this step is complete, to secure your application, remove the UR administrator role \[sn\_uni\_req.ur\_admin\] from the System Administrator \[admin\] role.

By doing so, you prevent the user with a default System Administrator \[admin\] role from viewing all the Universal Request information.

**Note:** Ensure that you have at least two users with the UR administrator role. If you assign only one person with the role and that person is deactivated, you no longer will have a user that can perform the UR admin duties.

Also, ensure that the same users have the System Administrator \[admin\] role to access the UR modules.

## Procedure

1.  Log in as admin.

2.  From **User Administration**, go to **Roles** \(left navigation menu\).

3.  Click **admin**.

4.  On the **Contains Roles** tab, click **Edit**.

    **Note:** If you do not see the **Edit** button, change the **Application** scope to `Global`.

5.  From the **Contains Roles List** column, highlight and move **sn\_uni\_req.ur\_admin** to the **Collection** column.

6.  Click **Save**.

7.  Log out.


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)


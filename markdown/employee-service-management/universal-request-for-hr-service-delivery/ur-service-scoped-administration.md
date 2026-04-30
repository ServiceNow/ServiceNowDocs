---
title: Register application administration enabled scoped application
description: If your application is an admin enabled scoped application, register the application with Universal Request \(UR\) to make your application’s service and service set data available for the Universal Request application to work.
locale: en-US
release: zurich
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure service to use Universal Request, Configure, Universal Request, Employee Service Management]
---

# Register application administration enabled scoped application

If your application is an admin enabled scoped application, register the application with Universal Request \(UR\) to make your application’s service and service set data available for the Universal Request application to work.

## Before you begin

Role required: admin

## About this task

After you [configure your service](../concept/config-service-for-ur.md), you must perform these steps and create the following ACL-inheritance entries. This enables Universal Request to use your application’s service and service set data.

Only UR administrator \[sn\_uni\_req.ur\_admin\] can assign scoped UR roles.

To configure your system, you must log in as a System Administrator \[admin\]. The UR Administrator \[sn\_uni\_req.ur\_admin\] role is contained in the System Administrator \[admin\] role. The combination of these two roles allows a user to perform all tasks associated with configuring your system.

After system configuration, ensure that only the UR Administrator \[sn\_uni\_req.ur\_admin\] role has access to sensitive information. Remove the UR Administrator role from System Administrator \[admin\] role to prevent the System Administrator from viewing sensitive UR information. For more information, see [Remove UR administrator role from system administrator](remove-admin-role-ur.md).

After granting access, define the **sn\_uni\_req.min\_admin\_count** property in the system properties for UR to ensure that a minimum number of scoped administrators exist and the application is not locked out in one administrators absence.

## Procedure

1.  In the navigation panel, enter `sys_scoped_admin_acl_inheritance.list`.

2.  In the **Application Administration ACL Inheritance** page, click **New**.

3.  Select `Service Set` from the **Table** drop-down list.

4.  Check that the **Application** is your scoped application

5.  Click **Submit**.

    Creates an ACL inheritance record for the service set table in your scoped application.

6.  In the **Application Administration ACL Inheritance** page, click **New** again.

7.  Select `Service Configuration` from the **Table** drop-down list.

8.  Check that the **Application** is your scoped application

9.  Click **Submit**.

    Creates an ACL inheritance record for the service configuration table in your scoped application.


**Parent Topic:**[Configure service to use Universal Request](../concept/config-service-for-ur.md)


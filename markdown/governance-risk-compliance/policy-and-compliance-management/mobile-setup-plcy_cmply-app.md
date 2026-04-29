---
title: Setup checklist for the GRC Mobile application
description: The following checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform instance and on your mobile device prior to using the GRC Mobile application. Complete these set up tasks prior to using the GRC Mobile application to view the Policy and Compliance Management application on your mobile device.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Managing mobile experience for GRC Policy and Compliance, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Setup checklist for the GRC Mobile application

The following checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform® instance and on your mobile device prior to using the GRC Mobile application. Complete these set up tasks prior to using the GRC Mobile application to view the Policy and Compliance Management application on your mobile device.

## Before you begin

As an option, print this checklist and use it to guide you through the set up tasks that are required for the GRC Mobile application.

Estimated time to complete this task: 15-20 minutes.

Roles required: admin, sn\_compliance.manager

## Procedure

1.  Verify that you complete each item on the list so that you can log in to the GRC Mobile application and add a ServiceNow AI Platform instance.

<table id="table_lqq_1qt_rhb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the admin role, verify that you have the GRC core applications installed on a ServiceNow AI Platform instance. This is the ServiceNow AI Platform instance that you view on your mobile device.

 **Note:** The GRC core applications and the ServiceNow AI Platform instance should be from the same family release.

 1.  To verify the GRC: GRC Profile Dependencies core application is installed on your instance, navigate to **Plugins** and search for GRC Profile.
2.  If the GRC Profile core application is not already installed, click **Install** to install it.
3.  After the GRC Profile application is installed, install either the Policy and Compliance Management core application, or the Risk Management core application, or both the Policy and Compliance Management and Risk Management applications. These are the two GRC applications that you can view with the GRC Mobile application.
 If not visible in your instance, all of the GRC core applications are available from the ServiceNow Store.

 For more information about getting entitlement, downloading, and installing the GRC core applications, see [GRC and the ServiceNow Store](../../grc-common/concept/grc-and-store.md).

When you install the GRC core applications, the dependency plugins for the GRC Mobile application, \(com.glide.sg and com.glide.sg.agent\_native\_client\) are also automatically installed.To verify that these dependency plugins are installed and activated:

 1.  Navigate to **Plugins**.
2.  Search for the plugin IDs \(com.glide.sg and com.glide.sg.agent\_native\_client\).
3.  If they are not activated, activate these plugins.


</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the admin role, verify that you have the GRC mobile app installed on the ServiceNow AI Platform instance that you want to view on your mobile device.

 **Note:** The GRC mobile app and the ServiceNow AI Platform instance should be from the same family release.

 For more information about getting entitlement, downloading, and installing the GRC Mobile application, see [GRC and the ServiceNow Store](../../grc-common/concept/grc-and-store.md).

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the admin role, in your ServiceNow AI Platform instance verify that you have assigned mobile users with the required ServiceNow AI Platform roles.

 1.  To view the roles that are assigned to a user, navigate to **Users and Groups** &gt; **Users**.
2.  Select the user name followed by the roles related list. All roles assigned to this user are displayed.
3.  Verify a user is assigned, or assign a user with the IT Infrastructure Library role \(itil\). Users with the itil role can create, open, and update records. Only users with the itil role can have tasks assigned to them.
4.  Verify a user is assigned, or assign a user with the compliance manager role \(sn\_compliance.manager\). This role is automatically added when you assign the itil role.
5.  Verify you have created any required assignment groups and assigned mobile users to these groups.
 **Note:** If you have multiple users for the mobile application, you alternatively can assign the sn\_compliance.manager role to a group. Each user you add to the group inherits this role.

 For more information on users and assigning roles to users and groups, see [Create a user](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US), [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US), [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a mobile user with the sn\_compliance.manager role, download and install the most current ServiceNow® Agent app on your mobile device.

 The most current Agent app is available on the Apple iOS App Store and the Google Play Store.

 ![Agent app Fullfiller.](../../../common/image/mobile-vr-agent_app-8182.png)

</td></tr><tr><td>

![Check box.](../../grc-audit-implementation/image/checkbox.png)

</td><td>

As a user with the sn\_compliance.manager role, verify notifications are enabled on your mobile device and in your ServiceNow AI Platform instance.

 Notifications inform you when critical pending approval requests are assigned to you or to your assignment group. To assist you with timely remediation, after you enable notifications, click on a notification in the GRC Mobile application and navigate directly to the record.

 To enable notifications in your ServiceNow AI Platform instance so they are displayed on your mobile device, follow these steps.

1.  Verify you have downloaded and installed the GRC Mobile application on your ServiceNow AI Platform instance.
2.  In System Settings in your ServiceNow AI Platform instance, under Notifications, verify you have enabled the **ServiceNow Mobile Application**.
 ServiceNow AI Platform notifications are also displayed on the messages screen on your mobile device. Verify that notifications are also enabled in the settings of your mobile device.

</td></tr></tbody>
</table>    You have successfully set up your mobile device and the ServiceNow AI Platform for the GRC Mobile application. The next step is to log in to your ServiceNow AI Platform instance with the ServiceNow Agent app on your mobile device.


**Parent Topic:**[Managing mobile experience for GRC Policy and Compliance](../concept/mobile-policy_compliance-ovrvw.md)


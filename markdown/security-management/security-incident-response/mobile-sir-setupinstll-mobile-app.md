---
title: Set up checklist for the Security Incident Response Mobile app
description: The following checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform instance and on your mobile device prior to using the Security Incident Response Mobile app.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Mobile Experience for Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Set up checklist for the Security Incident Response Mobile app

The following checklist includes the set up tasks that you are required to complete in your ServiceNow AI Platform® instance and on your mobile device prior to using the Security Incident Response Mobile app.

## Before you begin

As an option, print this checklist and use it to guide you through the set up tasks that are required for the Security Incident Response Mobile app. Verify that each item on the list is completed so that you can view and edit SIR security incidents on your mobile device.

The check list items are displayed in highlighted text. More information follows each item in the right column. Estimated time to complete this task: 15-20 minutes.

Roles required: admin, sn\_si.analyst

<table id="table_l5b_h24_nhb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

![Checkbox.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the admin role, verify that you have the Security Incident Response core application installed on a ServiceNow AI Platform instance. This is the ServiceNow AI Platform instance that you view on your mobile device.**Note:** The Security Incident Response core application and the ServiceNow AI Platform instance should be from the same family release.

 1.  To verify the core application is installed on your instance, navigate to **Plugins** and search for Security Incident Response.
2.  If the Security Incident Response core application is not already installed, click **Install** to install it.

 For more information about installing the Security Incident Response core application, see [Install and configure Security Incident Response](install-and-configure-sir.md).

 If the Security Incident Response core application is not visible in Plugins, for more information about installing core applications and entitlements to applications, see [Security Operations and the ServiceNow Store](../../planning-and-policy/concept/secops-and-store.md).

</td></tr><tr><td>

![Checkbox.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the admin role, verify that you have the Security Incident Response Mobile app installed on the ServiceNow AI Platform instance that you want to view on your mobile device.**Note:** the Security Incident Response Mobile app and the ServiceNow AI Platform instance should be from the same family release.

 Download and install the Security Incident Response Mobile app from the ServiceNow Store on your ServiceNow AI Platform instance.

 When you install the Security Incident Response Mobile app, its dependencies, com.glide.sg and com.glide.sg.agent\_native\_client, are also installed.

 To verify that these dependencies are installed:

1.  Navigate to **Plugins**.
2.  Search for the plugin IDs \(com.glide.sg and com.glide.sg.agent\_native\_client\).
3.  If they are not activated, activate these plugins. These plugins are required for the Security Incident Response Mobile app.

 For more information about installing applications and entitlements to applications, see [Security Operations and the ServiceNow Store](../../planning-and-policy/concept/secops-and-store.md).

</td></tr><tr><td>

![Checkbox.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the ServiceNow AI Platform admin role, verify that you have assigned mobile users with the required roles in your ServiceNow AI Platform instance. 1.  To view the roles that are assigned to a user, navigate to **Users and Groups** &gt; **Users**.
2.  Select the user name followed by the roles related list. All roles assigned to this user are displayed.
3.  Verify a user is assigned, or assign a user with the IT Infrastructure Library role \(itil\). Users with the itil role can create, open, update and close security incidents. Only users with the itil role can have tasks assigned to them.
4.  Verify a user is assigned, or assign a user with the security analyst role \(sn\_si.analyst\). Users with the sn\_si.analyst role can read and edit security incident records. This role is automatically added when you assign the itil role.
5.  Verify you have created any required assignment groups and assigned mobile users to these groups.

 **Note:** If you have a large number of users for the mobile application, you alternatively can assign the sn\_si.analyst role to a group. Each user you add to the group inherits this role.

 For more information about security analysts, see [Assigning security analysts](../reference/r_AgentAssignment.md#).

 For more information on users and assigning roles to users and groups, see [User administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_UserAdministration.md).

</td></tr><tr><td>

![Checkbox.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the sn\_si.analyst role, download the most current ServiceNow® Agent app on your mobile device.The most current version of the Agent app is available on the Apple iOS App Store and the Google Play Store.

 ![ServiceNow Agent app.](../../../common/image/mobile-vr-agent_app-8182.png)

</td></tr><tr><td>

![Checkbox.](../../vulnerability-response/image/checkbox.png)

</td><td>

As a user with the sn\_si.analyst role, verify notifications are enabled on your mobile device and in your ServiceNow AI Platform instance.Notifications inform you when critical security incidents are assigned to you or to your assignment group. To assist you with timely remediation, after you enable notifications, click on a notification in the Security Incident Response Mobile app to navigate directly to the security incident.

 To enable notifications in your ServiceNow AI Platform instance so they are displayed on your mobile device, follow these steps.

1.  Verify you have downloaded and installed the Security Incident Response Mobile app on your ServiceNow AI Platform instance.
2.  In System Settings in your ServiceNow AI Platform instance, under Notifications, verify you have enabled the **ServiceNow Mobile Application**.

For more information about setting notifications, see [Setting user notification preferences in Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-notification-preferences.md).


 ServiceNow AI Platform notifications are also displayed on the messages screen on your mobile device. Verify that notifications are also enabled in the settings of your mobile device.

</td></tr></tbody>
</table>You have successfully set up your mobile device and the ServiceNow AI Platform for the Security Incident Response Mobile app. The next step is to log in to your ServiceNow AI Platform instance with your mobile device.


---
title: Change tenant to configure pre-published apps
description: Change the tenant to use pre-published apps in your environment.Override an existing tenant connection, only if, for any reason, you are unable to uninstall the connected Microsoft Teams tenant from the original ServiceNow instance.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration for Employee Experience, Setup for integrating pre-published apps, Setup the Servicenow instance, Integrating ServiceNow with Microsoft Teams and Microsoft 365, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Change tenant to configure pre-published apps

Change the tenant to use pre-published apps in your environment.

## Before you begin

Role required: External admin \(external\_app\_install\_admin\)

## About this task

If you have already set up a connection on a different Microsoft Teams tenant, changing to a new tenant stops the integration from working on the originally configured tenant. All users using the integration on the original tenant will no longer be able to use it. If you are only changing from self-configured Azure apps to pre-published Azure apps, but keeping the integration on the same Microsoft Teams tenant, there will not be an impact to users.

Uninstall the connected Microsoft Teams tenant from the original/registered ServiceNow instance. Then install the same Microsoft Teams tenant on the new/required ServiceNow instance.

## Procedure

1.  Uninstall the connected Microsoft Teams tenant from the original ServiceNow instance.

    1.  Open your current/original/registered ServiceNow instance.

    2.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

    3.  Select **Uninstall**.

        ![Uninstall current Microsoft Teams tenant](../images/uninstall-current-ms-teams-tenant1.png)

    4.  Select **Uninstall** on the Uninstall Microsoft Teams Tenant dialog box to uninstall the connected Microsoft Teams in your instance.

        ![Select Uninstall](../images/uninstall-current-ms-teams-tenant2.png)

        Your Microsoft Teams tenant is disconnected from the original/registered ServiceNow instance.

2.  Install the same Microsoft Teams tenant on the new/required ServiceNow instance.

    1.  Open your new/target ServiceNow instance.

    2.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

    3.  Click **Install** to install the same Microsoft Teams in your new/target instance.

    4.  Select the **Consent on behalf of your organization** option to provide the consent for all your users, and click **Accept** button to provide the admin consent.

        ![Admin consent for the app.](../images/sso-activity-notification-admin-consent.png)

    5.  Once the tenant is mapped with the ServiceNow instance, you must authorize the apps by providing the admin consent.

        The Notify Connector and Import Chat apps appear only if you install Notify plugin in your instance.

        ![Authorize Azure apps](../images/uninstall-current-ms-teams-tenant1.png)

        -   **SSO and Activity Notification**: Authorize this app to display **Employee Center** tab in Microsoft Teams app.
        -   **Notify Connector**: Authorize this app to enable agents to initiate a Microsoft Teams meeting from a task record.
        -   **Request-based Chats**: Authorize this app to enable the agents to initiate chat in Microsoft Teams and import chat messages to the respective record.
    6.  Authorize the apps as required.


## What to do next

You must upload the manifest file in Microsoft Teams. For more information, refer [Create and download the manifest file for pre-published apps](download-manifest-file-mt.md).

**Parent Topic:**[Setup for integrating pre-published apps with Microsoft Teams for Employee Experience](../concept/c_employee_ex_tnt.md)

## Override Microsoft Teams tenant connection

Override an existing tenant connection, only if, for any reason, you are unable to uninstall the connected Microsoft Teams tenant from the original ServiceNow instance.

### Before you begin

Role required: External admin \(external\_app\_install\_admin\)

### About this task

Create the sn\_now\_azure.allow\_tenant\_override system property and set it to True. Then override the existing Microsoft Teams tenant connection on the Install Azure Apps page.

**Note:** ServiceNow doesn’t recommend the override method.

### Procedure

1.  Open your new/target ServiceNow instance.

2.  In the navigation filter, enter `sys_properties.list`.

3.  Select **New** on the System Properties page.

4.  On the System Property form, fill in the fields.

    -   Search and select **Azure Active Directory User Mapping** as **Application**.
    -   Enter **allow\_tenant\_override** in **Suffix**.
    -   Name value **sn\_now\_azure.allow\_tenant\_override** is auto populated in **Name**.
    -   Select **true \| false** as **Type**.
    -   Enter **true** in **Value**.
5.  Select **Submit**.

    **Note:**

    If the **Value** field entry is **false**, then the method of uninstalling the connected Microsoft Teams tenant from the original ServiceNow instance should be followed.

    ![Set system property sn_now_azure.allow_tenant_override](../images/sys-prop-allow-tenant-override.png)

    This activates the method of overriding the Microsoft Teams tenant connection on the Install Azure Apps page by enabling the **Change tenant** option.

6.  Navigate to **All** &gt; **ServiceNow for Microsoft 365** &gt; **Install Azure apps**.

7.  Select **Change tenant** to map the tenant with your new ServiceNow instance.

    ![Override using Change tenant option](../images/change-tenant-with-override.png)

8.  Enter **CHANGE** and select **Override connection**.

    ![Override tenant connection](../images/override-tenant-connection.png)

9.  Authorize the apps by providing the admin consent after the tenant is mapped to the new ServiceNow instance.



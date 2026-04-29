---
title: Update a Now Assist application with the Application Manager
description: When you update a Now Assist application to a new version, the Application Manager uses Now Assist suites to verify compatibility with any other Now Assist applications in your instance.
locale: en-US
release: australia
product: Application Manager
classification: application-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing Now Assist apps, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Update a Now Assist application with the Application Manager

When you update a Now Assist application to a new version, the Application Manager uses Now Assist suites to verify compatibility with any other Now Assist applications in your instance.

## Before you begin

For domain-separated instances:

-   applications must be installed and updated from the global domain.
-   The `sys_user` table record for the user who completes the task must also be in the global domain.

Role required: admin or sn\_appclient.app\_client\_user

**Note:** Some applications and plugins can't be uninstalled after they've been installed.

## Procedure

1.  Navigate to the **Installed** tab of Application Manager in one of the following ways.

    -   Navigate to **Admin** &gt; **Application Manager** &gt; **Installed**.
    -   Navigate to **All** &gt; **Admin Center** &gt; **Application Manager** &gt; **Installed**.
2.  Find and select the Now Assist application that you want to update.

    You can search for an application by name, or use the filter options available in the Application Manager.

3.  Select **Proceed to update**.

    **Note:** If **Proceed to update** is unavailable, it means there is an update for the Now Assist suite version that application is part of, but no update for that application itself. No further action is required.

4.  In the **Select suite version** drop-down menu, select a Now Assist suite version.

    The available suite versions are compatible with your instance. If you have other Now Assist applications already installed on your instance, they might require update for suite compatibility. For more information about Now Assist suite compatibility, see [Now Assist suite versions in the Application Manager](../concept/now-assist-suites-app-mgr.md).

    If you haven't installed a Now Assist suite version yet, you have the option to choose **none** in the version selector. This option enables you to begin using Now Assist suites at a time that works best for your organization.

5.  If you have available application customizations, use the **Customized ver.** drop-down menu to select which customization to use.

    Your customizations might not be compatible with a new application version. Update the application in a non-production instance, then make any necessary changes to your customization and validate compatibility before making updates in production instances. For more information about managing customizations, see [Manage customizations to applications](https://www.servicenow.com/docs/access?context=manage-customizations-store-apps&version=australia&pubname=australia-application-development&ft:locale=en-US).

6.  Include demo data if it's desired and available.

    1.  Select the option to install demo data next to each Now Assist application you want demo data for.

        The option to install demo data isn't available for all applications.

    2.  Turn on the **Load demo data for selected apps** toggle switch.

7.  Select **Continue** to review the installation details.

    If any applications display "Installation blocked," it means that application version isn't licensed yet. Either uninstall the application or license the required version. For more information, see [App installation blocked when installing or updating Now Assist suite](../reference/app-installation-blocked.md).

8.  Update the application now or schedule installation for a later time.

<table id="choicetable_vcm_ndz_tgc"><thead><tr><th align="left" id="d180068e307">

Installation option

</th><th align="left" id="d180068e310">

Procedure

</th></tr></thead><tbody><tr><td id="d180068e316">

**Install now**

</td><td>

1.  Leave the default option to **Install now** selected.
2.  Select **Install**.


</td></tr><tr><td id="d180068e340">

**Install later**

</td><td>

1.  Select the option to **Install later**.
2.  Enter a start date and start time.
3.  Select **Schedule**.


</td></tr></tbody>
</table>
## Result

If you choose to install the update now, the new application version begins to install immediately. Any dependencies or other Now Assist applications that require updates for compatibility are also installed.

Scheduled version installations begin at the chosen date and time.

**Related topics**  


[App installation blocked when installing or updating Now Assist suite](../reference/app-installation-blocked.md)

[Uninstall an application](uninstall-application-app-mgr.md)

[Buy a ServiceNow application](../../servicenow-store/task/buy-servicenow-app.md)


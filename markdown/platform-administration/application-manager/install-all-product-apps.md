---
title: Install all applications in a product
description: Install all applications and plugins included in a product using Application Manager.
locale: en-US
release: australia
product: Application Manager
classification: application-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Installing apps, plugins, and products, Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install all applications in a product

Install all applications and plugins included in a product using Application Manager.

## Before you begin

For domain-separated instances:

-   applications must be installed and updated from the global domain.
-   The `sys_user` table record for the user who completes the task must also be in the global domain.

Role required: admin, sn\_appclient.app\_client\_user, or sn\_appclient.app\_client\_company\_installer

**Note:** Some applications and plugins can't be uninstalled after they've been installed.

## Procedure

1.  Navigate to the **Available for you** tab of the Application Manager in one of the following ways.

    -   Navigate to **Admin** &gt; **Application Manager** &gt; **Available for you**
    -   Navigate to **All** &gt; **Admin Center** &gt; **Application Manager** &gt; **Available for you**.
2.  Find and select the product you want to install.

    You can search for a product by name, or use the sort and filter options available in the Application Manager.

3.  Review the technical details of each included application to verify that you have access to all required dependencies.

    1.  Select an application dependency and scroll to the technical details section of the application details page.

        From the technical details section, you can review the dependencies of the individual application. You can see which dependencies are installed, not installed, and not licensed.

    2.  Procure any dependencies that aren't licensed from the ServiceNow Store.

        For more information, see [Getting apps and trials from the ServiceNow Store](../../servicenow-store/concept/getting-apps-trials.md).

    3.  Go back to the product details page and repeat for each application dependency.

4.  From the product details page, select **Install**.

5.  Select the desired versions of each application to be included in the product.

6.  Select **Load demo data** if you want demo data to be included in the installation.

7.  Select **Proceed**.

8.  Install the product now or schedule installation for a later time.

<table id="choicetable_dm4_3km_yfc"><thead><tr><th align="left" id="d291280e229">

Installation option

</th><th align="left" id="d291280e232">

Procedure

</th></tr></thead><tbody><tr><td id="d291280e238">

**Install now**

</td><td>

1.  Leave the default option to **Install now** selected.
2.  Select **Install**.


</td></tr><tr><td id="d291280e262">

**Install later**

</td><td>

1.  Select the option to **Install later**.
2.  Enter a start date and start time.
3.  Select **Schedule**.


</td></tr></tbody>
</table>
## Result

If you choose to install the product now, it and its dependencies begin to install immediately. Scheduled installations begin at the chosen date and time.

**Parent Topic:**[Installing applications, plugins, and products](../concept/installing-apps-app-manager.md)


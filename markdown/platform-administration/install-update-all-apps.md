---
title: Install or update all applications in a ServiceNow product
description: Install or update all applications that are part of a ServiceNow product from your ServiceNow instance at a time.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install or update all applications in a ServiceNow product

Install or update all applications that are part of a ServiceNow product from your ServiceNow instance at a time.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Select the **ServiceNow Products** option in the **Listing type** filter options.

    The list of the ServiceNow products in displayed.

3.  Search for the required ServiceNow product and open the record.

    Use the **Licensed** and **Not Licensed** tabs to view details about applications in the product.

4.  Click **Install/Update All**.

    **Note:** By default, application of the latest version is installed. If you want to install the application of another version, select the required version and select the application check box.

5.  Select the **Load demo data** check box to load demo data for all the applications displayed in the Install pop-up window.

6.  Click **Install**.

    -   If there are any errors or conflicts, the details are displayed in the Install pop-up window. To proceed with installation, you must address the errors and resolve the conflicts.
    -   If there are no errors or conflicts, the applications are installed or updated, and a confirmation message is displayed.
7.  While installation is in progress, you can have application installed in the background by clicking **Continue in background**.

    After refreshing the page, this message is displayed: `Product installation in progress, click here to view details.` Click the link to see the installation progress.


## Result

A confirmation message is displayed if all the applications are installed. Otherwise, the number of successful and unsuccessful installations are displayed.

**Parent Topic:**[Using Legacy Application Manager](using-legacy-application-manager.md)


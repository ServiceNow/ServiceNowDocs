---
title: Install or update all applications in a ServiceNow product
description: Install or update all applications that are part of a ServiceNow product from your ServiceNow instance at a time.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Legacy Application Manager, Administering applications, Get started, Administer the ServiceNow AI Platform]
---

# Install or update all applications in a ServiceNow product

Install or update all applications that are part of a ServiceNow product from your ServiceNow instance at a time.

## Before you begin

**Note:**

Legacy Application Manager is being prepared for deprecation. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

A known issue affects the use of bookmarks to access the Legacy Application Manager. For details about possible issues with accessing the Legacy Application Manager, see the [Deprecated Classic App Manager URL usage causes issues on instances running ZP5 / YP10 and above \[KB2804238\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2804238) article in the Now Support knowledge base.

A new Application Manager experience is available. The new experience simplifies the process of managing your licensed applications by consolidating them in one convenient location, displaying all applications, plugins, installed applications, and available updates. For more information, see [Application Manager](../../../administer/application-manager/concept/application-manager.md).

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


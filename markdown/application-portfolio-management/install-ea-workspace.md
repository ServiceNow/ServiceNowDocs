---
title: Install Enterprise Architecture Workspace
description: Install the Enterprise Architecture Workspace application \(sn\_apm\_ws\) if you have the admin role.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Install Enterprise Architecture Workspace

Install the Enterprise Architecture Workspace application \(sn\_apm\_ws\) if you have the admin role.

## Before you begin

-   Review the Enterprise Architecture Workspace application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Ensure you have activated the Enterprise Architecture plugin \(com.snc.apm\).
-   For enabling the technology portfolio management information in the Enterprise Architecture Workspace:
    -   Ensure you have activated the Software Asset Management Foundation plugin \(com.snc.sams\).
    -   Ensure you have installed the Technology Portfolio Management \(sn\_apm\_tpm\) store app.

Role required: admin

![Install Enterprise Architecture Workspace screen.](../image/eaw-image/eaw-install-app.png)

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


-   **[Enterprise Architecture Workspace access roles](../reference/eaw-reference/eaw-access-roles.md)**  
The following roles help you to configure and use the Enterprise Architecture Workspace application. After access has been granted to a role, all the groups or users assigned to the role are granted access. Roles can contain other roles, and any access granted to a role is granted to any other role that includes it.
-   **[Tables installed with Enterprise Architecture Workspace](../reference/eaw-reference/eaw-installed-tables.md)**  
The following tables are added with activation of Enterprise Architecture Workspace.

**Parent Topic:**[Enterprise Architecture Workspace](../concept/ea-workspace.md)


---
title: Set up Service Graph Workspace
description: Set up and access CMDB Workspace and then switch to using Service Graph Workspace.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-02-09"
reading_time_minutes: 4
breadcrumb: [Configure, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set up Service Graph Workspace

Set up and access CMDB Workspace and then switch to using Service Graph Workspace.

Use the sections in this topic to try and then switch into using Service Graph Workspace:

1.  Request and install the latest CMDB Workspace store app.
2.  Optionally, enable demo data for the app.
3.  Review the prerequisites for CMDB Workspace.
4.  From within CMDB Workspace, switch into using Service Graph Workspace.

**Note:** CMDB Workspace and Service Graph Workspace can't be active at the same time. You can use only one of those at any given time.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** The CMDB Workspace store app is automatically installed when installing or upgrading the product.

## Enable demo data

Enable demo data to install demo data-specific scheduled jobs that if the needed requirement is met, generates and populates demo data in CMDB Workspace and Service Graph Workspace cards such as:

-   Cloud vs Non-cloud resources chart: If Cloud Service Accounts \[cmdb\_ci\_cloud\_service\_account\] table exists
-   Cards in the CMDB 360 view: If CMDB 360 is enabled
-   Cards in the Insights view, CMDB Feature Adoption tile:
    -   CIs processed by IRE
    -   CIs processed by IRE based on source
    -   Data Manager
    -   Data attestation
    -   Query Builder
    -   Intelligent Search
-   Cards in the What's new tile in the Service Graph Workspace landing page.

To populate Service Graph Workspace dashboards with demo data:

1.  When installing the CMDB Workspace store app, check **Load demo data**.
2.  Access the **\[Demo\] — CMDB Workspace demo data** scheduled job and select **Execute Now**.

**Note:** As a general practice, don't enable demo data in a production instance to prevent demo data mixing with real production data.

## Prerequisites

-   Plugins:

    -   Recommended: CSDM Activation \(com.snc.cmdb.csdm.activation\)

        Allows for legacy **Lifecycle Status** field mappings and synchronization to legacy status fields. For details about use and customization of retirement definitions when this plugin isn't activated, see [Retirement definitions](life-cycle-rules.md).

    -   Required \(activated by default\): CMDB CSDM Support \(com.snc.cmdb.csdm\)
    -   Required \(activated by default\): CMDB Page Templates \(sn\_cmdb\_pg\_templts\)
    -   Required \(activated by default\): CMDB NLQ Search Connected \(sn-cmdb-nlq-search\)
    For details about activating a plugin, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   Roles: To access the Service Graph Workspace, you must, at a minimum, have one of the following roles, which are essential for interacting with the Service Graph Workspace. Depending on which of these roles is assigned to you, you might only have access to some of the features available in the Service Graph Workspace:

    -   sn\_cmdb\_admin
    -   sn\_cmdb\_editor
    -   sn\_cmdb\_user
    **Note:** As you drill down in the Service Graph Workspace, there are some dashboards and list views that require specific roles in addition to the key CMDB Admin, CMDB Editor, or CMDB User roles.

-   Features: Service Graph Workspace provides access to a wide range of applications and features. However, for Service Graph Workspace to provide meaningful reports, overviews, and trends, you must set up and configure some of those features. Setup for such features is listed under Additional requirements.

## Switch to Service Graph Workspace

After installing CMDB Workspace, administrators can try out Service Graph Workspace and also let users try Service Graph Workspace. After experimenting with the features that Service Graph Workspace provides, you can switch into permanently using Service Graph Workspace instead of CMDB Workspace. Once switching, CMDB Workspace is turned off, and using Service Graph Workspace applies to all users.

To switch to Service Graph Workspace and turn off CMDB Workspace:

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.
2.  In the Home view in CMDB Workspace, select **Try new workspace** or **Retry new workspace** in the Try the new Service Graph Workspace banner.

    This lets CMDB administrators experience using Service Graph Workspace.

3.  Select **Show banner** in the Let other users try the new Service Graph Workspace.

    This shows a banner for all CMDB users, where they can select **Try new workspace** to also experience the use of Service Graph Workspace.

4.  In the Data Governance view in Service Graph Workspace, select **Switch now** in the Make the permanent switch to Service Graph Workspace banner.

    This sets the system to permanently use Service Graph Workspace instead of CMDB Workspace.


For information about the different views in Service Graph Workspace, see [Exploring Service Graph Workspace](exploring-sg-workspace.md).

## Access Service Graph Workspace

Use either of the following methods:

-   Navigate to **All** &gt; **Workspaces** &gt; **Service Graph Workspace**.
-   Select **All** in the navigation filter, and then enter `service graph workspace`.


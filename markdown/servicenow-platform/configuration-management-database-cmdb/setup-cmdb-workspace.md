---
title: Set up CMDB Workspace
description: Set up and access the CMDB Workspace store app.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Set up CMDB Workspace

Set up and access the CMDB Workspace store app.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Note:** The CMDB Workspace store app is automatically installed when installing or upgrading the product.

## Enable demo data

Enable demo data to install demo data-specific scheduled jobs that if the needed requirement is met, generates and populates demo data in CMDB Workspace cards such as:

-   Cloud vs Non-cloud resources chart in the CMDB Workspace landing page and the Insights view: If Cloud Service Accounts \[cmdb\_ci\_cloud\_service\_account\] table exists
-   Cards in the CMDB 360 view: If CMDB 360 is enabled
-   Cards in the Insights view, CMDB Feature Adoption tile:
    -   CIs processed by IRE
    -   CIs processed by IRE based on source
    -   Data Manager
    -   Data attestation
    -   Query Builder
    -   Intelligent Search
-   Cards in the What's new tile in the CMDB Workspace landing page.

To populate CMDB Workspace dashboards with demo data:

1.  When installing the CMDB Workspace store app, check **Load demo data**.
2.  Access the **\[Demo\] — CMDB Workspace demo data** scheduled job and select **Execute Now**.

**Note:** As a general practice, don't enable demo data in a production instance to prevent demo data mixing with real production data.

## Prerequisites

-   Plugins:

    -   Recommended:CSDM Activation \(com.snc.cmdb.csdm.activation\)

        Allows for legacy **Lifecycle Status** field mappings and synchronization to legacy status fields. For details about use and customization of retirement definitions when this plugin isn't activated, see [Retirement definitions](life-cycle-rules.md).

    -   Required \(activated by default\):CMDB CSDM Support \(com.snc.cmdb.csdm\)
    -   Required \(activated by default\): CMDB Page Templates \(sn\_cmdb\_pg\_templts\)
    -   Required \(activated by default\): CMDB NLQ Search Connected \(sn-cmdb-nlq-search\)
    For details about activating a plugin, see Activate a plugin.

-   Roles: To access the CMDB Workspace, you must, at a minimum, have one of the following roles, which are essential for interacting with the CMDB Workspace. Depending on which of these roles is assigned to you, you might only have access to some of the features available in the CMDB Workspace:

    -   sn\_cmdb\_admin
    -   sn\_cmdb\_editor
    -   sn\_cmdb\_user
    **Note:** As you drill down in the CMDB Workspace, there are some dashboards and list views that require specific roles in addition to the key CMDB Admin, CMDB Editor, or CMDB User roles.

-   Features: CMDB Workspace provides access to a wide range of applications and features. However, for CMDB Workspace to provide meaningful reports, overviews, and trends, you must set up and configure some of those features. Setup for such features is listed under Additional requirements.

## Access the CMDB Workspace

Navigate to **Workspaces** &gt; **CMDB Workspace** to access CMDB Workspace.

Home view is the default view of CMDB Workspace and you can also use other views to access CMDB features:

-   [Home view in CMDB Workspace](cmdb-workspace-home-view.md): View various CMDB Health aggregations, use Intelligent Search to search through the CMDB, see what changed in the CMDB, and access important tasks. This is the default view for CMDB Workspace.
-   [My Work view](cmdb-workspace-govern-view.md): Manage CMDB Data Manager tasks such as [attestation tasks](attesting-cis.md), that are assigned to you.
-   [CMDB 360 view](cmdb-workspace-cmdb360-view.md): View aggregations and analysis of CMDB 360 data on a dashboard, and create CMDB 360 queries.
-   [Management view](cmdb-workspace-mangmnt-view.md): View recent key activities and health indicators for the CMDB, and access management tools and dashboards \(accessible only to CMDB admins\) that support your management tasks.
-   [Insights view](cmdb-workspace-insights-view.md): View level of adoption of key CMDB tools, features, and application services. Explore benefits and install those tools and features to maximize the efficiency of your CMDB functionality.

**Parent Topic:**[Configuring CMDB Workspace](configuring-cmdb-workspace.md)


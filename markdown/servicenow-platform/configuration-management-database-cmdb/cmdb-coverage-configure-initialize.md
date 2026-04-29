---
title: Configure CMDB Coverage
description: Configure the CMDB Coverage application to assess and improve the quality of the CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CMDB Coverage, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure CMDB Coverage

Configure the CMDB Coverage application to assess and improve the quality of the CMDB.

## Before you begin

Dependencies and requirements:

-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../../configuration-management/concept/cmdb-ci-class-models.md).
-   The SGC Central \(sn\_sgc\_central\) application.

    The admin user role is required to install the application.

-   Optional: The Discovery \(com.snc.discovery\) plugin.

    This plugin must be activated to view the **Discovery schedule gap** widget in the CMDB Coverage dashboard. The admin user role is required for plugin activation.


Role required: sn\_cmdb\_admin

## Procedure

1.  Use one of the following methods to open the **Get started with CMDB Coverage** page:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** &gt; **Management tools** &gt; **CMDB Coverage Dashboard**.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **Quick links** &gt; **CMDB Coverage Dashboard**.
2.  For the Configure an IPAM connector activity, select one of the following options:

    -   If you have an IPAM connector installed but not yet configured, select **Configure**, and then configure a connector using SGC Central.

        For information about configuring a connector using SGC Central, see [Install a Service Graph Connector from ServiceNow Store in SGC Central](../../sgc-central/task/sgcc-install-store-connectors.md) and [Install a Service Graph Connector with an available entitlement in SGC Central](../../sgc-central/task/sgcc-install-sgc-entitlements.md).

    -   If you already have an IPAM connector configured or if IPAM data is populated in the CMDB from a different source, set the **Already configured or set up through another source** option to `true`.
3.  For the Initialize CMDB Coverage activity, select **Begin initialization**.

    For more information about the initialization process, see [CMDB Coverage initialization](../reference/cmdb-coverage-initialization.md).

    **Note:** The time required for the initialization process to finish depends on the volume of your data. The percentage of completion is displayed in the real-time progress tracker.

    After the application is initialized, the CMDB Coverage dashboard is displayed. You can view the CMDB coverage details on this dashboard.



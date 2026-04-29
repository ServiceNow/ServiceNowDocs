---
title: Exploring SGC Central
description: Learn about the SGC Central application with a sample workflow and review the benefits it can provide for different users in your organization.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring SGC Central

Learn about the SGC Central application with a sample workflow and review the benefits it can provide for different users in your organization.

## SGC Central overview

With the SGC Central application you can discover and install integration-ready Service Graph Connectors, monitor their connection performance and insights, ensure complete visibility into discovered sources and processed data, and access tools and resources for diagnosing and resolving connection issues. You access the application from the SGC Central view in the Service Graph Workspace or CMDB Workspace.

## SGC Central users

<table id="table_gws_mxy_m3c"><thead><tr><th>

User role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrator

</td><td>

Users with the admin role can install and upgrade Service Graph Connectors, including API Service Graph Connectors. Administrators can perform the following tasks:-   Create a connection and configure connection properties.
-   Monitor connections and data imports.
-   Manage connections.
-   Upgrade the connector.
-   Run background scripts.
-   Provide access to tables in the global scope.

</td></tr><tr><td>

SGC-admin

</td><td>

The sn\_cmdb\_int\_util.sgc\_admin user role has the second-highest level of permissions for Service Graph Connectors. SGC-admin users can perform the following tasks:-   Create, update, and delete connections.
-   Configure connectors using the guided setup.
-   Read and write the system properties that are used by the connectors.
-   Perform all operations that are allowed by other user roles that have lower levels of permission.

</td></tr><tr><td>

CMDB installation administrator

</td><td>

Users with the cmdb\_inst\_admin role can use [IntegrationHub ETL](../../configuration-management/concept/integrationhub-etl.md) to create and customize integrations. CMDB installation administrators can perform the following tasks:-   Read all Service Graph Connector application modules.
-   Read and write the system properties that are used by the connectors.
-   Create, update, and delete custom tables.
-   Create, update, and delete scheduled imports and data sources.
-   Read records that are owned by other applications and are related to the functionality of Service Graph Connectors \(for instance, records in the em\_event table\).

</td></tr></tbody>
</table>## SGC Central workflow

![Workflow describing various tasks a user with the admin or cmdb_inst_admin role can perform in SGC Central.](../image/sgc-central-infographic.png "Example workflow for the SGC Central users")

A user with the SGC-admin or admin role uses SGC Central to perform the following tasks:

1.  Based on the connection type, searches for a Service Graph Connector within the SGC Central view in Service Graph Workspace or CMDB Workspace.
2.  Selects a connector type and creates the connection using the playbook available for the connector.
    1.  Configures the properties for the connection.
    2.  Sets up import schedules for targeted data sources.
3.  Tracks the third-party data imported by the system using the connection into CMDB.
4.  Monitors the SGC Central dashboard for any errors in the connection or the data processing pipeline.
5.  Makes edits to the configuration or import schedules if needed.

## SGC Central benefits

<table id="table_wpg_ssy_nbc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Visualize connection status

</td><td>

Integrated dashboard to gain instant insights into the connection status of your connectors and performance, keeping your connections running smoothly. In addition, quickly debug for seamless integration.

</td><td>

Administrator, SGC-admin, CMDB installation administrator

</td></tr><tr><td>

Discover integration-ready connectors

</td><td>

Explore and install connectors based on the connection type requirements. See which connectors have new versions available and are eligible for upgrade.

</td><td>

Administrator

</td></tr><tr><td>

Manage connections intuitively

</td><td>

Create or modify connections to your needs.

</td><td>

Administrator, SGC-admin

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using SGC Central, see:

-   [Configuring SGC Central](sgcc-configuring.md)
-   [Managing connections added for Service Graph Connectors in SGC Central](sgcc-managing-connection.md)
-   [SGC Central reference](sgcc-reference.md)


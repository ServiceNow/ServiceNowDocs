---
title: Configure Power BI username and password authentication
description: Set up API permissions for username and password authentication to enable Power BI metadata collection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-username-auth.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prepare to run the PowerBI collector, PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Configure Power BI username and password authentication

Set up API permissions for username and password authentication to enable Power BI metadata collection.

## Before you begin

Role required: admin

You must have permissions to configure API permissions in Azure Active Directory.

**Note:** Only administrators of the tenant can grant admin consent.

## About this task

When using user authentication, the collector harvests all objects except personal workspaces, user workspaces, and report pages. To harvest all apps and workspaces in the tenant, enable Catalog all workspaces and apps in tenant. To include personal and user workspaces, enable Catalog contents of user's My Workspace.

To harvest report pages, grant the user access to each workspace. The admin API doesn’t have an endpoint for report pages.

**Note:** Catalog all workspaces and apps in the tenant requires the user to have Microsoft 365 Global Administrator or Power BI Service Administrator rights for metadata scanning. For details, see the [Power BI documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-admin-metadata-scanning).

## Procedure

1.  Navigate to the Azure Portal and open the application registration.

2.  Select **API Permissions**.

3.  Add Microsoft Graph permissions.

    1.  Select **Add a permission**.

    2.  Search for and select **Microsoft Graph**.

    3.  Add the following permissions.

        -   Application permission: Application.Read.All
        -   Delegated permission: User.Read \(assigned by default\)
4.  Add Power BI service permissions.

    1.  Select **Add a permission**.

    2.  Search for and select **Power BI service**.

    3.  Select **Delegated permissions**.

    4.  Add the following permissions.

        -   App.Read.All
        -   Dashboard.Read.All
        -   Dataflow.Read.All
        -   Dataset.Read.All
        -   Report.Read.All
        -   Tenant.Read.All
        -   Workspace.Read.All
5.  Select the **Grant admin consent** button located next to the **Add a permission** button.

    This permission enables the collector to run without asking you for permission on every run.


**Parent Topic:**[Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md)


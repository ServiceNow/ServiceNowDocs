---
title: Configure Power BI service principal authentication
description: Set up service principal authentication to enable Power BI metadata collection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prep-to-run-powerbi-collector-service-principal-auth.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prepare to run the PowerBI collector, PowerBI metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Configure Power BI service principal authentication

Set up service principal authentication to enable Power BI metadata collection.

## Before you begin

Role required: admin

You must be a Power BI administrator to enable service principal settings.

**Important:** When running under a service principal, there must be no Power BI admin-consent-required permissions set on your app. For more information, see the [Microsoft documentation](https://learn.microsoft.com/en-us/power-bi/enterprise/service-premium-service-principal).

## About this task

When using service principal authentication, the collector harvests all objects except personal workspaces, user workspaces, and report pages. To harvest all apps and workspaces in the tenant, enable Catalog all workspaces and apps in the tenant. To include personal and user workspaces, enable Catalog contents of user's My Workspace.

**Note:** To harvest report pages, grant the service principal access to each workspace. The admin API doesn’t have an endpoint for report pages.

## Procedure

1.  Sign in to Power BI using a Power BI Admin account.

2.  Navigate to **Settings** &gt; **Admin Portal**.

3.  Enable service principal API access.

    1.  Under **Developer settings**, locate **Service principals can use Fabric APIs**.

    2.  Enable the setting.

    3.  Select whether the setting applies to the entire organization or specific security groups.

        If using specific security groups, confirm that the group includes the service principal.

    4.  Select **Apply** to save the changes.

4.  Add the service principal to workspaces for dataflow and report page access.

    Dataflows require the service principal to have at least Contributor access to the workspace. For report pages, the service principal also needs workspace access because the admin API doesn’t provide an endpoint for report pages.

    1.  Open the workspace.

    2.  Select **Manage access**.

    3.  Search for the service principal or the security group the service principal belongs to.

    4.  Select the appropriate access level.

        If dataflows are used, select at least Contributor access. Otherwise, select Viewer.

    5.  Select **Add**.


**Parent Topic:**[Prepare to run the PowerBI collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/prepare-to-run-powerbi-collector.md)


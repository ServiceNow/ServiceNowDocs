---
title: Exploring CMDB Workspace
description: Learn more about CMDB Workspace, its different views, and its benefits when using key CMDB features such as CMDB Health, CMDB Data Manager, and CMDB 360.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/exploring-cmdb-workspace.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring CMDB Workspace

Learn more about CMDB Workspace, its different views, and its benefits when using key CMDB features such as CMDB Health, CMDB Data Manager, and CMDB 360.

## CMDB Workspace overview

The CMDB Workspace is an efficient, central, and modernized way for you to work. Use CMDB Workspace to search and explore the CMDB, examine health and recent activity, and access various CMDB dashboards and tools to support tasks in your organization.

## General interaction and additional information

-   CMDB Workspace leverages many [Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/pa-overview.md) capabilities and features, such as indicator sources. Throughout the CMDB Workspace views, you can select the various cards to drill down to Performance Analytics KPI Details panes that show trends for the associated data. On a KPI Details pane, you can modify different settings to change the scope of the data. You can also select **Show Records** to list the records associated with the chart.
-   Lists throughout the CMDB Workspace have a filter icon that you can select to show the filter definition used for the list.
-   You can [open your Configurable Workspace experience in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/open-your-configurable-workspace-experience-in-ui-builder.md) to access and edit your CMDB Workspace experience.
-   See [List of workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/list-of-workspaces.md) for a list of all Workspaces that ServiceNow® provides.
-   CMDB Workspace doesn't support domain separation.

## CI details

When you drill down to CI details, how those details appear depends on system settings:

-   **CI Form**

    By default, the system property **sn\_cmdb\_ws.explore\_ci.record.enabled** is set to **true**, enabling the experience of the CI Form feature for viewing CI details. Using CI Form, you're navigated to a centralized location with a comprehensive set of CI details organized by sections. Use the forms provided by CI Form to examine and edit CI attributes, relationships, tags, services and offerings, CMDB Health and CMDB 360 data associated with the CI, related lists, and activities. When updating CIs in CI Form, IRE rules are applied to avoid potential issues such as duplicate CIs.

    For more information, see:

    -   [Components installed with CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/installed-with-cmdb-workspace.md): **sn\_cmdb\_ws.explore\_ci.record.enabled** system property.
    -   [Manage CI details using CI Form in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/ci-form-cmdb-workspace.md).
-   **CI details pane**

    If **sn\_cmdb\_ws.explore\_ci.record.enabled** is set to **false**, then the CI details pane is used for viewing CI details.When you drill down to a CI record in CMDB Workspace views and pages, the following details for the CI appear:

    -   CI Timeline - Last 14 days: A timeline of CI activities such as change requests.

        **Note:** A CI timeline in CMDB Workspace fails to load when the number of any of the following activities exceeds its threshold:

        -   History: 200
        -   Incidents: 100
        -   Requests: 50
        -   Total Events: 200
        Select the **Open CI Timeline** link in the error message to open the CI timeline in the base system, which shows activities for the CI, up to the specified threshold numbers.

    -   CI Health: A summary of the health of the CI, showing related items such as critical incidents, incomplete attributes, and stale relationships for the CI.

        Role requirement: sn\_cmdb\_user oritil \(for accessing incidents\).

    -   Details: CI attributes, grouped into categories such as Key attributes, Asset attributes, Discovery attributes, Operational attributes, and More attributes.

        **Note:** Use the **CMDB - Workspace** form view for a CI class to configure which attributes appear.

    -   Activity: An activity stream to track what's changed in the CI record.
    -   Infrastructure Relationships: List of the infrastructure CIs related to the CI.
    -   Service Relationships: List of business applications, service offerings, and application services that the CI may be related to.
    On the CI details pane, you can:

    -   Select **Open Dependency View** to open the [Dependency Views](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/dependency-views/c_BusinesssServiceManagementMaps.md) map and display a graphic infrastructure view of the specific CI record.
    -   Select **View CMDB 360 Data** to show CMDB 360 details at the CI attribute level for the specific CI record.
    -   Select **Save** to save any changes made to attributes for the CI record.

    -   Select the More Actions icon \(...\) for additional functions:
        -   Select **Create Change** to [create a new change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/t_CreateAChange.md) for the CI record.
        -   Select **Create Incident** to [create a new incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/create-an-incident.md) for the CI record.
        -   Select **Delete** to delete the CI record.
<table id="table_cxt_nn4_mrb"><thead><tr><th>

UI activity

</th><th>

Additional requirements

</th></tr></thead><tbody><tr><td>

CI Details

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

 

</td></tr><tr><td>

CI Health

 Accessible to:

-   Incidents card: sn\_incident\_read to view
-   Change requests card: sn\_change\_read to view
-   For remaining cards: At least sn\_cmdb\_user


</td><td>

itil

</td></tr><tr><td>

Related Open Changes

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

sn\_change\_read role

</td></tr><tr><td>

Related Incidents

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

sn\_incident\_read role

</td></tr><tr><td>

Related Alerts

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

Event Management \(com.glideapp.itom.snac\) plugin

 evt\_mgmt\_user role

 [Set up Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/c_EMConfiguration.md)

</td></tr><tr><td>

Related Application Services

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

app\_service\_user role

</td></tr><tr><td>

View CMDB 360 Data

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

[Enable and configure CMDB 360](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/multisource-cmdb.md)

</td></tr><tr><td>

Save

 Accessible to: CMDB Admin

</td><td>

 

</td></tr><tr><td>

More Actions/Delete

 Accessible to: CMDB Admin

</td><td>

 

</td></tr></tbody>
</table>
## Shared pages

For information about the shared pages, see the Dev site as follows:

-   [CI Service Relationships](https://developer.servicenow.com/dev.do#!/reference/now-experience/utah/now-components/ci%20service%20relationships/overview)
-   [CI Infrastructure Relationships](https://developer.servicenow.com/dev.do#!/reference/now-experience/utah/now-components/ci%20infrastructure%20relationships/overview)

## What to explore next

To learn more about configuring and using CMDB Workspace, see:

-   CMDB views:
    -   [Home view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace-home-view.md)
    -   
    -   
    -   
    -   
    -   [SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-landing.md) view in CMDB Workspace \(if installed\)
-   [Configuring CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/configuring-cmdb-workspace.md)
-   [Resume a disabled Cloud vs Non-cloud resources scheduled job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace-resume-cloud-job.md)
-   [Edit a related table from CMDB performance insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/insights-update-record-rltd-table.md)
-   [Edit a scheduled data import from CMDB performance insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/insights-schedule-data-import.md)
-   [Components installed with CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/installed-with-cmdb-workspace.md)

-   **[Home view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace-home-view.md)**  
Home view is the default view in CMDB Workspace. It shows important tasks that you should tend to, various counts for activities in CMDB such as new CIs, CMDB Health aggregations, and various charts. The Home view also provides several links with immediate access to key CMDB tools.
-   **[SGC view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-ingestion-view.md)**  
The Overview page in the Ingestion view in Service Graph Workspace provides a centralized dashboard view for administrators to monitor the installation, performance, and error handling of Service Graph Connectors.
-   **[Governance view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-governance-view.md)**  
Governance view in CMDB Workspace provides administrators with important information, actions, and links to tools that are used to manage, monitor, and administer data ingestion and other CMDB functions.
-   **[Explore and Search view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-search-explore-view.md)**  
Search through CMDB tables without having detailed knowledge of the CMDB data model by using contexts that are mapped to CI classes as navigation. Use natural language with the AI-driven search to search the CMDB and related data.
-   **[Tasks view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-tasks-view.md)**  
The Task view in CMDB Workspace provides task owners access for tracking and managing their tasks such as CMDB Health related tasks, certification, attestation, and lifecycle tasks generated by the CMDB Data Manager.
-   **[Insights view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-insights-view.md)**  
View insightful dashboards that show aggregated counts, state, and health for key features such as CMDB Health, Service Instances, and CMDB 360.
-   **[Data Owner view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-data-owner-home-view.md)**  
Data Owner view in CMDB Workspace provides a filtered view for data owner users who own, manage, or support CIs. It provides those users with a simple method to browse their CIs, view health, related activity associated with their CIs, understand what their CIs support, and access to actions they're authorized to use for their CIs.
-   **[Lists view in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/sg-workspace-lists-view.md)**  
The Lists view in CMDB Workspace provides access to CIs within the CMDB hierarchy and to records in tables that aren't descendants of the Configuration Item \[cmdb\_ci\] table, but are important in the CMDB ecosystem.
-   **[Configuration identifiers framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/configuration-identifiers-framework.md)**  
Configuration identifiers provide a framework that lets you customize some behaviors of a CMDB Workspace feature, enabling different settings for that feature, on different workspaces. Most importantly, you can use this customization framework when integrating a CMDB Workspace feature into another workspace.

**Parent Topic:**[CMDB Workspace store app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md)


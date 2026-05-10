---
title: Exploring Service Graph Workspace
description: Learn more about Service Graph Workspace, its different views and insight dashboards, when using key CMDB features such as CMDB Health, CMDB Data Manager, and CMDB 360.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring Service Graph Workspace

Learn more about Service Graph Workspace, its different views and insight dashboards, when using key CMDB features such as CMDB Health, CMDB Data Manager, and CMDB 360.

## Service Graph Workspace overview

The Service Graph Workspace is an efficient, central, and modernized way for you to work with the underlying graph database that includes CIs, services, and related data such as company and location data. Use Service Graph Workspace to search and explore the CMDB, examine health and recent activity, and access various insight dashboards and tools to support tasks in your organization.

## Guided Tour

Administrators assigned to the guided tour admin role \(guided\_tour\_admin\) can use the Guided Tour Designer to create step-by-step walkthroughs that can guide users through the Service Graph Workspace. For more information, see [Guided Tours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/guided-tours.md).

## General interaction and additional information

-   Service Graph Workspace leverages many [Performance Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/pa-overview.md) capabilities and features, such as indicator sources. Throughout the Service Graph Workspace views, you can select the various cards to drill down to Performance Analytics KPI Details panes that show trends for the associated data. On a KPI Details pane, you can modify different settings to change the scope of the data. You can also select **Show Records** to list the records associated with the chart.
-   Lists throughout the Service Graph Workspace have a filter icon that you can select to show the filter definition used for the list.
-   You can [open your Configurable Workspace experience in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/open-your-configurable-workspace-experience-in-ui-builder.md) to access and edit your Service Graph Workspace experience.
-   See [List of workspaces](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/list-of-workspaces.md) for a list of all Workspaces that ServiceNow® provides.
-   Service Graph Workspace doesn't support domain separation.

## Personas

The Service Graph Workspace is intended to support the following personas in performing their tasks:

|Persona|Description|Role|
|-------|-----------|----|
|CMDB administrator|Manages the configuration of CMDB, data ingestion, governance, and reporting, to ensure that the CMDB supports the needs of their organization.|sn\_cmdb\_admin|
|Data owner|Owns and manages data in CMDB. This persona is primarily focused on managing data that they own. However, this persona may also be associated with data owned by a group that the data owner user belongs to such as a Change and Managed by groups.|sn\_cmdb\_editor|
|Analyst|Investigates and analyzes data in support of their organization. Visits the workspace to search and browse CMDB data and to access insight reports.|sn\_cmdb\_user|

## CI details

When you drill down to CI details, how those details appear depends on system settings:

-   **CI Form**

    By default, the system property **sn\_cmdb\_ws.explore\_ci.record.enabled** is set to **true**, enabling the experience of the CI Form feature for viewing CI details. Using CI Form, you're navigated to a centralized location with a comprehensive set of CI details organized by sections. Use the forms provided by CI Form to examine and edit CI attributes, relationships, tags, services and offerings, CMDB Health and CMDB 360 data associated with the CI, related lists, and activities. When updating CIs in CI Form, IRE rules are applied to avoid potential issues such as duplicate CIs.

    For more information, see:

    -   [Components installed with Service Graph Workspace](../reference/installed-with-sg-workspace.md): **sn\_cmdb\_ws.explore\_ci.record.enabled** system property.
    -   [Manage CI details using CI Form in Service Graph Workspace](ci-form-sg-workspace.md).
-   **CI details pane**

    If **sn\_cmdb\_ws.explore\_ci.record.enabled** is set to **false**, then the CI details pane is used for viewing CI details.When you drill down to a CI record in Service Graph Workspace views and pages, the following details for the CI appear:

    -   CI Timeline - Last 14 days: A timeline of CI activities such as change requests.

        **Note:** A CI timeline in Service Graph Workspace fails to load when the number of any of the following activities exceeds its threshold:

        -   History: 200
        -   Incidents: 100
        -   Requests: 50
        -   Total Events: 200
        Select the **Open CI Timeline** link in the error message to open the CI timeline in the base system, which shows activities for the CI, up to the specified threshold numbers.

    -   CI Health: A summary of the health of the CI, showing related items such as critical incidents, incomplete attributes, and stale relationships for the CI.

        Role required: sn\_cmdb\_user oritil \(for accessing incidents\)

    -   Details: CI attributes, grouped into categories such as Key attributes, Asset attributes, Discovery attributes, Operational attributes, and More attributes.

        **Note:** Use the **CMDB - Workspace** form view for a CI class to configure which attributes appear.

    -   Activity: An activity stream to track what's changed in the CI record.
    -   Infrastructure Relationships: List of the infrastructure CIs related to the CI.
    -   Service Relationships: List of business applications, service offerings, and application services that the CI may be related to.
    On the CI details pane, you can:

    -   Select **Open Dependency View** to open the [Dependency Views](../../business-service-management-map-ng/concept/c_BusinesssServiceManagementMaps.md) map and display a graphic infrastructure view of the specific CI record.
    -   Select **View CMDB 360 Data** to show CMDB 360 details at the CI attribute level for the specific CI record.
    -   Select **Save** to save any changes made to attributes for the CI record.

    -   Select the More Actions icon \(...\) for additional functions:
        -   Select **Create Change** to [create a new change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateAChange.md) for the CI record.
        -   Select **Create Incident** to [create a new incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/create-an-incident.md) for the CI record.
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

 [Set up Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/c_EMConfiguration.md)

</td></tr><tr><td>

Related Application Services

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

app\_service\_user role

</td></tr><tr><td>

View CMDB 360 Data

 Accessible to: CMDB Admin, CMDB Editor, CMDB User

</td><td>

[Enable and configure CMDB 360](multisource-cmdb.md#section_enable_multisource_CMDB)

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

To learn more about configuring and using Service Graph Workspace, see:

-   Views:
    -   [Data Owner Home view in Service Graph Workspace](sg-workspace-data-owner-home-view.md)
    -   [Governance view in Service Graph Workspace](sg-workspace-governance-view.md)
    -   [Explore and Search view in Service Graph Workspace](sg-workspace-search-explore-view.md)
    -   [Insights view in Service Graph Workspace](sg-workspace-insights-view.md)
    -   [Tasks view in Service Graph Workspace](sg-workspace-tasks-view.md)
    -   [Lists view in Service Graph Workspace](sg-workspace-lists-view.md)
    -   [SGC Central](../../sgc-central/reference/sgcc-landing.md) \(if installed\)
    -   [CMDB success advisor](../../cmdb-success-advisor/reference/cmdb-sa.md) \(if installed\)
-   [Configuring Service Graph Workspace](configuring-sg-workspace.md)
-   [Resume a disabled Cloud vs Non-cloud resources scheduled job](../task/sg-workspace-resume-cloud-job.md)
-   [Edit a related table from CMDB performance insights in Service Graph Workspace](../task/sginsights-update-record-rltd-table.md)
-   [Edit a scheduled data import from CMDB performance insights in Service Graph Workspace](../task/sg-insights-schedule-data-import.md)
-   [Components installed with Service Graph Workspace](../reference/installed-with-sg-workspace.md)


---
title: Exploring CMDB Workspace
description: Learn more about CMDB Workspace, its different views, and its benefits when using key CMDB features such as CMDB Health, CMDB Data Manager, and CMDB 360.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Exploring CMDB Workspace

Learn more about CMDB Workspace, its different views, and its benefits when using key CMDB features such as CMDB Health, CMDB Data Manager, and CMDB 360.

## CMDB Workspace overview

The CMDB Workspace is an efficient, central, and modernized way for you to work. Use CMDB Workspace to search and explore the CMDB, examine health and recent activity, and access various CMDB dashboards and tools to support tasks in your organization.

## General interaction and additional information

-   CMDB Workspace leverages many [Performance Analytics](https://www.servicenow.com/docs/access?context=pa-overview&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) capabilities and features, such as indicator sources. Throughout the CMDB Workspace views, you can select the various cards to drill down to Performance Analytics KPI Details panes that show trends for the associated data. On a KPI Details pane, you can modify different settings to change the scope of the data. You can also select **Show Records** to list the records associated with the chart.
-   Lists throughout the CMDB Workspace have a filter icon that you can select to show the filter definition used for the list.
-   You can [open your Configurable Workspace experience in UI Builder](https://www.servicenow.com/docs/access?context=open-your-configurable-workspace-experience-in-ui-builder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) to access and edit your CMDB Workspace experience.
-   See [List of workspaces](https://www.servicenow.com/docs/access?context=list-of-workspaces&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) for a list of all Workspaces that ServiceNow® provides.
-   CMDB Workspace doesn't support domain separation.

## CI details

When you drill down to CI details, how those details appear depends on system settings:

-   **CI Form**

    By default, the system property **sn\_cmdb\_ws.explore\_ci.record.enabled** is set to **true**, enabling the experience of the CI Form feature for viewing CI details. Using CI Form, you're navigated to a centralized location with a comprehensive set of CI details organized by sections. Use the forms provided by CI Form to examine and edit CI attributes, relationships, tags, services and offerings, CMDB Health and CMDB 360 data associated with the CI, related lists, and activities. When updating CIs in CI Form, IRE rules are applied to avoid potential issues such as duplicate CIs.

    For more information, see:

    -   [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md): **sn\_cmdb\_ws.explore\_ci.record.enabled** system property.
    -   [Manage CI details using CI Form in CMDB Workspace](ci-form-cmdb-workspace.md).
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

    -   Select **Open Dependency View** to open the [Dependency Views](../../business-service-management-map-ng/concept/c_BusinesssServiceManagementMaps.md) map and display a graphic infrastructure view of the specific CI record.
    -   Select **View CMDB 360 Data** to show CMDB 360 details at the CI attribute level for the specific CI record.
    -   Select **Save** to save any changes made to attributes for the CI record.

    -   Select the More Actions icon \(...\) for additional functions:
        -   Select **Create Change** to [create a new change request](https://www.servicenow.com/docs/access?context=t_CreateAChange&version=australia&pubname=australia-it-service-management&ft:locale=en-US) for the CI record.
        -   Select **Create Incident** to [create a new incident](https://www.servicenow.com/docs/access?context=create-an-incident&version=australia&pubname=australia-it-service-management&ft:locale=en-US) for the CI record.
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

 [Set up Event Management](https://www.servicenow.com/docs/access?context=c_EMConfiguration&version=australia&pubname=australia-it-operations-management&ft:locale=en-US)

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

To learn more about configuring and using CMDB Workspace, see:

-   CMDB views:
    -   [Home view in CMDB Workspace](cmdb-workspace-home-view.md)
    -   [My Work view in CMDB Workspace](cmdb-workspace-govern-view.md)
    -   [CMDB 360 view in CMDB Workspace](cmdb-workspace-cmdb360-view.md)
    -   [Insights view in CMDB Workspace](cmdb-workspace-insights-view.md)
    -   [Management view in CMDB Workspace](cmdb-workspace-mangmnt-view.md)
    -   [SGC Central](../../sgc-central/reference/sgcc-landing.md) view in CMDB Workspace \(if installed\)
-   [Configuring CMDB Workspace](configuring-cmdb-workspace.md)
-   [Resume a disabled Cloud vs Non-cloud resources scheduled job](../task/cmdb-workspace-resume-cloud-job.md)
-   [Edit a related table from CMDB performance insights](../task/insights-update-record-rltd-table.md)
-   [Edit a scheduled data import from CMDB performance insights](../task/insights-schedule-data-import.md)
-   [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md)

-   **[Home view in CMDB Workspace](cmdb-workspace-home-view.md)**  
Home view is the default view in CMDB Workspace. It shows important tasks that you should tend to, various counts for activities in CMDB such as new CIs, CMDB Health aggregations, and various charts. The Home view also provides several links with immediate access to key CMDB tools.
-   **[My Work view in CMDB Workspace](cmdb-workspace-govern-view.md)**  
Use the My Work view in CMDB Workspace to manage your tasks. Tasks in this view are related to data compliance such as attestation, certification, and other life-cycle tasks.
-   **[CMDB 360 view in CMDB Workspace](cmdb-workspace-cmdb360-view.md)**  
The CMDB 360 dashboard provides aggregations and analysis of CMDB 360 data. CMDB 360 collects data about all the discovery sources reporting attribute values for CIs. Use the CMDB 360 view in CMDB Workspace to track activities and identify potential issues of discovery sources. You can also create your own queries and associated schedules and reportsto explore CMDB 360 data.
-   **[Insights view in CMDB Workspace](cmdb-workspace-insights-view.md)**  
Use the Insights view in CMDB Workspace to see and increase the level of adoption of key CMDB features and application services to improve the overall health of the CMDB. Explore how tools and features can maximize the health and efficiency of your CMDB and use direct links to install and start using features immediately.
-   **[Management view in CMDB Workspace](cmdb-workspace-mangmnt-view.md)**  
The Management view provides CMDB Admins with quick access to key management tools and deep insights into CMDB health and activities. The view provides details such as duplicate CIs and recent activities in the CMDB.
-   **[Configuration identifiers framework](configuration-identifiers-framework.md)**  
Configuration identifiers provide a framework that lets you customize some behaviors of a CMDB Workspace feature, enabling different settings for that feature, on different workspaces. Most importantly, you can use this customization framework when integrating a CMDB Workspace feature into another workspace.

**Parent Topic:**[CMDB Workspace store app](cmdb-workspace.md)


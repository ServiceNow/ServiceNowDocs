---
title: Home view in CMDB Workspace
description: Home view is the default view in CMDB Workspace. It shows important tasks that you should tend to, various counts for activities in CMDB such as new CIs, CMDB Health aggregations, and various charts. The Home view also provides several links with immediate access to key CMDB tools.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 21
breadcrumb: [Explore, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Home view in CMDB Workspace

Home view is the default view in CMDB Workspace. It shows important tasks that you should tend to, various counts for activities in CMDB such as new CIs, CMDB Health aggregations, and various charts. The Home view also provides several links with immediate access to key CMDB tools.

For Administrators, banners appear letting administrators try out Service Graph Workspace and also configuring the system to let users try Service Graph Workspace. For information about switching into permanently using Service Graph Workspace, see [Set up Service Graph Workspace](setup-service-graph-workspace.md).

## Access

Role requirements: sn\_cmdb\_admin \(CMDB Admin\), sn\_cmdb\_editor \(CMDB Editor\), or sn\_cmdb\_user \(CMDB User\).

To access the Home view, navigate to **Workspaces** &gt; **CMDB Workspace** and then select **Home** in the CMDB Workspace menu bar.

## Now Assist for CMDB

Select the Now Assist icon ![](../image/ai-sparkle-cmdb.png) to access Now Assist for CMDB skills, agents, and agentic workflows.

For more information, see [Now Assist for Configuration Management Database \(CMDB\)](now-assist-landing-cmdb.md).

## Intelligent Search

Accessible to: CMDB Admin, CMDB Editor, CMDB User.

Lets you use Natural Language Query \(NLQ\) search capabilities provided by [Intelligent Search for CMDB](intelligent-search-cmdb.md). Use the input field to construct a search string using everyday language. As you type, a dynamic list of relevant suggestions appears, with items matching single words or part phrases in the typed-in text, such as table names.

You can:

-   Select **Search tips** to see tips about constructing search strings. See details about the usage, examples for single and multi-table search, advanced filtering, and relationships in Intelligent Search.
-   Select **Search** to either run the query if the search string is already fully converted into a valid CMDB query, or to open the Refine your query dialog box.
    -   If the search string has no ambiguities with the table name or relationships, then the query runs and the results appear in a list view format.

        Only the first 100 results of the query appear in the results pane.

        -   Select **Load More Results** to view the next set of 100 results.
        -   Select **Load All Results** to view the rest of the query results, up to the number specified by the [glide.cmdb.query.max\_results\_limit](../reference/cmdb-querybldr-sysproprties.md) system property \(10,000 by default\).
        If the constructed CMDB query contains more than a single table, then the **View in Query Builder** button appears. Select the button to open the [CMDB Query Builder](querying-cmdb.md) with your query fully constructed on the Query Builder canvas. You can use the Query Builder to continue editing the query.

    -   If there are any ambiguities with table names or relationship types in the search string, then the search string can't be converted into a valid CMDB query. In this case, the Refine your query dialog box appears letting you select from suggested CI classes and continue to parse your search string into a valid CMDB query. Those suggested CI classes are based on phrases in your search string. Use the drop-down lists to select the CI classes that match your intended search and then select **View search results** to run the query.
    -   If Intelligent Search is unable to convert your search string into a valid CMDB query, then selecting **Search** doesn't generate any query results. Instead, a feedback form appears. Fill out the form and select **Submit Feedback** to record your feedback for your CMDB Admin to review.
-   Use the Sample searches list to get you started in running a pre-defined search. This list consists of more common searches, or searches that are more difficult to construct such as searches that involve application services.
-   Use the Your recent searches list to rerun a previous search.
-   Select **Results Feedback** to submit feedback on the search results for your CMDB Admin to review.

For more details about using NLQ with Intelligent Search, see [Intelligent Search for CMDB](intelligent-search-cmdb.md).

Alternatively, you can select **Use conditional search instead** to use a basic [condition builder](https://www.servicenow.com/docs/access?context=create-related-list-query&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) functionality where you can specify conditions to search for CIs of a specific class.

You can:

-   Select **New condition set** to add a condition phrase.
-   Select **Related List Condition** to [add a condition phrase for related lists](https://www.servicenow.com/docs/access?context=create-related-list-query&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).
-   Select **Search** to search through the CMDB.
-   Add and then adjust the **sn\_cmdb\_ws.list.record\_count\_limit** system property to limit the record count summation and so to minimize the performance impact of that operation. The record count shows on the Conditional search page, for example, above the results list. For more information about adding and modifying that system property, see [Components installed with CMDB Workspace](../reference/installed-with-cmdb-workspace.md).

In the results list, select a CI to see its details.

<table id="table_tdz_dnw_v5b"><thead><tr><th>

UI activity

</th><th>

Additional requirements

</th></tr></thead><tbody><tr><td>

-   Mapped Application Service
-   Application Service
-   Application Service Group
-   Dynamic CI Group
-   Tag Based Service

</td><td>

app\_service\_user role

</td></tr><tr><td>

-   Business Service
-   Technical Service
-   Application Service Outage

</td><td>

service\_viewer role

</td></tr></tbody>
</table>## Important actions

Accessible to: CMDB Admin and CMDB Editor.

Important actions of various categories that require your attention or action. There are several task categories such as:

-   Health tasks generated by [CMDB Health](c_CMDBHealth.md): In health-related cards, such as Duplicate CIs, Orphan CIs, stale CIs, and De-Duplication tasks, select **View CIs** or **View Tasks** to show the list of associated CIs or important tasks.In the CI list view page, you can select **CMDB Health Dashboard** to open the CMDB Health Dashboard. In de-duplication-related cards generated by [IRE](id-detect-dup-ci.md), you can access the De-duplication dashboard and de-duplication libraries, to remediate de-duplication tasks in bulk.
-   Data attestation and life cycle approval tasks generated by the [CMDB Data Manager](cmdb-data-management.md): In data attestation-related cards, such as Reassignment Requests and Unassigned Overdue cards, select **View Tasks** to drill down to the associated important tasks.

Important actions are stored in the CMDB WS Imp Action Card Config \[sn\_cmdb\_ws\_imp\_action\_card\_config\] table that is accessible for editing only to users with the sn\_cmdb\_admin role. Authorized users can modify attributes of an important action such as **Active** and **Filter conditions**, but can't modify the **Type**, **Persona**, and **Table** attributes.

-   Important action cards show per the logged in user role, as specified in the CMDB WS Imp Action Card Config \[sn\_cmdb\_ws\_imp\_action\_card\_config\] table.
-   A card appears only if there is at least one record that meets the card's filter condition.
-   If you drill down a Health-related card and modify an associated CI, any resulting impact to health KPIs might appear only after the next cycle of the [CMDB Health dashboard jobs](../task/t_EnableCMDBHealthDashboardJob.md).

For information about managing the cards in the Important actions tile, see [Modify important actions on the Home view of CMDB Workspace](../task/cmdb-workspace-edit-imp-action.md).

## What's new

Accessible to: CMDB Admin, CMDB Editor, CMDB User.

Counts of newly created CIs within a recent time interval. The New CIs total counts all CI types including applications, hardware, and application services, which also appear in separate cards in the tile. By default, historical data is aggregated for the **Last 24 hours**, which you can set to a different time interval such as **Last 7 days**.

Select a card to drill down to a Performance Analytics KPI Details pane that shows the trend for the respective item.

Counts in the What's new cards are based on the following tables:

|Count|Table|
|-----|-----|
|New CIs|Configuration Item \[cmdb\_ci\]|
|New application|Application \[cmdb\_ci\_appl\]|
|New hardware|Hardware \[cmdb\_ci\_hardware\]|
|New application services|Service Instance \[cmdb\_ci\_service\_auto\]|

## CI overview

The following tabs provide summaries about CIs:

-   **CI Summary**

    Accessible to: CMDB Admin, CMDB Editor, CMDB User \(without tabs\).

    A chart of all CIs in the CMDB, grouped by up to 20 CMDB groups. The CMDB groups in the chart are specified as groups of closely-related classes. On this chart, you can:

    -   Select a bar to drill down to the classes in the group and their CIs.
    -   Drill down a CI to show the CI form with a timeline, health overview, and several types of attributes such as key and discovery attributes.
    -   Drill down a class to access the Create CI experience to create a new CI in the selected class. For more information about the Create CI experience which applies Identification and Reconciliation Engine \(IRE\) processes, see [Create a CI manually in CMDB Workspace](../task/create-ci-manual-cmdb-workspace.md).
    -   Add custom class groups by creating [CMDB groups](cmdb-groups.md#) with the following settings:

        -   Group type is set to 'CMDB Workspace'.
        -   Populated by encoded queries.
        Such custom class groups will appear after the next time that the **CMDB Workspace – Group** and **Encoded Query Counts** scheduled jobs run and update the CMDB Workspace.

    **Note:**

    In systems with a very large number of CIs, for example a billion or more CIs, the set of queries that populate the CI Overview widget might run for an unreasonable length of time. In that case, you can choose to switch the default queries with a set of simpler queries that can handle such load and properly load the CI Overview widget. However, the results yielded from the simpler queries aren't as complete or accurate as the results of the original queries. A fundamental difference between the original and the simpler queries is that the simpler queries use only [Common Service Data Model \(CSDM\)](../../csdm-implementation/concept/csdm-landing-page.md) attributes for CI status \(such as **life\_cycle\_stage**\), while the default queries also use the legacy **operational\_status** and **status** attributes. In an environment that hasn't migrated to CSDM, the simple queries yield fewer results.

    You can examine \(read access only\) the simple query in the **Simple Condition** column in the **cmdb\_group\_contains\_encoded\_query** table.

    To use the simpler set of queries, set the **sn\_cmdb\_ws.ci\_overview.enable\_simple\_condition** system property to **true** \(**false** by default\).

-   **My CIs**

    Accessible to: CMDB Admin, CMDB Editor.

    A chart of Cls with **Managed By Group** being one of the groups you are a part of. CIs are grouped by up to 20 common class categories such as **Applications**, **Devices**, and **Servers**. If there are more than 20 classes to show, then all remaining classes are lumped into one additional bar on the chart.

    Select a class bar to drill down into the CIs for the class. Then drill down to a CI's form with a timeline, health overview, and several types of attributes such as key and discovery attributes.

    Use the [sn\_cmdb\_ws.ci\_overview.managed\_by\_me.enabled​](../reference/installed-with-cmdb-workspace.md) property to show or hide this chart.

-   **Cloud vs Non-cloud resources**

    Charts showing counts and details for resources that are hosted on various cloud services versus those resources that aren't, with breakdown by key CI classes such as applications, databases, and datacenters. Resources can be deployed on cloud services such as the Microsoft Azure Cloud, or on the local instance or other non-cloud solutions. For some ongoing operations in the organization, it might be necessary to have those details that can be difficult to obtain.

    The following conditions must be met for the Cloud vs Non-cloud resources charts to appear and to show meaningful data:

    -   The table Cloud Service Accounts \[cmdb\_ci\_cloud\_service\_account\] must exist.
    -   The Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] table must contain at least one record for a cloud datacenter.
    -   The Datacenter Types \[sn\_cmdb\_ws\_datacenter\_type\] table must contain at least one record for a datacenter that is classified as cloud storage in the organization. In the base system, this table is pre-populated with several records for common cloud services such as the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] class. The chart calculates and shows data only for cloud services for which there's a record in the Datacenter Types \[sn\_cmdb\_ws\_datacenter\_type\] table.

        For details about adding datacenters in your organization, with the cloud or non-cloud classification, see [Configure datacenters for Cloud vs Non-cloud resources](../task/cmdb-workspace-config-datacenter.md).

    The following cloud vs Non-cloud charts are available:

    -   CI classes bar chart:

        Each bar in the CI classes chart represents a pair of a CI class and a storage type \(cloud, non-cloud\), such as the bar for Applications/Cloud. For each bar, there's a scheduled job that runs every 24 hours to collect and calculate the data for the bar. The running time depends on the amount and complexity of the data that a job collects, which can be different for each scheduled job. Also, the schedules of the jobs are staggered so that they don't all run at the same time and exhaust resources. For details about the class-specific criteria used for the chart calculations, see [Class criteria in Cloud vs Non-cloud resources chart](../reference/criteria-cloud-resources-chart.md).

        If there’s a CI class/type pair that isn't important in the organization, you can exclude that pair from the CI classes chart. For more details, see [Configure classes for Cloud vs Non-cloud resources](../task/cmdb-workspace-config-classes-cloud.md).

        On the CI classes chart, you can:

        -   Select a bar to open the Cloud vs Non-cloud resources pane. Then, select either of the following tabs to drill down into further details for the bar:

            -   **Cloud vs Non-cloud CIs**

                Shows a bar chart for CIs stored on a cloud service and those CIs that aren't, per CI class. For each CI class, select the cloud or the non-cloud bar to show the CIs that are associated with the selected bar, in a list view. You can then select a CI to see its details.

            -   **CI Classes by Cloud Providers**

                Pie charts per CI class with more granular details for those CIs that are hosted on cloud providers. Pie slices have randomly-selected colors, and they show a breakdown by cloud providers for various CI classes. For each pie, select a slice to show the CIs that are associated with the pie slice, in a list view. You can then select a CI to see its details.

        -   Select **Latest updates** to see updated status for the scheduled jobs that produce the data for the chart. Status is color-coded to indicate whether the job has completed successfully \(green\), or failed to complete \(red\).

    -   Application Services pie chart:

        The Application Services pie chart uses the Service Configuration Item Associations \[svc\_ci\_assoc\] table and checks the cloud/non-cloud status of application service CIs in the CI classes chart. Application services in the Application Services pie chart are classified as follows:

        -   Cloud: All of the CIs in the application service have been determined to be hosted on a cloud service.
        -   Non-cloud: All of the CIs in the application service have been determined not to be hosted on a cloud service.
        -   Hybrid: The application service contains a mixture of CIs where some are hosted and some aren't hosted on cloud services.
        -   Unknown: The cloud/non-cloud classification couldn't be determined because some of the application service CIs aren't classified as cloud or non-cloud CIs.
        **Note:** Because classification of Application Services depends on the classification of CIs in the CI classes chart, there might be some discrepancy between the two charts. This can occur if an application service CI changed its cloud/non-cloud status, and the Application Services chart hasn't refreshed yet to reflect that change.

        Select the Application Services chart to access the list views of the associated application services, grouped by cloud/non-cloud classifications. From those list views, you can drill down to the [Dependency Views](../../business-service-management-map-ng/concept/c_BusinesssServiceManagementMaps.md) map for application services.

    The scheduled jobs associated with the charts are set up with several hard-coded limits that if exceeded, result in failure conditions that are reflected in the job status. Timing out is set to two hours and the maximum number of records to collect is set to 500,000. If a job exceeds any of those limits, it's automatically stopped.

    A scheduled job that can't complete for 3 \(default\) consecutive days is automatically disabled for future runs. You can manage the disabling of scheduled jobs, in the following ways:

    -   Modify the default number of consecutive days that are counted by adding the **sn\_cmdb\_ws.insight.category.disable\_after\_failure** system property to the System Properties \[sys\_properties\] table and then setting its value. For more details, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).
    -   [Resume a disabled scheduled job](../task/cmdb-workspace-resume-cloud-job.md).

<table id="table_jkk_2ln_x5b"><thead><tr><th>

UI activity

</th><th>

Additional requirements

</th></tr></thead><tbody><tr><td>

-   Mapped Application Service view
-   Application Service
-   Dynamic CI Group
-   Tag Based Service

</td><td>

app\_service\_user role

</td></tr></tbody>
</table>## My work

Accessible to: CMDB Admin, CMDB Editor, CMDB User.

All open tasks from [CMDB Data Manager](cmdb-data-management.md) that are assigned to you, or to an assigned group in the **Managed by Group** attribute which you are a member of. For CMDB Admins, also tasks that aren't assigned to anyone so that CMDB Admins can assign those unassigned tasks. Tasks can be, for example, attestation tasks and life cycle-related tasks.

Select **Open tasks** and **Overdue tasks** to review and process the tasks.

## CMDB Health

Accessible to: CMDB Admin, CMDB Editor, CMDB User.

KPIs health scores calculated by CMDB Health for CIs. Select a percentage number for a KPI to navigate to the KPIs tile on the CMDB Health Dashboard.

For more information, see [CMDB Health](c_CMDBHealth.md), [CMDB Health KPIs and metrics](../reference/r_CMDBHealthMetrics.md).

<table id="table_plv_b34_mrb"><thead><tr><th>

UI activity

</th><th>

Additional requirements

</th></tr></thead><tbody><tr><td>

CMDB Health

</td><td>

asset or itil role

 [Configuring CMDB Health](c_CMDBHealthSetupandConfig.md)

</td></tr></tbody>
</table>## Quick links

A list of links to key CMDB dashboards and tools. You can [add a link](../task/cmdb-workspace-add-quick-link.md) to the list of quick links that are available to you.

-   [Dependency Views](../../business-service-management-map-ng/concept/c_BusinesssServiceManagementMaps.md): Provides a graphic infrastructure view for a CI and any application or business services that it’s part of and that it supports.
-   [Query Builder](querying-cmdb.md): Easily build complex infrastructure and service queries, that span multiple CMDB classes, non-CMDB tables, and that can involve many CIs that are connected by different relationships.
-   [Data Manager](cmdb-data-management.md): Centrally create, edit, review, publish, and track Data Manager policies and the tasks generated by the policies.
-   CI Class List: List view of CMDB CIs grouped by common classes.
-   [Unified Map](cmdb-workspace-unified-map.md): Graphical map showing the hierarchy of CIs and the relationships between them, and application services. Directly from the map, you can access attributes of CIs and relationships, and related items such as changes, incidents, and problems for a CI.
-   [CMDB Health Dashboard](c_MonitorCMDBHealth.md): View CMDB Health reports and configure the CMDB health KPIs and metrics that CIs are evaluated by in CMDB Health dashboards.
-   [Relationship Health Dashboard](../task/t_ViewRelationshipsHealth.md): View the Relationship Health Dashboard with CMDB Health scores for CI relationship.
-   [Create CI](../task/create-ci-manual-cmdb-workspace.md): Create a new CI while enforcing Identification and Reconciliation Engine \(IRE\) processes and other requirements that result in a valid and unique CI.
-   [Data Certification Dashboard](data-cert-dashboard-workspace.md): View Data Certification instances, tasks and status such as past due certification tasks. Drill down to specific tasks to reassign them for faster resolution.

<table id="table_wks_yz3_krb"><thead><tr><th>

UI activity

</th><th>

Accessibility

</th><th>

Additional requirements

</th></tr></thead><tbody><tr><td>

Dependency View

</td><td>

CMDB Admin, CMDB Editor, CMDB User

</td><td>

dependency\_views role

</td></tr><tr><td>

Query Builder

</td><td>

CMDB Admin, CMDB Editor, CMDB User

</td><td>

cmdb\_query\_builder\_read role

</td></tr><tr><td>

Data Manager

</td><td>

CMDB Admin

</td><td>

 

</td></tr><tr><td>

Add or edit a custom quick link

</td><td>

CMDB Admin, CMDB Editor, CMDB User

</td><td>

 

</td></tr></tbody>
</table>-   **[Cloud vs Non-cloud resources chart](cmdb-workspace-ci-overview-cloud.md)**  
The Cloud vs Non-cloud resources chart appears on the Home view in CMDB Workspace.

**Parent Topic:**[Exploring CMDB Workspace](exploring-cmdb-workspace.md)


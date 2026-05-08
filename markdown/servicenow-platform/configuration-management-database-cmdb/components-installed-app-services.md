---
title: Components installed with application services
description: Several types of components are installed with activation of the Application Service \[com.snc.cmdb.it\_service\] plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Service instances \(Application services\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with application services

Several types of components are installed with activation of the Application Service \[com.snc.cmdb.it\_service\] plugin, including tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

\[app\_service\_user\]

</td><td>

Views maps for operational service instances and retrieves service content using the getContent - GET REST API. The itil role that serves as the basic helpdesk technician role contains the app\_service\_user role.

</td><td>

None

</td></tr><tr><td>

\[app\_service\_admin\]

</td><td>

Creates and modifies service instances, creates service groups, views, and edits service instance maps.

</td><td>

itil

</td></tr></tbody>
</table>## Tables installed

<table id="table_xqr_k1n_kx"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

BaseLines\[sa\_baselines\]

</td><td>

Storing points in the time defined as baselines for application services.

</td></tr><tr><td>

Business Service User preferences\[sa\_business\_service\_user\_prefs\]

</td><td>

User preferences associated with a specific application service.

</td></tr><tr><td>

Menu Action\[sa\_context\_menu\]

</td><td>

Data on configurable menu options for CIs in the application service map.

</td></tr><tr><td>

Hash\[sa\_hash\]

</td><td>

Internal table which contains counters and hashes on various types of updates related to application services.

</td></tr><tr><td>

Entry Point\[sa\_m2m\_service\_entry\_point\]

</td><td>

Maps entry points to application services.

</td></tr><tr><td>

Discovered Service Notification\[sa\_notification\]

</td><td>

Internal table which contains data on notifications between different parts of the software. Mostly used after activating Service Mapping.

</td></tr><tr><td>

Service Group Members\[sa\_service\_group\_member\]

</td><td>

Maps service groups to application service members.

</td></tr><tr><td>

Business Service Group Responsibilities\[sa\_service\_group\_responsibilities\]

</td><td>

Data on users having access to application service groups.

</td></tr><tr><td>

Checkpoint Attribute Description\[checkpoint\_attribute\_description\]

</td><td>

Links between history timeline changes and service model internal entities \(checkpoints\). Used in lists of history of changes in application service maps.

</td></tr><tr><td>

Service Instance\[cmdb\_ci\_service\_auto\]

</td><td>

Services that can be monitored by the system, which in the base system, includes only application services. If Service Mapping is activated, there can also be records for dynamic CI groups. If Event Management is activated, there can be records for alert groups.

</td></tr><tr><td>

Mapped Application Service\[cmdb\_ci\_service\_discovered\]

</td><td>

Application service CIs. For each application service, there is a container CI record that models the application service.

</td></tr><tr><td>

Bulk Convert Services \[cmdb\_convert\_bulk\_services\]

</td><td>

All bulk conversions of business services to application services \(current and past\), along with the conversion progress which is refreshed every 10 seconds.

</td></tr><tr><td>

Application Services Action Results\[csdm\_dashboard\_action\_report\_result\]

</td><td>

Results for the 'Application Services Missing Data' report in the Application Services dashboard.

</td></tr><tr><td>

Application Services Types Results\[csdm\_dashboard\_type\_report\_result\]

</td><td>

Results for the 'Application Services by Type' report in the Application Services dashboard.

</td></tr><tr><td>

Application Services Dashboard Results\[csdm\_dashboard\_reports\_result\]

</td><td>

Results for the '&lt;Application Servers \| Databases \| Hardware Servers&gt; Not in an Application Service' reports in the Application Services dashboard.

</td></tr><tr><td id="manual-ci-inclusion-exclusion-list">

Manual CI Inclusions / Exclusions \[svc\_manual\_ci\_exclusions\_inclusions.list\]

</td><td>

Contains CI classes included or excluded from application services during population of manual or dynamic application services. Service population happens when-   Manually adding CIs to an application service
-   Converting a business service to an application service
-   Creating or updating an application service using APIs
-   Manually updating an application service with changes from the CMDB

**Note:** The Manual CI Exclusions/Inclusions \[svc\_manual\_ci\_exclusions\_inclusions\] table doesn't include CIs added using traversal rules.

 In the base system, the following CI classes are excluded:

-   NAT \[cmdb\_ci\_translation\_rule\]
-   Endpoint \[cmdb\_ci\_endpoint\]
-   Qualifier \[cmdb\_ci\_qualifier\]
-   Application cluster \[cmdb\_ci\_application\_cluster\]

 CIs of any CI class that is not configured for exclusion in this table can be added to application services.

**Note:** In the CMDB hierarchy, a class derives the included/excluded setting from its closest ancestor. If a class has its own explicit setting, it overrides the derived setting.

 This table supports the functionality that was earlier supported using the following deprecated property: sa.mapping.user.manual.citype.blacklist.

</td></tr></tbody>
</table>## Properties installed

To access application services properties, navigate to **All** &gt; **Configuration** &gt; **Application Services** &gt; **Properties**. The role required for modifying property values, is app\_service\_admin.

If Service Mapping is deployed, see Properties installed with Service Mapping for additional application service properties.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_hw3_25b_qdb"><thead><tr><th>

Property

</th><th>

Usage

</th></tr></thead><tbody><tr><td>

The sys\_id of the default relation type to be added between source and target when adding CI manually to application service

 sa.it\_service.manual\_ci\_rel\_type

</td><td>

-   Type: string
-   Default value: 5599a965c0a8010e00da3b58b113d70e \(Depends on::Used by\)
-   Learn more: [Manually add CIs to an application service](../../service-mapping/task/manually-add-ci-to-business-service.md)

</td></tr><tr><td>

Coefficient of aggregation interval. 0 value means no aggregation is performed on history timeline. The purpose of this property is to decrease number of changes in history timeline by increasing the interval allowed between changes

 sa.history.aggr\_interval\_coef

</td><td>

-   Type: integer
-   Default value: 1

</td></tr><tr><td>

Sync Service Mapping operations with Service Modeling

 sa.service\_modeling.use

</td><td>

-   Type: true\|false
-   Default value: true

</td></tr><tr><td>

Enable limitation of application service maps drawing by number of nodes and edges.

 sa.map.LIMIT\_MAX\_GRAPH\_SIZE

</td><td>

Limit the number of nodes and edges on application service maps.

 -   Type: true\|false
-   Default value: true

 Setting this property to false may reduce performance in maps of large services.

</td></tr><tr><td>

Maximal number of displayable nodes on application service map. Maps with larger values will not be displayed.

 sa.map.MAX\_NODES\_FOR\_LAYOUT

</td><td>

The max number of nodes displayed on an application service map. If the number of nodes exceeds the specified number, the map does not appear and an error message appears.

 -   Type: integer
-   Default value: 5000

</td></tr><tr><td>

Global flag to allow or disable spanning tree view for maps. true \(default\) - allows but not forces spanning tree view on maps.

 sa.map.ALLOW\_SPANNING\_TREE\_VIEW

</td><td>

Enable spanning tree view for application service maps.

 -   Type: true\|false
-   Default value: true

</td></tr><tr><td>

Maximal number of displayable edges on application service map before spanning tree view applied.

 sa.map.MAX\_EDGES\_FOR\_FULL\_LAYOUT

</td><td>

The max number of edges displayed on an application service map, before applying spanning tree view.

 -   Type: integer
-   Default value: 1000

</td></tr><tr><td>

Maximal number of displayable edges on application service map. Maps with larger values will not be displayed.

 sa.map.MAX\_EDGES\_FOR\_LAYOUT

</td><td>

Max number of edges displayed on an application service map. If the number of edges exceeds the specified number, the map does not appear and an error message appears.

 -   Type: integer
-   Default value: 100000

 Increasing the default value may reduce performance in maps for large services.

</td></tr><tr><td>

Maximal degree of node on application service map for large map mode. Maps with smaller degrees will be displayed in regular mode. Maps with larger degrees will apply more edges merging for more compact view.

 sa.map.LIMIT\_GRAPH\_DEGREE

</td><td>

-   Type: integer
-   Default value: 1000

 Increasing the default value may reduce performance in maps for large services.

</td></tr><tr><td>

Limit of amount of services that displayed on Services Tree on maps. Then this limit reached, Services Tree will be blocked.

 sa.service\_tree.MAX\_ITEMS\_TO\_DISPLAY

</td><td>

-   Type: integer
-   Default value: 7000

</td></tr><tr><td>

Maximal amount of connection properties to be shown at once when connection line selected on service map. If selected line contains more connections than defined here, then properties panel will have notification about cut-off connections.

 sa.map.max\_connections\_in\_properties\_panel

</td><td>

-   Type: integer
-   Default value: 50

</td></tr><tr><td>

Enable grouping of CIs on map.

 sa.map.enable\_auto\_grouping

</td><td>

-   Type: true\|false
-   Default value: true

</td></tr><tr><td>

Minimal number of CIs on a map to apply CI grouping. Relevant only if CI grouping is enabled on the map. The following CIs are not counted: discovered clusters, internal CIs inside inclusion boxes, entry points, error nodes, host CIs or CIs that are not hosted on other CIs.

 sa.map.min\_nodes\_for\_auto\_grouping

</td><td>

-   Type: integer
-   Default value: 10

</td></tr><tr><td>

Render full labels on CIs on map. Applicable to all CI labels \(CI name, host name, cluster label, etc.\) Enabling this will disable labels truncation, and labels will most probably overlap with other map elements. Not applicable to network/storage path maps.

 sncCommonMap.RENDER\_FULL\_LABELS

</td><td>

The default value of disabled, means none.-   Type: choice list
-   Default value: Disabled
-   Other possible values:
    -   Exported PDF only: pdf
    -   Map and PDF views: all

</td></tr><tr><td>

Maximal width of CI node labels in pixels. Relevant for any kind of labels \(CI name, host name, cluster label etc.\) This size also modifies horizontal space between CI elements. Applied to map view and exported PDF view. Not applicable to network/storage path maps.

 sncCommonMap.NODE\_LABEL\_WIDTH

</td><td>

-   Type: integer
-   Default value: 95
-   **Other possible values**:
    -   Min value: 20
    -   Max value: 1000

</td></tr><tr><td>

glide.cmdb.csdm.app\_service.max\_results

</td><td>

Max number of items that are calculated in the '&lt;Application Servers \| Databases \| Hardware Servers&gt; Not in an Application Service' report in the Application Services dashboard. -   Type: integer
-   Default value: 100000
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

sa.service.max\_ci\_service\_population

</td><td>

The maximum number of CI connections added to application services during the following operations: Converting manual services created in Event Management into application services and updating application services with changes from the CMDB.-   Type: integer
-   Default value: 1,000
-   Location: Add to System Properties \[sys\_properties\] table.

 Increasing the default value may cause performance issues.

</td></tr><tr><td>

sa.service.population.stop\_expansion\_under\_ci\_classes

</td><td>

List of application service CI classes. If an application service belongs to a CI class that extends one of the CI classes in the list, the system does not insert CIs under this application service CI during [Manually updating an application service with changes from the CMDB](../../service-mapping/task/update-services-from-cmdb.md).-   Type: string
-   Default value: cmdb\_ci\_service\_discovered
-   Location: System Property \[sys\_properties\] table.

</td></tr></tbody>
</table>
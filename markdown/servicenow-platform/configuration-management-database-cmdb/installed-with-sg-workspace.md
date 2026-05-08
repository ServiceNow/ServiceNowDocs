---
title: Components installed with Service Graph Workspace
description: Several types of components are installed with the activation of the CMDB Workspace \(sn\_cmdb\_ws\) plugin, which includes Service Graph Workspace. This includes properties, tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [Reference, Service Graph Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with Service Graph Workspace

Several types of components are installed with the activation of the CMDB Workspace \(sn\_cmdb\_ws\) plugin, which includes Service Graph Workspace. This includes properties, tables, user roles, and scheduled jobs.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see Find components installed with an application.

In addition, the CMDB Workspace plugin adds the CMDB Group type 'CMDB Workspace'. For components associated with the CMDB Data Manager, see [Components related to CMDB Data Manager](components-cmdb-data-manager.md).

## Properties installed

The following properties are installed by the Configuration Management \(CMDB\) \(com.snc.cmdb\) plugin which is included in base systems.

<table id="table_iv2_bwx_dxb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cmdb\_ws.ci\_overview.managed\_by\_me.enabled​

</td><td>

Shows/hides the My CIs section of CI Overview on the CMDB Workspace landing page, for users with sn\_cmdb\_editor role.

 -   Type: true \| false
-   Default: true
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

sn\_cmdb\_ws.total\_cis.enabled​

</td><td>

Shows/hides the Total CIs section on the CMDB Workspace landing page.

 -   Type: true \| false
-   Default: true
-   Location: Add to System Properties \[sys\_properties\] table.

</td></tr><tr><td>

sn\_cmdb\_ws.ms.discovery\_source\_not\_reporting\_max\_days

</td><td>

Number of days after which if one or more discovery sources stop reporting CIs, that CI is included in the CIs not reported by discovery sources chart in the CMDB 360 view.

 -   Type: integer
-   Default: 7
-   Location: Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **CMDB 360**. Select Settings and configure **Number of days since CIs were last discovered by a discovery source** in the Potential issues section.
-   Learn more: [Configure the CMDB 360 dashboard in CMDB Workspace or in Service Graph Workspace](../task/workspc-mltsrc-configure.md).

</td></tr><tr><td>

sn\_cmdb\_ws.ms.report\_max\_limit

</td><td>

Maximum number of records that appear as list views when drilling down from the following charts:

-   CIs not reported by discovery sources
-   Data mismatch
-   CIs by number of discovery sources
-   CIs with a single source

 Details:

-   Type: integer
-   Default: 100,000
-   Location: Navigate to **Workspaces** &gt; **CMDB Workspace** and then select **CMDB 360**. Select Settings and configure **Maximum number of records to process** in the Global section.
-   Learn more: [Configure the CMDB 360 dashboard in CMDB Workspace or in Service Graph Workspace](../task/workspc-mltsrc-configure.md).

</td></tr><tr><td>

sn\_cmdb\_ws.unifiedmap.map\_search\_filter.default\_levels

</td><td>

Initial default number of levels from the home node, up and down the CMDB hierarchy, to show on a map. ​Up the hierarchy goes from all parents to their parents up to the specified level. Down the hierarchy goes from all children to their children up to the specified level.

 -   Type: integer
-   Default: 3
-   Location: Add to System Properties \[sys\_properties\] table.

 Editing affects all users and requires the sn\_cmdb\_admin user role.

</td></tr><tr><td>

sn\_cmdb\_ws.unifiedmap.map\_search\_filter.max\_levels​

</td><td>

Maximum number of levels from the home node, up and down the CMDB hierarchy, to show on a map. ​Up the hierarchy goes from all parents to their parents up to the specified level. Down the hierarchy goes from all children to their children up to the specified level.

-   Type: integer
-   Default: 25
-   Location: System Properties \[sys\_properties\] table

 Editing affects all users and requires the sn\_cmdb\_admin user role.

</td></tr><tr><td>

sn\_cmdb\_ws.list.record\_count\_limit

</td><td>

The maximum number of results that the system counts for when using conditional search to search for CIs on the Home view in CMDB Workspace. This count shows for example, at the top of the search results list.

 -   Type: integer
-   Default: 100,000
-   Location: Add to System Properties \[sys\_properties\] table.
-   More information: [CMDB Workspace store app](../concept/cmdb-workspace.md)

 For example, if a limit of 100,000 is reached, the count shows "100,000 +" to indicate that counting stopped at 100,000 and that there are additional uncounted results.

 Increasing the value of this property directly results in greater impact on performance. However, if a precise count is needed, set this limit to a number that isn't reached by the anticipated count.

</td></tr><tr><td>

sn\_cmdb\_ws.explore\_ci.record.enabled

</td><td>

Enables the use of the CI Form feature when selecting CIs to view in CMDB Workspace or in another workspace.

 When false, the system shows CI records in a basic list view instead of CI Form. You might need to temporarily disable the CI Form experience if its not yet ready to be used. For example, you might need to migrate previous custom configurations to CI Form to prepare it for use.

 -   Type: true \| false
-   Default: true
-   Location: Add to System Properties \[sys\_properties\] table.
-   More information: [Manage CI details using CI Form in CMDB Workspace](../concept/ci-form-cmdb-workspace.md)

</td></tr></tbody>
</table>## Roles installed

The following roles are installed by the Configuration Management \(CMDB\) \(com.snc.cmdb\) plugin which is included in base systems. These roles are required for access and interaction with the CMDB Workspace, and are included for completeness.

**Note:** On an instance that has been upgraded directly from Xanadu or Yokohama to the Australia release: To correctly configure some of the user roles as described below, such as CMDB Admin and CMDB Editor, you must run the '**Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles**' scheduled job. For more information about this scheduled job and its use, see [Zurich release notes](https://www.servicenow.com/docs/bundle/zurich-release-notes/page/release-notes/now-platform-capabilities/cmdb-rn.html).

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Role containment

</th></tr></thead><tbody><tr><td>

CMDB Admin\[sn\_cmdb\_admin\]

</td><td>

Provides the highest level of access to tools and UIs within CMDB Workspace, including full access to the Configuration Item \[cmdb\_ci\] table. A CMDB Admin, for example, can set policies in the CI Class Manager and service instance \(application service\) requirements.

 CMDB Admin can also modify default config records under the default identifier or the default identifier itself.

</td><td>

Contains:

-   data\_manager\_admin
-   canvas\_admin
-   sn\_cmdb\_editor
-   cmdb\_ms\_admin
-   cmdb\_dedup\_admin

</td></tr><tr><td>

CMDB Editor\[sn\_cmdb\_editor\]

</td><td>

Provides access to tools and UIs within CMDB Workspace including full access to the Configuration Item \[cmdb\_ci\] table.

 A CMDB Editor has writing privileges to CMDB Data Manager tasks and to CIs but can't change policies such as in the CMDB Data Manager or in the CI Class Manager.

</td><td>

Contains:

-   sn\_cmdb\_user
-   cmdb\_ms\_editor

</td></tr><tr><td>

CMDB User\[sn\_cmdb\_user\]

</td><td>

Provides read-only access to the CMDB data and to basic UIs such as CMDB reports and dashboards, within CMDB Workspace.

</td><td>

Contained by: itil \(indirectly\)

 Contains roles:

-   canvas\_user
-   data\_manager\_user
-   cmdb\_ms\_user

</td></tr><tr><td>

Multisource CMDB Admin\[cmdb\_ms\_admin\]

</td><td>

Provides full access to data, dashboard configurations, and queries related to Multisource CMDB and CMDB 360.

</td><td>

Contains: cmdb\_ms\_editor

</td></tr><tr><td>

Multisource CMDB Editor\[cmdb\_ms\_editor\]

</td><td>

Provides access to CMDB 360 records and enables users to create and edit CMDB 360 queries.

</td><td>

Contains: cmdb\_ms\_user

</td></tr><tr><td>

Multisource CMDB User\[cmdb\_ms\_user\]

</td><td>

Provides read-only access to multisource data, CMDB 360 queries, and to related UIs such as CMDB 360 reports and dashboards.

</td><td>

Contains: cmdb\_read

</td></tr><tr><td>

Workspace Config Admin\[sn\_cmdb\_ws.config\_admin\]

</td><td>

Provides an administrator full access to the Config identifiers \[sn\_cmdb\_ws\_config\_identifier\] table and its descendent config tables.

 Can modify non-default config or config identifier records. Since config tables contain properties which belong to different applications, Workspace Config Admins should only modify records related to their application.

</td><td>

Contains: sn\_cmdb\_ws.config\_editor

</td></tr><tr><td>

Workspace Config Editor\[sn\_cmdb\_ws.config\_editor\]

</td><td>

Provides editing access to child config tables such as the Workspace Config Properties \[sn\_cmdb\_ws\_config\_property\] table.

 Can modify non-default config records. Since config tables contain properties which belong to different applications, Workspace Config Editors should only modify records related to their application.

</td><td>

 

</td></tr><tr><td>

\[cmdb\_manual\_ci\_ire\_access\]

</td><td>

Provides access to the experience of manual CI creation in CMDB Workspace and in other workspaces.

</td><td>

 

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB Workspace Collection

</td><td>

Updates the information in all the 7-Day Activity charts such as the CI Activity in Last 7 Days chart.

</td></tr><tr><td>

Multisource Dashboard Analytics Population

</td><td>

Runs daily to calculate the aggregate statistics of CMDB 360 data and populates the CMDB 360 dashboard landing page.

</td></tr><tr><td>

Multisource Dashboard Collection

</td><td>

Collects CMDB 360 data and then invokes the **Multisource Dashboard Analytics Population** scheduled job.

</td></tr><tr><td>

Multisource Dashboard Data Generator \( Demo data\)

</td><td>

Demo job that populates CMDB 360 tables with simulated data, to showcase the CMDB 360 dashboard landing page. Runs on demand.

</td></tr><tr><td>

insight – cloud non-cloud aggregate

</td><td>

Runs every 30 minutes to collect data for the Cloud and non-cloud resources chart.

</td></tr><tr><td>

Insight - Cloud Applications

</td><td>

Collects cloud data for the cmdb\_ci\_appl table.

</td></tr><tr><td>

Insight - Non-cloud Applications

</td><td>

Collects non-cloud data for the cmdb\_ci\_appl table.

</td></tr><tr><td>

Insight - Cloud Object Storage

</td><td>

Collects cloud data for the cmdb\_ci\_cloud\_object\_storage table.

</td></tr><tr><td>

Insight - Cloud Service Account

</td><td>

Collects cloud data for the cmdb\_ci\_cloud\_service\_account table.

</td></tr><tr><td>

Insight - Cloud DB Instances

</td><td>

Collects cloud data for the cmdb\_ci\_db\_instance table.

</td></tr><tr><td>

Insight - Non-cloud DB Instances

</td><td>

Collects non-cloud data for the cmdb\_ci\_db\_instance table.

</td></tr><tr><td>

Insight - Cloud Kubernetes Cluster

</td><td>

Collects cloud data for the cmdb\_ci\_kubernetes\_cluster table.

</td></tr><tr><td>

Insight - Non-cloud Kubernetes Cluster

</td><td>

Collects non-cloud data for the cmdb\_ci\_kubernetes\_cluster table.

</td></tr><tr><td>

Insight - Cloud Servers​

</td><td>

Collects cloud data for the cmdb\_ci\_server​ table.

</td></tr><tr><td>

Insight - Non-cloud Servers​

</td><td>

Collects non-cloud data for the cmdb\_ci\_server​ table.

</td></tr><tr><td>

Insight - Cloud Storage Volume​

</td><td>

Collects cloud data for the cmdb\_ci\_storage\_volume​ table.

</td></tr><tr><td>

Insight - Non-cloud Storage Volume​

</td><td>

Collects non-cloud data for the cmdb\_ci\_storage\_volume table.​

</td></tr><tr><td>

Insight - Cloud VM Instances

</td><td>

Collects cloud data for the cmdb\_ci\_vm\_instance table.

</td></tr><tr><td>

Insight - Non-cloud VM Instances

</td><td>

Collects non-cloud data for the cmdb\_ci\_vm\_instance table.

</td></tr><tr><td>

CMDB Workspace – Populate aggregates Daily

</td><td>

Runs daily to collect the latest data from the instance for cards such as the CI Summary chart in the CMDB Workspace landing page, and the following cards in the Insights view:

-   CIs processed by IRE​
-   CIs used in Data Manager policies​
-   CIs used in data attestation​
-   Query Builder queries
-   Intelligent search

 Populates the Base Aggregate Data \[sn\_cmdb\_ws\_base\_aggregate\_data\] table with the collected data.

 Once collection completes, invokes the **CMDB Workspace Aggregates Daily Collection** scheduled job.

</td></tr><tr><td>

CMDB Workspace – Populate aggregates Monthly

</td><td>

Runs monthly to collect data from the instance for cards such as the following, in the Insights view:

-   CIs processed by IRE based on source
-   CIs processed by IRE​

 Once collection completes, invokes the **CMDB Workspace Aggregates Monthly Collection** scheduled job.

</td></tr><tr><td>

CMDB Workspace Aggregates Daily Collection

</td><td>

A Performance Analytics job that stores the latest data generated by the **CMDB Workspace – Populate aggregates Daily** scheduled job. The stored data is then shown in respective cards in the Insights view.

</td></tr><tr><td>

CMDB Workspace Aggregates Monthly Collection

</td><td>

A Performance Analytics job that stores the latest data generated by the **CMDB Workspace – Populate aggregates Monthly** scheduled job. The stored data is then shown in respective cards in the Insights view.

</td></tr><tr><td>

\[Demo\] — CMDB Workspace Collection

</td><td>

Supports demo data for CMDB Workspace charts in various views such as the Home view.

 Installed only if **Load demo data** was checked when the CMDB Workspace store app was installed or upgraded.

</td></tr><tr><td>

\[Demo\] — CMDB Workspace demo data

</td><td>

Activates demo data for CMDB Workspace charts in views such as the Insights view, and CMDB 360 view \(if CMDB 360 is enabled\). Populates the Base Aggregate Data \[sn\_cmdb\_ws\_base\_aggregate\_data\] table with random numbers that illustrate trend lines in charts in the Home and Insights views. It then runs demo data collection scheduled jobs.

 Installed only if **Load demo data** was checked when the CMDB Workspace store app was installed or upgraded.

</td></tr><tr><td>

\[Demo\] CMDB Workspace Aggregates Daily Collection

</td><td>

A Performance Analytics job that supports demo data for CMDB Workspace charts in various views such as the Insights view and which is installed only if **Load demo data** was checked when the CMDB Workspace store app was installed or upgraded.

 Stores the demo data generated by the **CMDB Workspace – Populate aggregates Daily** scheduled job. The demo data is then shown in respective cards in the Insights view.

</td></tr><tr><td>

\[Demo\] CMDB Workspace Aggregates Monthly Collection

</td><td>

A Performance Analytics job that supports demo data for CMDB Workspace charts in various views such as the Insights view and which is installed only if **Load demo data** was checked when the CMDB Workspace store app was installed or upgraded.

 Stores the demo data generated by the **CMDB Workspace – Populate aggregates Monthly** scheduled job. The demo data is then shown in respective cards in the Insights view.

</td></tr><tr><td>

CMDB Workspace Collection On Demand With Lookback

</td><td>

Collects historical data \(past 30 days\) for some indicators such as the Integration outliers.

 Runs automatically during install or upgrade and isn't configured with any recurring schedule.

</td></tr><tr><td>

PopulateDuplicate Task Group Daily

</td><td>

Runs daily to populate the following tables:

-   Group Task Mapping \[ sn\_cmdb\_ws\_reconcile\_duplicate\_task\_group\_m2m\]
-   Remediate Duplicate Task Groups \[ sn\_cmdb\_ws\_reconcile\_duplicate\_task\_group\]

Reads de-duplication task data records and calculates the root cause analysis for the duplication.

 Used in support of Now Assist for CMDB.

</td></tr></tbody>
</table>## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB Group Metadata

 \[sn\_cmdb\_ws\_group\_metadata\]

</td><td>

CMDB group data with count of CIs in each group.

</td></tr><tr><td>

CMDB Group Query Metadata

 \[sn\_cmdb\_ws\_group\_query\_metadata\]

</td><td>

Encoded queries with count of CIs in each encoded query subgroup.

</td></tr><tr><td>

NLQ Sample Search

 \[sn\_cmdb\_ws\_nlq\_sample\_search\]

</td><td>

Sample searches that appear when selecting the search box of an Intelligent Search for CMDB widget.

</td></tr><tr><td>

NLQ Sample Search Table

 \[sn\_cmdb\_ws\_nlq\_sample\_search\_table\]

</td><td>

References the actual tables associated with sample searches that appear when selecting the search box of an Intelligent Search for CMDB widget.

</td></tr><tr><td>

NLQ Excluded Table

 \[sn\_cmdb\_ws\_nlq\_excluded\_table\]

</td><td>

Tables with ambiguous names that should be excluded from Intelligent Search. These tables won’t appear in suggestions, and other tables with similar names are given higher priority in search results.

</td></tr><tr><td>

Important Actions Configuration

 \[sn\_cmdb\_ws\_imp\_action\_card\_config\]

</td><td>

Configuration of appearance and behavior of Important action cards that appear on the landing page of the CMDB Workspace. Editing in this table is accessible only to users with the sn\_cmdb\_admin role. Authorized users can modify attributes of an important action such as Active and Filter conditions, but can't modify the Type, Persona, and Table attributes.

</td></tr><tr><td>

Quick Links

 \[sn\_cmdb\_ws\_quick\_links\]

</td><td>

Quick links that appear on the CMDB Workspace landing page.

</td></tr><tr><td>

CIs by Number of Sources

 \[sn\_cmdb\_ws\_ms\_cis\_by\_number\_of\_sources\]

</td><td>

CIs grouped by the number of discovery sources they were discovered by. Records appear as a list view when clicking on the CIs by number of discovery sources bar chart in the CMDB 360 view.

</td></tr><tr><td>

CIs With a Single Source

 \[sn\_cmdb\_ws\_ms\_cis\_with\_single\_source\]

</td><td>

CIs reported by only one discovery source. Records appear as a list view when selecting the CIs with a single discovery source chart in the CMDB 360 view.

</td></tr><tr><td>

CMDB Workspace Multisource Class Metadata

 \[sn\_cmdb\_ws\_ms\_class\_metadata\]

</td><td>

Class configuration settings such as class selections and weights, that CMDB Admins can modify from the CMDB 360 view. Used by CMDB 360 analytics population queries to store a sample set of coverage data for the CIs by number of sources and CIs with a single source drill-downs cards.

</td></tr><tr><td>

Multisource Data Mismatch Records

 \[sn\_cmdb\_ws\_ms\_data\_mismatch\]

</td><td>

Data mismatch records found from attribute discrepancies from various data sources. Records appear as a list view when selecting the Data mismatch chart in the CMDB 360 view.

</td></tr><tr><td>

CMDB Workspace Multisource Data Mismatch Configurations

 \[sn\_cmdb\_ws\_ms\_data\_mismatch\_config\]

</td><td>

Data mismatch settings, such as the selection of classes, attributes, conditions, and weights, that CMDB Admins can modify in the CMDB 360 view. Used by CMDB 360 analytics population queries to store a sample set of data mismatch records in the sn\_cmdb\_ws\_ms\_data\_mismatch table.

</td></tr><tr><td>

Discovery sources not reporting CIs

 \[sn\_cmdb\_ws\_ms\_discovery\_sources\_not\_reporting\]

</td><td>

Data for when one or more discovery sources stop reporting CIs after the specific X number of days \(X can be set in the CMDB 360 view and is stored in the sn\_cmdb\_ws.ms.discovery\_source\_not\_reporting\_max\_days system property\). Records appear as a list view when selecting the CIs not reported by discovery sources chart in the CMDB 360 view.

</td></tr><tr><td>

Multisource Workspace Settings Weight Type

 \[sn\_cmdb\_ws\_ms\_settings\_weight\_type\]

</td><td>

Weight type \(automatic or manual\) for data mismatch and coverage settings in CMDB 360 view.

</td></tr><tr><td>

Datacenter Types

 \[sn\_cmdb\_ws\_datacenter\_type\]

</td><td>

Classifications of datacenter classes which are considered cloud or non-cloud in the organization, which is used for the Cloud and non-cloud resources chart.

</td></tr><tr><td>

CMDB Insight Query Categories

 \[sn\_cmdb\_ws\_insight\_query\_category\]

</td><td>

Class categories and their status for inclusion in the Cloud and non-cloud resources chart.

</td></tr><tr><td>

CMDB Insight Data

 \[sn\_cmdb\_ws\_insight\_data\]

</td><td>

Legacy table for storing data for the Cloud and non-cloud resources chart.

 Starting with CMDB Workspace version 3.4, the CMDB Product Insight Data \[sn\_cmdb\_ws\_product\_insight\_data\] table is used instead.

</td></tr><tr><td>

Base Aggregate Data

 \[sn\_cmdb\_ws\_base\_aggregate\_data\]

</td><td>

Aggregation data for CMDB Workspace cards and parent table to other aggregation tables. When processing for a count completes, **State** of the existing record for that count is set to **retired** and a new record for that count is created with the updated count value. Cards in CMDB Workspace views show values only for counts where **State** = **ready**.

 Read only.

</td></tr><tr><td>

Service Graph Connector

 \[sn\_cmdb\_ws\_service\_graph\_connector\]

</td><td>

Details about all Service Graph Connectors that are currently available in the ServiceNow Store \(excluding any Innovation Lab connectors\). Data is used to provide a current count for the Service Graph Connectors card in the Insights view.

 Read only.​

</td></tr><tr><td>

Rating Configuration

 \[sn\_cmdb\_ws\_rating\_config\]

</td><td>

Start and end values for different ratings of a category. For example, start and end values for low, moderate, and high adoption level ratings for the data governance category in the Insights view.

 Read only.​

</td></tr><tr><td>

Feature Category

 \[sn\_cmdb\_ws\_feature\_category\]

</td><td>

Metadata of the feature card for most of the features at CMDB Workspace level.

 Read only.​

</td></tr><tr><td>

CMDB Product Insight Data

 \[sn\_cmdb\_ws\_product\_insight\_data\]

</td><td>

Aggregated count for each class and datacenter class, used for cards in the Insights view.

 Read only.​

</td></tr><tr><td>

Feature Category Runtime Attributes

 \[sn\_cmdb\_ws\_feature\_category\_runtime\_attribute\]

</td><td>

Runtime attributes related to performance insights, that can be used when running various scheduled jobs.

 Read only.​

</td></tr><tr><td>

Integration Aggregate Data

 \[sn\_cmdb\_ws\_integration\_aggregate\_data\]

</td><td>

Integration outlier information related to performance insights. Details for each Integration with execution records which contain processing rate or rows outliers.

 Read only.​

</td></tr><tr><td>

Partial Payload Items

 \[sn\_cmdb\_ws\_partial\_payload\_item\]

</td><td>

Extracted partial payload information related to performance insights. Includes discovery source, error, and class, associated with each partial payload item.

 Read only.​

</td></tr><tr><td>

Application Service Insights Data

 \[sn\_cmdb\_ws\_app\_svc\_insight\_data\]

</td><td>

Service instances \(Application services\) details such as classification \(cloud vs. non-cloud, hybrid, or unknown\) and count of CIs associated with the service instance.

 Read only.​

</td></tr><tr><td>

Table Attributes

 \[sn\_cmdb\_ws\_node\_map\_table\_attributes​\]

</td><td>

Set of extended properties, per class, that appear in the Attributes pane in the contextual side panel for a selected CI in Unified Map.

 This table leverages the use of the configuration identifiers framework.

 For more information, see [Configure which attributes to display in the Attributes panel](../task/unified-map-config-extended-prop.md).

</td></tr><tr><td>

Node Map Related Items

 \[sn\_cmdb\_ws\_node\_map\_related\_item​\]

</td><td>

Categorization and order of related items, per class, that appear in the **Related items** panel, in CI badges, and on the timeline in Unified Map.

 This table leverages the use of the configuration identifiers framework.

 For more information, see [Configure how to display related items on the map](../task/unified-map-config-related-items.md).

</td></tr><tr><td>

Node Map References

 \[sn\_cmdb\_ws\_node\_map\_reference\]

</td><td>

Reference relationships that appear as a dotted line relationship in Unified Map.

 This table leverages the use of the configuration identifiers framework.

 For more information, see [Configure display of connections to a referenced class](../task/unified-map-config-map-references.md).

</td></tr><tr><td>

Class Icons

 \[sn\_cmdb\_ws\_class\_icon​\]

</td><td>

Maps ServiceNow platform UI Builder \(UIB\) icon values \(for example 'serverbox-outline'\) to CMDB class display names that they are used for \(for example 'Network Disk'\) in Unified Map.​

</td></tr><tr><td>

Node Map Profiles

 \[sn\_cmdb\_ws\_node\_map\_profiles​\]

</td><td>

Class profiles that include default filters and some Unified Map settings, per class. A class profile is applied if no filter preset is in effect, to the initial map and when setting the filter preset to `Default view`.

 Specifying a class profile can be especially useful for Service Mapping data with the Mapped Application Service class.

 This table leverages the use of the configuration identifiers framework.

 For more information, see [Create a class profile of visible layers for classes](../task/unified-map-config-class-profile.md).

</td></tr><tr><td>

CMDB Data Management Certification Task To Document

 \[sn\_cmdb\_ws\_dm\_certification\_task\_to\_document\]

</td><td>

Mappings between certification tasks and each of their associated CI records targeted for certification.

</td></tr><tr><td>

CMDB Certification Attribute Status

 \[sn\_cmdb\_ws\_dm\_certification\_attribute\_status\]

</td><td>

Flattened failed attribute status JSON. Used for reporting certification exceptions.

</td></tr><tr><td>

CMDB Data Management Task Execution Context

 \[sn\_cmdb\_ws\_dm\_task\_execution\_context\]

</td><td>

Mappings between tasks and a policy’s' execution context.

</td></tr><tr><td>

Remediate Duplicate Task Groups

 \[sn\_cmdb\_ws\_reconcile\_duplicate\_task\_group\]

</td><td>

Groupings of de-duplication tasks, the CI class affected, any discovery source associated with the de-duplication task, and the CI identification rule that was used to discover the CIs.

 Used in support of Now Assist for CMDB.

 -   sn\_cmdb\_admin role has create/write/delete privileges
-   sn\_cmdb\_user OR dedup\_admin roles have read privileges

</td></tr><tr><td>

Group Task Mapping

 \[sn\_cmdb\_ws\_reconcile\_duplicate\_task\_group\_m2m\]

</td><td>

Reference to the Remediate Duplicate Task Groups table and a root cause analysis summary of the reason that the Cis were added to the de-duplication task

 Used in support of Now Assist for CMDB.

 -   sn\_cmdb\_admin role has create/write/delete privileges
-   sn\_cmdb\_user OR dedup\_admin roles have read privileges

</td></tr><tr><td>

Config identifiers

 \[sn\_cmdb\_ws\_config\_identifier\]

</td><td>

Parent table of the configuration identifiers framework. By default, contains the 'Default' config identifier with default settings for various CMDB Workspace features.

 Stores any additional config identifiers, configured with custom settings for a CMDB Workspace feature, that is applicable to a specific workspace.

 For information about the configuration identifiers framework, see [Configuration identifiers framework](../concept/configuration-identifiers-framework.md).

</td></tr><tr><td>

Workspace Config Properties

 \[sn\_cmdb\_ws\_config\_property\]

</td><td>

Collection of properties that control different behaviors in Unified Map.

 This table leverages the use of the configuration identifiers framework.

</td></tr><tr><td>

CI additional attributes config

 \[sn\_cmdb\_ws\_ci\_additional\_attributes\]

</td><td>

Settings of requests for specific CI attributes when using the CMDB Workspace feature of manually creating a new CI.

 This table leverages the use of the configuration identifiers framework.

 For more information, see [Request additional attributes for new CIs](../task/additional-att-create-ci-workspace.md#).

</td></tr><tr><td>

CI class configs

 \[sn\_cmdb\_ws\_ci\_class\_config\]

</td><td>

Settings that limit the selection of classes for a new CI when using the CMDB Workspace feature of creating manually a new CI.

 This table leverages the use of the configuration identifiers framework.

 For more information, see [Limit the class list for new CIs created in a workspace](../task/limit-class-create-ci-workspace.md).

</td></tr></tbody>
</table>
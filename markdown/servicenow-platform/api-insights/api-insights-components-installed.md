---
title: Components installed with API Insights
description: Several types of components are installed with activation of the API Insights plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: xanadu
product: API Insights
classification: api-insights
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, API Insights, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components installed with API Insights

Several types of components are installed with activation of the API Insights plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_gt1_hhq_ybc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Enterprise architect administrator

 \[sn\_api\_insights\_ws.api\_mgmt\_architect\_admin\]

</td><td>

Accesses the API Insights workspace to search APIs, review data model recommendations, monitors API connections, evaluate metrics on API usage, and set parameters for data model recommendations and de-duplication tasks.

</td><td>

sn\_api\_insights\_ws.api\_mgmt\_architect

</td></tr><tr><td>

Enterprise architect

 \[sn\_api\_insights\_ws.api\_mgmt\_architect\]

</td><td>

Accesses the API Insights workspace to search APIs, monitor team APIs, view managed and subscribed APIs, track API activity, review API access requests, and manage API life cycle aspects, including APIs without business context, ownership, product models, or designs.

</td><td>

-   task\_editor
-   sn\_incident\_read
-   sn\_vul.vulnerability\_read
-   sn\_cmdb\_editor
-   sn\_msi.msi\_incident\_read

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_f5b_q5v_f2c"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Gather APIs without Business App relationship

</td><td>

Identifies and collects APIs that do not have an associated business context also called as business application.

</td></tr><tr><td>

Import ServiceNow API to API Insights

</td><td>

Retrieves ServiceNow APIs from the ServiceNow registry and imports them into API Insights.

</td></tr><tr><td>

Import ServiceNow API usage to MetricBase

</td><td>

Collects ServiceNow API usage data and pushes it to the MetricBase application.

</td></tr><tr><td>

SyncOwnershipGroupsOfAPIVersions

</td><td>

Synchronizes ownership groups for API versions in API Insights.

</td></tr><tr><td>

API Specification Validation

</td><td>

Performs automated validation of API specifications in an instance.

</td></tr><tr><td>

Tag based relationship mapping

</td><td>

Applies tag-based mapping rules between APIs and application services or business applications.

</td></tr></tbody>
</table>## Tables installed

<table id="table_kt1_hhq_ybc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

APIs missing relationships

 \[sn\_api\_insights\_ws\_apis\_missing\_relationships\]

</td><td>

API records that lack a defined relationship.

</td></tr><tr><td>

API Specification

 \[sn\_api\_insights\_ws\_api\_specification\]

</td><td>

API specification details, such as OpenAPI definitions.

</td></tr><tr><td>

Importable ServiceNow APIs

 \[sn\_api\_insights\_ws\_importable\_servicenow\_api\]

</td><td>

Details of APIs imported from ServiceNow.

</td></tr><tr><td>

Open API Specifications

 \[sn\_api\_insights\_ws\_openapi\_specifications\]

</td><td>

OpenAPI specification records for API Insights.

</td></tr><tr><td>

Push API Specification

 \[sn\_api\_insights\_ws\_push\_api\_spec\]

</td><td>

Records for pushing API specifications.

</td></tr><tr><td>

API Requests Access Task

 \[sn\_api\_insights\_ws\_request\_access\_task\]

</td><td>

Tasks related to API access requests.

</td></tr><tr><td>

Specification Validation Rule

 \[sn\_api\_insights\_ws\_spec\_validation\_rule\]

</td><td>

Validation rules that validate API specifications based on the configured rules.

</td></tr><tr><td>

API Metric Configuration

 \[sn\_api\_insights\_ws\_api\_metric\_config\]

</td><td>

Configuration that maps each discovery source to the MetricBase application used for analytics, defining the metric name, whether it applies at API or component level, and the metric type \(usage, error rate, latency, cache hit\).

</td></tr><tr><td>

Tag Based Relationship Mapping\[sn\_api\_insights\_ws\_tag\_relationship\_mapping\]

</td><td>

Relationship rules that apply tag-based mapping between APIs and application services or business applications, defining the CI types involved, the relationship type, and which CI acts as the parent.

</td></tr></tbody>
</table>## Plugins installed

<table id="table_dyd_hpw_vnb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MetricBase \(com.snc.clotho\)

</td><td>

Collects, retains, analyzes, graphs, and acts on time-series data.

</td></tr></tbody>
</table>## ServiceNow Store applications installed

<table id="table_e2s_lsj_wnb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

@devsnc/sn-list-selector \(sn\_list-selector\)

</td><td>

Enables selecting a set of values from a simple or multi-dimensional data source.

</td></tr><tr><td>

CMDB CI Class Models \(sn\_cmdb\_ci\_class\)

</td><td>

Provides the single source for all new base-system CMDB CI class models defined by ServiceNow.

</td></tr><tr><td>

CMDB Workspace \(sn\_cmdb\_ws\)

</td><td>

Enables a workspace for working with the CMDB to search and explore the CMDB, understand its health, work on related tasks, view activity, performance and feature usage, and access various management tools to support tasks in an organization.

</td></tr><tr><td>

Node map Experience Component \(sn\_node\_map\)

</td><td>

Enables mapping and visualizing connections between concepts.

</td></tr><tr><td>

SGC Central \(sn\_sgc\_central\)

</td><td>

Enables discovering, installing, and monitoring Service Graph Connectors.

</td></tr><tr><td>

Timeline component \(sn\_ui\_timeline\)

</td><td>

Shows events and information across a timeline to contextualize history or important information for an object.

</td></tr><tr><td>

UX Commons \(sn\_app\_ux\_commons\)

</td><td>

Enhances component experience with common UI Builder utilities, controllers, and bundles.

</td></tr></tbody>
</table>**Parent Topic:**[API Insights reference](../concept/api-insights-reference.md)


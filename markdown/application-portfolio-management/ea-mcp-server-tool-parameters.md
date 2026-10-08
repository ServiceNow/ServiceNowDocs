---
title: MCP for Enterprise Architecture tool parameters
description: Parameters that each MCP for Enterprise Architecture tool accepts, and how to phrase prompts that return the data you need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/ea-mcp-server-tool-parameters.html
release: brazil
topic_type: reference
last_updated: "2026-09-23"
reading_time_minutes: 6
keywords: [MCP tool parameters, EA MCP server]
breadcrumb: [Reference, MCP for Enterprise Architecture, Enterprise Architecture]
---

# MCP for Enterprise Architecture tool parameters

Parameters that each MCP for Enterprise Architecture tool accepts, and how to phrase prompts that return the data you need.

The tools installed with the application are annotated as read-only. They retrieve or analyze EA data but don't create, update, or delete records in your instance. For details about tool annotations, see [Components installed with MCP for Enterprise Architecture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/installed-with-mcp-for-ea.md).

Tools that return lists support pagination through the **limit** and **offset** parameters. When more results are available, the response includes `has_more` and `next_offset` values that the AI assistant uses to request the next set of results.

## Get EA Business App Insights

<table id="table_ea_mcp_param_app_insights"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sys\_id**

</td><td>

Sys ID of the business application to generate insights for.Required.

</td></tr><tr><td>

**page\_context**

</td><td>

Prompt variant that shapes the insights. Possible values:-   `business_portfolio`: Capability mapping and business value of the application.
-   `app_rationalization_list`: Consolidation, redundancy, and modernization recommendations.
-   `app_rationalization_bubble_chart`: Technical fitness compared with business value, for investment prioritization.

When omitted, general insights covering lifecycle, technical health, cost, risk, and strategic alignment are generated.

</td></tr><tr><td>

**primary\_capability\_sys\_id**

</td><td>

Sys ID of the business capability to treat as the primary capability. Used only when **page\_context** is `business_portfolio`. When omitted, the first capability connected to the application is used.

</td></tr><tr><td>

**bubble\_chart\_axis**

</td><td>

Sys ID of the bubble chart axis configuration \(`apm_bubble_chart` record\) to use. Used only when **page\_context** is `app_rationalization_bubble_chart`.

</td></tr><tr><td>

**fiscal\_period**

</td><td>

Sys ID of the fiscal period \(`fiscal_period` record\) to scope indicator scores to.

</td></tr></tbody>
</table>## Capability Hierarchy App Resolver

<table id="table_ea_mcp_param_cap_hierarchy"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**mode**

</td><td>

Operation to perform. Possible values:-   `prompt`: Hierarchy statistics for a capability, before applications are queried.
-   `direct`: Applications mapped directly to the capability.
-   `hierarchy`: Applications mapped to the capability and all its descendant capabilities.
-   `all_top_level`: Portfolio-wide coverage across all top-level capability domains.
-   `bc_health`: Overall score, indicator scores, assessment status, health of supporting business applications, and an optional multi-year trend.
-   `resolve_capability`: Sys ID of a capability, matched by name.
-   `get_descendants`: All descendant capabilities of a capability.

Required.

</td></tr><tr><td>

**capability\_name**

</td><td>

Name of the business capability. Required for all modes except `all_top_level`. If no exact match is found, the closest matches are returned.

</td></tr><tr><td>

**target\_table**

</td><td>

Table of the entities to look up. Used in the `direct`, `hierarchy`, and `all_top_level` modes.Default: `cmdb_ci_business_app`

</td></tr><tr><td>

**fiscal\_period\_name**

</td><td>

Fiscal period for the `bc_health` mode, for example, `FY25`. When omitted, the current fiscal year is used.

</td></tr><tr><td>

**include\_trend**

</td><td>

Option to include multi-year trend history in the `bc_health` mode.Default: false

</td></tr><tr><td>

**trend\_period\_count**

</td><td>

Number of historical fiscal years in the trend, up to 20. Used only when **include\_trend** is true.Default: 5

</td></tr><tr><td>

**limit**, **offset**

</td><td>

Pagination controls.Default: 100 records, starting at offset 0

</td></tr></tbody>
</table>## App Rationalization Query

<table id="table_ea_mcp_param_app_rat"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**operation**

</td><td>

Query to run. Possible values:-   `RESOLVE_ENTITY`, `RESOLVE_FISCAL_PERIOD`, `RESOLVE_INDICATOR`: Sys ID of an entity, fiscal period, or indicator, matched by name.
-   `LIST_INDICATORS_FOR_ENTITY`: Indicators that apply to an entity.
-   `GET_OVERALL_SCORE`, `GET_INDICATOR_SCORE`, `GET_FULL_SCORECARD`: Overall score, a single indicator score, or all indicator scores for an entity.
-   `FILTER_ENTITIES_BY_CRITERIA`: Entities that meet one or more score conditions.
-   `COMPARE_PERIODS`: Score trend across fiscal periods.
-   `CLASSIFY_QUADRANT`: Rationalization quadrant \(invest, sustain, migrate, or retire\) based on two indicators.
-   `SCORE_DISTRIBUTION`: Portfolio-wide distribution of an indicator or overall score.
-   `GET_TPM_RISK`, `FILTER_BY_TPM_RISK`: TLM technology risk score for an entity, or entities above or below a risk threshold.

Required.

</td></tr><tr><td>

**entity\_type**

</td><td>

Type of entity to query. For score operations: `business_app` or `business_capability`. For technology risk operations: `business_app`, `service`, `hardware_product_model`, or `software_product`. Required for all operations except `RESOLVE_FISCAL_PERIOD` and `RESOLVE_INDICATOR`.

</td></tr><tr><td>

**op\_args**

</td><td>

Operation-specific arguments, such as the entity name, indicator names, score conditions, or fiscal periods to compare.Required.

</td></tr><tr><td>

**global\_opts**

</td><td>

Optional settings that apply to all operations: the fiscal period to score against, pagination \(default 200 records, maximum 500\), and whether to include entity names in the results.

</td></tr></tbody>
</table>## Related Entities Resolver

<table id="table_ea_mcp_param_rel_entities"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**mode**

</td><td>

Analysis to perform. Possible values:-   `related`: Entities directly related to the source entities.
-   `list_related`: Full list of source and target pairs, with statistics.
-   `not_related`: Source entities that have no relationship to the target type, for example, applications without any service.
-   `not_related_multi_hop`: Source entities with no indirect relationship through a path of two or three tables, for example, applications without servers through their services.
-   `counts_only`: Relationship counts and statistics per source entity, for example, applications with more than three services.
-   `traverse`: Multi-level impact or dependency analysis from a single configuration item \(CI\), for example, what depends on a database.

Required.

</td></tr><tr><td>

**source\_table**, **target\_table**

</td><td>

Tables of the source and target entities, which must be directly related through CI relationships. Required for all modes except `not_related_multi_hop` and `traverse`.

</td></tr><tr><td>

**source\_names**

</td><td>

Names of up to 50 source entities to restrict the query to.

</td></tr><tr><td>

**rel\_type\_sys\_id**

</td><td>

Sys ID of a relationship type, used when more than one relationship type exists between the same two tables.

</td></tr><tr><td>

**path**

</td><td>

Two or three table names, from source to target, for the `not_related_multi_hop` mode.

</td></tr><tr><td>

**ci\_name**, **ci\_sys\_id**

</td><td>

Name or sys ID of the CI to start from, for the `traverse` mode. A name that matches more than one CI returns the candidates to choose from.

</td></tr><tr><td>

**direction**

</td><td>

Direction of the `traverse` analysis. Possible values:-   `up`: What depends on the CI \(impact analysis\).
-   `down`: What the CI depends on.
-   `both`: Both directions.

Default: up

</td></tr><tr><td>

**max\_levels**

</td><td>

Number of relationship levels to traverse, up to 10.Default: 6

</td></tr><tr><td>

**max\_nodes**

</td><td>

Number of CIs to discover during traversal, up to 500. When the limit is reached before all levels are traversed, the response indicates that the results may be partial.Default: 250

</td></tr><tr><td>

**target\_class**

</td><td>

CI class to filter traversal results to, for example, `cmdb_ci_business_capability`.

</td></tr><tr><td>

**include\_paths**

</td><td>

Option to include the relationship path from each discovered CI back to the starting CI.Default: true

</td></tr><tr><td>

**include\_svc\_assoc**

</td><td>

Option to also traverse service-to-CI associations, in addition to CI relationships.Default: false

</td></tr><tr><td>

**limit**, **offset**

</td><td>

Pagination controls.Default: 100 records \(`counts_only` mode: up to 5,000; `traverse` mode: 10, up to 30\), starting at offset 0

</td></tr></tbody>
</table>## Artifact Resolver

<table id="table_ea_mcp_param_artifact"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**mode**

</td><td>

Lookup to perform. Possible values:-   `artifacts_for_entity`: Architectural artifacts, such as documents and diagrams, linked to an entity.
-   `entities_for_artifact`: Entities that an architectural artifact documents.
-   `all_for_table`: Entity-to-artifact mapping for all entities in a table.

Default: artifacts\_for\_entity

</td></tr><tr><td>

**entity\_name**

</td><td>

Name of the entity \(`artifacts_for_entity` mode\) or of the architectural artifact \(`entities_for_artifact` mode\). Not used in the `all_for_table` mode.

</td></tr><tr><td>

**entity\_table**

</td><td>

Table of the entities to look up. Possible values: `cmdb_ci_business_app`, `cmdb_ci_service`, `cmdb_ci_business_capability`, `cmdb_ci_information_object`, `cmdb_ci_appl`, or `cmdb_ci_business_service`. Required for the `artifacts_for_entity` and `all_for_table` modes.

</td></tr><tr><td>

**limit**, **offset**

</td><td>

Pagination controls.Default: 10 records, up to 30, starting at offset 0

</td></tr></tbody>
</table>## Diagram change analysis

This tool is available only when the Enterprise Modeling and Visualization plugin \(com.snc.apm\_modelling\_tool\) is installed on your instance.

<table id="table_ea_mcp_param_diagram"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**action\_type**

</td><td>

Analysis to perform. Possible values:-   `summary`: Structured overview of a single diagram, identifying the central business application and its connected entities.
-   `compare`: Comparison of two diagram versions, with the added, removed, and modified elements and a business-impact summary.

Default: compare

</td></tr><tr><td>

**diagram\_version\_a**

</td><td>

Sys ID of the diagram instance to summarize, or of the baseline version when comparing.Required.

</td></tr><tr><td>

**diagram\_version\_b**

</td><td>

Sys ID of the updated diagram version to compare against the baseline. Required for the `compare` action.

</td></tr><tr><td>

**diagram\_type**

</td><td>

Type of diagram. Possible values: Business Hierarchy Map, Business Capability Map, or Business Process Map.Default: Business Hierarchy Map

</td></tr><tr><td>

**output\_granularity\_level**

</td><td>

Level of detail in the comparison output. Possible values: `executive` \(business summary\) or `high` \(detailed\).Default: executive

</td></tr></tbody>
</table>**Parent Topic:**[MCP for Enterprise Architecture reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-portfolio-management/reference-ea-mcp-server.md)


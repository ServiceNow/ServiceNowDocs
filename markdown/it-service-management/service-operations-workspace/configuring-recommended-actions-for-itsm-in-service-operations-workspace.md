---
title: Configuring Recommended Actions for ITSM in Service Operations Workspace
description: Configure contexts, rules, recommendations, and resource generators to provide agents with AI-powered suggestions when working with incidents, problems, change requests, and other records in Service Operations Workspace in ITSM.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/service-operations-workspace/configuring-recommended-actions-for-itsm-in-service-operations-workspace.html
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-09-01"
reading_time_minutes: 8
keywords: [recommended actions, ITSM, Service Operations Workspace, AI-powered suggestions, incident management, problem management, change management, contexts, rules, recommendations, resource generators, guidance-based recommendations, field-level recommendations, AI search, Task Intelligence, Predictive Intelligence, major incident, similar incidents, knowledge articles, agent productivity]
breadcrumb: [Contextual side panel configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Configuring Recommended Actions for ITSM in Service Operations Workspace

Configure contexts, rules, recommendations, and resource generators to provide agents with AI-powered suggestions when working with incidents, problems, change requests, and other records in Service Operations Workspace in ITSM.

## Contexts in Recommended Actions for ITSM

 A context enables agents to see recommendations for a specific type of record when certain rules are met. These recommendations can help agents by suggesting actions to take based on the record context.  For more information, see [Contexts in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-contexts.md).

The ITSM base system ships the following contexts:

-   Incident
-   Incident task
-   Problem
-   Problem task
-   Change request
-   Change task
-   Interaction
-   Request

For more information about the field description of this context, see [Contexts in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/contexts-in-recommended-actions-for-itsm.md).

**Note:** Recommended Actions have now introduced a context for the Interaction table.

To get the correct Recommended Actions context, you must set up the **Context Sys ID** property in the Recommended Actions record page of UI Builder in Service Operations Workspace.

To configure the Context ID, see **Configuring a context record for Recommended Actions component** section in [Create a context in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-contexts-create.md).

## Rules in Recommended Actions for ITSM

A rule is a set of conditions that applies to a context. A rule shows recommendations to agents with certain roles for records that meet certain conditions. For more information, see [Rules in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-rules.md).

The ITSM base system includes the following rules:

-   Active incident
-   Active non-child non-MI Incident
-   AI Search
-   Major Incident with no Problem record

**Note:** These rules are available only for the Incident context.

For more information about the field descriptions of these rules, see [Rules in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/rules-in-recommended-actions-for-itsm.md).

**Note:** To create a rule, see [Create a rule in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-rules-create.md).

## Recommendations in Recommended Actions for ITSM

A recommendation is a way to suggest a helpful action to an agent. A recommendation includes the action and any relevant resources and inputs. For more information about recommendations and types, see [Recommendations in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-recommendations.md).

**Note:** To create a recommendation, see [Create a recommendation in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-recommendations-create.md).

The ITSM base system includes Guidance-based recommendations and Field-level recommendation types.

## Guidance-based recommendations

The ITSM base system includes these guidance-based recommendations:

-   AI Search Recommendation
-   Create Problem Record for a Major Incident
-   Open incidents \(CI &amp; Service\)
-   Open PRBs \(CI &amp; Service\)
-   Similar Incidents \(TI\)
-   Similar KB Articles \(Similarity\)
-   Propose major incident \(Trend\)
-   Similar major incidents \(Trend\)
-   Similar open Incidents \(Similarity\)
-   Similar open PRBs \(Similarity\)
-   Similar resolved incidents \(CI &amp; Service\)
-   Similar resolved incidents \(Similarity\)

For more information about the field descriptions of the guidance-based recommendations, see [Guidance based recommendations in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/guidance-based-recommendations-in-recommended-actions-for-itsm.md).

## Field-level recommendations

The ITSM base system includes the following field-level recommendations:

-   Predictive Intelligence -based recommendations:
    -   Assignment Group \(Classification\)
    -   Configuration Item \(Classification\)
    -   Service \(Classification\)
-   Task Intelligence for ITSM -based recommendation: Incident Fields value prediction \(TI\)

    **Note:** All Predictive Intelligence -based recommendations included in the ITSM base system are inactive by default. To activate them, navigate to the Recommendations screen, edit the corresponding Active column to the required recommendation of **true**, and select **Update**.


For more information about the field-level recommendations field descriptions, see [Field level recommendations in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/field-level-recommendations-in-recommended-actions-for-itsm.md).

**Note:** To create a recommendation, see [Create a recommendation in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-recommendations-create.md).

To create a guidance and field recommendations, see [Creating guidance and field recommendation in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-config-recommendations.md).

## Resource generators in Recommended Actions for ITSM

The ITSM base system includes the following resource generators:

-   AI Search Resource Generator
-   Assignment group using Classification.
-   Configuration item using Classification
-   Incident Fields predictions TI
-   Similar Open Incidents with same CI &amp; Service
-   Open PRBs using CI &amp; Service
-   Propose major incident using trend
-   Service using Classification
-   Similar KBs using similarity
-   Similar major incident using trend
-   Similar open incidents using Similarity
-   Similar open incidents with same CI &amp; Service
-   Similar incidents using TI similarity
-   Similar PRBs using similarity
-   Resolved Incidents with same CI &amp; Service
-   Similar resolved incidents using similarity.

For more information about the field descriptions of resource generators, see [Resource generators in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/resource-generators-in-recommended-actions-for-itsm.md).

For more information about the types of resource generator, see [Resource generators in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-resource-generators.md).

**Note:** To create a resource generator, see [Create a resource generator in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-resource-generators-create.md).

## Guidances

The ITSM base system includes the following guidance:

-   Link to major incident
-   Propose Major Incident
-   Review and attach article for incident
-   Show Change request \[No Action\]
-   Show genius result \[No Action\]
-   Show Problem \[No Action\]
-   \[Incident\] Attach KB
-   \[Incident\] Copy resolution
-   \[Incident\] Link open incident
-   \[Incident\] Link open problem
-   \[Interaction\] Review and attach article
-   \[ Non-ML\] Copy resolution
-   \[ Non-ML\] Create Problem
-   \[ Non-ML\] Link open incident
-   \[ Non-ML\] Link open problem
-   \[Task\] Link change request
-   \[Task\] Link incident
-   \[Task\] Link outage
-   \[Task\] Link problem
-   \[Task\] Order item

For more information about the field descriptions of the guidance, see [Guidances in Recommended Actions for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/guidances-in-recommended-actions-for-itsm.md).

**Note:** To create guidance, see [Create a guidance in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/ra-csm-guidances-create.md).

## Search result mappings

The search result mappings appear in AI search results for various records in the Service Operations Workspace.

The IT Service Management base system includes the following search result mappings based on context type:

<table id="table_o3z_l2b_gkc"><thead><tr><th>

Context type

</th><th>

Search result mappings

</th></tr></thead><tbody><tr><td>

Incident

</td><td>

-   Outage \[cmdb\_ci\_outage\]
-   Knowledge \[kb\_knowledge\]
-   Change Request \[change\_request\]
-   Incident \[incident\]
-   Incident \[incident\]- Genius result for Pro plus users

**Note:** Genius result uses ServiceNow Otto Multi-Content Response.

-   Catalog item \[sc\_cat\_item\]
-   Problem \[problem\]

</td></tr><tr><td>

Incident task

</td><td>

-   Knowledge \[kb\_knowledge\]
-   Incident \[incident\]
-   Catalog item \[sc\_cat\_item\]
-   Problem \[problem\]

</td></tr><tr><td>

Problem

</td><td>

-   Outage \[cmdb\_ci\_outage\]
-   Knowledge \[kb\_knowledge\]
-   Change Request \[change\_request\]
-   Incident \[incident\]
-   Catalog item \[sc\_cat\_item\]
-   Problem \[problem\]

</td></tr><tr><td>

Problem task

</td><td>

Knowledge \[kb\_knowledge\]

</td></tr><tr><td>

Change request

</td><td>

-   Knowledge \[kb\_knowledge\]
-   Change Request \[change\_request\]
-   Incident \[incident\]
-   Catalog item \[sc\_cat\_item\]
-   Problem \[problem\]

</td></tr><tr><td>

Change task

</td><td>

-   Knowledge \[kb\_knowledge\]
-   Change Request \[change\_request\]
-   Incident \[incident\]
-   Catalog item \[sc\_cat\_item\]
-   Problem \[problem\]

</td></tr><tr><td>

Interaction

</td><td>

-   Knowledge \[kb\_knowledge\]
-   Catalog item \[sc\_cat\_item\]

</td></tr><tr><td>

Request

</td><td>

-   Knowledge \[kb\_knowledge\]
-   Catalog item \[sc\_cat\_item\]

</td></tr></tbody>
</table>## Search Application Configuration

The IT Service Management base system includes the **\[AIS\] Recommended Actions for ITSM Search Config**. This application supports the AI search for various records in the Service Operations Workspace, including Incident, Incident Tasks, Problem, Problem Tasks, Change Request, Change Request Task, Interaction, and Request.

## Advanced Recommended actions for ITSM

The standard version of Recommended Actions for ITSM is provided as a part of the Service Operations Workspace application.

The Advanced Recommended actions for ITSM \(sn\_sow\_itsm\_ra\_adv\) plugin is included with the ITSM Pro package subscription.

With Advanced Recommended actions for ITSM, your agents can use recommendations powered by Task Intelligence, including:

-   Incident fields value prediction
-   Similar incidents
-   Similar open change requests
-   Similar open problems
-   Similar major incidents
-   Propose major incident

For more information, see [Task Intelligence for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/task-intelligence-for-itsm/c-itsm-task-intelligence.md).

**Note:** The Advanced Recommended actions for ITSM \(sn\_sow\_itsm\_ra\_adv\) and Task Intelligence Admin Console \(com.sn\_ti\_admin\) plugins are installed as dependencies of the ITSM Pro package subscription.

## Predictive Intelligence

To use recommendations powered by Predictive Intelligence, install the following plugins:

-   Install the Predictive Intelligence for Incident \(com.snc.incident.ml\) plugin to install the Relevant problems solution definition-Similar open PRBs \(Similarity\). For information about this plugin installation, see [Request Predictive Intelligence for Incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/request-predictive-intelligence-for-im.md).
-   Install the Problem Management for Service Operations Workspace \(**com.snc.uib.sow\_problem**\) plugin to install the solution definition-Create Problem for Major incident.
-   Install the Predictive Intelligence for Major Incident Management \(com.snc.incident.mim.ml\_solution\) plugin to install the following IT Service Management solution definitions.

    -   Propose major incident \(Trend\)
    -   Similar major incident \(Trend\)
    For information about this plugin installation, see [Request Predictive Intelligence for Major Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/request-pred-intelli-mim.md).

-   Install the Predictive Intelligence for Incident Management \(com.snc.incident.ml\_solution\) plugin to install the following IT Service Management solution definitions.

    -   Assignment group \(Classification\)
    -   Configuration item \(Classification\)
    -   Service \(Classification\)
    -   Similar open incidents \(Similarity\)
    -   Similar KB articles \(Similarity\)
    -   Similar resolved incidents \(Similarity\)
    -   Similar Incidents \(TI\)

        **Note:** Similar Incidents \(TI\) recommendation is available only from Service Operations Workspace version 6.0.

    For more information, see [Request Predictive Intelligence for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/request-pred-intelli-inc-mgmt.md).


Train solution definitions to predict recommendations for an incident. For information about training solution definitions, see [Predictive Intelligence for Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/predictive-intelligence-for-incident.md)

-   **[Recommended Actions for ITSM Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/sow-itsm-ra-workflow.md)**  
Configure AI-driven recommendations for ITSM records by creating contexts, setting rules, and defining resource generators with action types. Use this workflow to enable guidance-based and field-level recommendations in Service Operations Workspace.
-   **[Access Recommended Actions for ITSM Panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/sow-itsm-access-ra-panel.md)**  
Agents access recommended actions in Service Operations Workspace to view a list of recommendations that are presented to help to resolve incidents. They can also manually search for AI-powered recommendations to quickly find solutions.

**Parent Topic:**[Contextual side panel configurations in Service Operations Workspace for ITSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/service-operations-workspace/contextual-side-panel-configurations-sow-itsm.md)


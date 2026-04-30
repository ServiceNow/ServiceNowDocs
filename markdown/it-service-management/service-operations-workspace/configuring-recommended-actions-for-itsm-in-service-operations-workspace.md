---
title: Configuring Recommended Actions for ITSM in Service Operations Workspace
description: IT Service Management \(ITSM\) includes the following base system components used to configure Recommended Actions for various records in the Service Operations Workspace, including Incident, Incident Tasks, Problem, Problem Tasks, Change Request, Change Request Task, Interaction, and Request.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Contextual side panel configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configuring Recommended Actions for ITSM in Service Operations Workspace

IT Service Management \(ITSM\) includes the following base system components used to configure Recommended Actions for various records in the Service Operations Workspace, including Incident, Incident Tasks, Problem, Problem Tasks, Change Request, Change Request Task, Interaction, and Request.

## Contexts in Recommended Actions for ITSM

 A context enables agents to see recommendations for a specific type of record when certain rules are met. These recommendations can help agents by suggesting actions to take based on the record context.  For more information, see [Contexts in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-contexts&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

The ITSM base system ships the following contexts:

-   Incident
-   Incident task
-   Problem
-   Problem task
-   Change request
-   Change task
-   Interaction
-   Request

For more information about the field description of this context, see [Contexts in Recommended Actions for ITSM](../reference/contexts-in-recommended-actions-for-itsm.md).

**Note:** Recommended Actions have now introduced a context for the Interaction table.

To get the correct Recommended Actions context, you must set up the **Context Sys ID** property in the Recommended Actions record page of UI Builder in Service Operations Workspace.

To configure the Context ID, see **Configuring a context record for Recommended Actions component** section in [Create a context in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-contexts-create&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Rules in Recommended Actions for ITSM

A rule is a set of conditions that applies to a context. A rule shows recommendations to agents with certain roles for records that meet certain conditions. For more information, see [Rules in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-rules&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

The ITSM base system includes the following rules:

-   Active incident
-   Active non-child non-MI Incident
-   AI Search
-   Major Incident with no Problem record

**Note:** These rules are available only for the Incident context.

For more information about the field descriptions of these rules, see [Rules in Recommended Actions for ITSM](../reference/rules-in-recommended-actions-for-itsm.md).

**Note:** To create a rule, see [Create a rule in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-rules-create&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Recommendations in Recommended Actions for ITSM

A recommendation is a way to suggest a helpful action to an agent. A recommendation includes the action and any relevant resources and inputs. For more information, see [Recommendations in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-recommendations&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

For more information about recommendation types, see [Recommendations in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-recommendations&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Note:** To create a recommendation, see [Create a recommendation in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-recommendations-create&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

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

For more information about the field descriptions of the guidance-based recommendations, see [Guidance based recommendations in Recommended Actions for ITSM](../reference/guidance-based-recommendations-in-recommended-actions-for-itsm.md).

## Field-level recommendations

The ITSM base system includes the following field-level recommendations:

-   Predictive Intelligence -based recommendations:
    -   Assignment Group \(Classification\)
    -   Configuration Item \(Classification\)
    -   Service \(Classification\)
-   Task Intelligence for ITSM -based recommendation: Incident Fields value prediction \(TI\)

    **Note:** All Predictive Intelligence -based recommendations included in the ITSM base system are inactive by default. To activate them, navigate to the Recommendations screen, edit the corresponding Active column to the required recommendation of **true**, and select **Update**.


For more information about the field-level recommendations field descriptions, see [Field level recommendations in Recommended Actions for ITSM](../reference/field-level-recommendations-in-recommended-actions-for-itsm.md).

**Note:** To create a guidance and field recommendations, see [Creating guidance and field recommendation in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-config-recommendations&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

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

For more information about the field descriptions of resource generators, see [Resource generators in Recommended Actions for ITSM](../reference/resource-generators-in-recommended-actions-for-itsm.md).

For more information about the types of resource generator, see [Resource generators in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

**Note:** To create a resource generator, see [Create a resource generator in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-resource-generators-create&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

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

For more information about the field descriptions of the guidance, see [Guidances in Recommended Actions for ITSM](../reference/guidances-in-recommended-actions-for-itsm.md).

**Note:** To create guidance, see [Create a guidance in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-guidances-create&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

## Search result mappings

The search result mappings appear in AI search results for various records in the Service Operations Workspace, including Incident, Incident Tasks, Problem, Problem Tasks, Change Request, Change Request Task, Interaction, and Request.

The IT Service Management base system includes the following search result mappings based on context type:

-   Incident: Outage \[cmdb\_ci\_outage\], Knowledge \[kb\_knowledge\], Change Request \[change\_request\], Incident \[incident\], Catalog item \[sc\_cat\_item\], Incident \[incident\]- Genius result for Pro plus users, Problem \[problem\]
-   Incident task: Knowledge \[kb\_knowledge\], Incident \[incident\], Catalog item \[sc\_cat\_item\], Problem \[problem\]
-   Problem: Outage \[cmdb\_ci\_outage\], Knowledge \[kb\_knowledge\], Change Request \[change\_request\], Incident \[incident\], Catalog item \[sc\_cat\_item\], Problem \[problem\]
-   Problem task: Knowledge \[kb\_knowledge\]
-   Change request: Knowledge \[kb\_knowledge\], Change Request \[change\_request\], Incident \[incident\], Catalog item \[sc\_cat\_item\], Problem \[problem\]
-   Change task: Knowledge \[kb\_knowledge\], Change Request \[change\_request\], Incident \[incident\], Catalog item \[sc\_cat\_item\], Problem \[problem\]
-   Interaction: Knowledge \[kb\_knowledge\], Catalog item \[sc\_cat\_item\]
-   Request: Knowledge \[kb\_knowledge\], Catalog item \[sc\_cat\_item\]

## Search Application Configuration

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

For more information, see [Task Intelligence for ITSM](../../task-intelligence-for-itsm/concept/c-itsm-task-intelligence.md).

**Note:** The Advanced Recommended actions for ITSM \(sn\_sow\_itsm\_ra\_adv\) and Task Intelligence Admin Console \(com.sn\_ti\_admin\) plugins are installed as dependencies of the ITSM Pro package subscription.

## Predictive Intelligence

To use recommendations powered by Predictive Intelligence, install the following plugins:

-   Install the Predictive Intelligence for Incident \(com.snc.incident.ml\) plugin to install the Relevant problems solution definition-Similar open PRBs \(Similarity\). For information about this plugin installation, see [Request Predictive Intelligence for Incident](../../incident-management/task/request-predictive-intelligence-for-im.md).
-   Install the Problem Management for Service Operations Workspace \(**com.snc.uib.sow\_problem**\) plugin to install the solution definition-Create Problem for Major incident.
-   Install the Predictive Intelligence for Major Incident Management \(com.snc.incident.mim.ml\_solution\) plugin to install the following IT Service Management solution definitions.

    -   Propose major incident \(Trend\)
    -   Similar major incident \(Trend\)
    For information about this plugin installation, see [Request Predictive Intelligence for Major Incident Management](../../incident-management/task/request-pred-intelli-mim.md).

-   Install the Predictive Intelligence for Incident Management \(com.snc.incident.ml\_solution\) plugin to install the following IT Service Management solution definitions.

    -   Assignment group \(Classification\)
    -   Configuration item \(Classification\)
    -   Service \(Classification\)
    -   Similar open incidents \(Similarity\)
    -   Similar KB articles \(Similarity\)
    -   Similar resolved incidents \(Similarity\)
    -   Similar Incidents \(TI\)

        **Note:** Similar Incidents \(TI\) recommendation is available only from Service Operations Workspace version 6.0.

    For more information, see [Request Predictive Intelligence for Incident Management](../../incident-management/task/request-pred-intelli-inc-mgmt.md).


Train solution definitions to predict recommendations for an incident. For information about training solution definitions, see [Predictive Intelligence for Incident Management](../../incident-management/concept/predictive-intelligence-for-incident.md)

**Parent Topic:**[Contextual side panel configurations in Service Operations Workspace for ITSM](contextual-side-panel-configurations-sow-itsm.md)


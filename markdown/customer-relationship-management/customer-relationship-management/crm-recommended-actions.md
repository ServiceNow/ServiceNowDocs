---
title: Recommended Actions
description: Recommended Actions is a context-aware recommendation framework that displays relevant, actionable guidance to users directly within workspaces based on the context of the record they are working on. It acts as a one‑stop experience that combines contextual actions, guided decisions, rule-based and AI-driven recommendations, and AI Search to help users resolve issues faster and more consistently across workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 4
---

# Recommended Actions

Recommended Actions is a context-aware recommendation framework that displays relevant, actionable guidance to users directly within workspaces based on the context of the record they are working on. It acts as a one‑stop experience that combines contextual actions, guided decisions, rule-based and AI-driven recommendations, and AI Search to help users resolve issues faster and more consistently across workflows.

## Recommended Actions overview

Recommended Actions is a configurable component that evaluates the active record \(such as a case, incident, or interaction\) against configurable rules and surfaces contextually relevant recommendations automatically in the contextual side panel of supported workspaces to agents. These recommendations can include guidance cards with actions, guided decision trees, field-level suggestions, and AI Search results. It is designed as a horizontal platform capability, meaning it works across multiple products and workflows rather than being limited to a single application.

The Suggested actions tab in Recommended Actions surfaces context-aware, actionable recommendations that agents can take directly to progress or resolve a record, such as applying resolutions, linking related records, or initiating guided actions. These suggestions are generated based on record context, configured rules, and underlying resource generators, ensuring that only relevant actions appear at the right stage of the agent’s workflow.

AI search in Recommended Actions is built on the AI Search framework, which combines vector-based semantic search with traditional keyword matching to retrieve results from knowledge bases and similar case repositories. Matching logic evaluates contextual inputs from the active record, such as short description, category, and customer details, against indexed content and scores results according to the configured relevancy model.

## Recommended Actions benefits

Recommended Actions provides benefits to internal users across an organization.

-   Improves agent productivity by surfacing the right actions at the right time without manual searching.
-   Reduces time to resolution \(MTTR\) through proactive and contextual guidance.
-   Provides consistency in resolution by promoting proven actions such as applying resolutions from similar cases or attaching relevant knowledge.
-   Supports extensibility and low-code configuration, enabling admins to tailor recommendations using rules, contexts, and guidances.
-   Unifies multiple recommendation types \(rule-based, ML-based, and GenAI-driven\) in a single experience.

## Products and contexts

Recommended Actions is available across the CRM solution, with each product context supporting independent configuration of knowledge sources and search behavior.

-   **CSM**

    Customer service agents use Recommended Actions to identify resolution paths for cases across service categories. Administrators can configure the component for each case type, connecting the relevant knowledge bases, setting contextual inputs such as case short description and category, and applying dynamic filters to restrict results by product, language, or support tier. Similar case results can be enabled alongside knowledge articles so agents can view how comparable cases were resolved.

-   **FSM**

    Field service technicians and dispatchers use Recommended Actions to access service procedures, equipment manuals, and resolution guides relevant to the active work order. The component can be configured with work order fields, such as asset type, failure code, and location, as contextual inputs, so returned results reflect the specific equipment and issue being addressed. Administrators can configure separate instances for dispatcher and technician record pages with distinct knowledge sources and filter criteria for each role.

-   **Sales CRM**

    Sales CRM users can use Recommended Actions to surface product documentation, pricing guidance, and resolution steps relevant to active orders and cases. Administrators configure the component with order and account fields as contextual inputs to return content appropriate to the sales or fulfillment context.

-   **Industry solutions**

    Telecommunications, financial services, and manufacturing solutions include preconfigured Recommended Actions setups tailored to the knowledge sources and workflows common in those industries. Organizations can deploy preconfigured configurations as a starting point and modify the knowledge sources, contextual inputs, and relevancy settings in UI Builder as requirements evolve.


## Use cases

-   **Customer service: tiered support operations**

    A customer service organization operates separate tier-1 and tier-2 teams, each with access to different knowledge bases. Administrators configure two Recommended Actions instances: one for the tier-1 record page, pointing to the general product knowledge base, and one for the tier-2 page, pointing to the advanced technical repository. Dynamic filters restrict tier-1 results to articles marked for general support audiences, while tier-2 results surface technical procedures and engineering notes.

    When tier-1 agents receive cases, Recommended Actions returns relevant general resolution guidance without surfacing advanced content intended for specialist teams. When cases are escalated to tier-2, agents see the technical articles and similar cases appropriate to the complexity of the issue.

-   **Field service: telecommunications**

    A telecom provider uses Recommended Actions on work order record pages in the FSM Configurable Workspace to help field technicians locate installation and fault-resolution procedures on-site. The component is configured with equipment type, fault code, and service area as contextual inputs. Dynamic filters restrict results by equipment model and certified procedure status.

    When a technician opens a work order for a fiber splice fault, Recommended Actions returns procedures specific to that equipment model and fault type. The technician can review the steps, mark the procedure as used, and attach it to the work order, all without leaving the record page or navigating to a separate knowledge portal.

-   **Financial services: consumer banking**

    A retail bank configures Recommended Actions for agents handling mortgage complaint cases in the CSM Configurable Workspace. The component is connected to the bank's complaint resolution knowledge base and a repository of regulatory guidance. Contextual inputs include complaint category, product type, and SLA status. A relevancy threshold is set to suppress low-confidence matches that could mislead agents working within regulatory constraints.

    When agents open complaint cases, Recommended Actions surfaces the applicable resolution procedures and regulatory requirements for the specific complaint and product type. Agents can apply guidance directly from the component without consulting a separate reference system, reducing average handling time and supporting consistent application of regulated procedures.


**Related topics**  


[bundle-csm.configure-nba]

[bundle-csm.configure-recommended-actions]

[bundle-csm.ra-configuring-ai-search]

[bundle-csm.recommended-actions-use-case]


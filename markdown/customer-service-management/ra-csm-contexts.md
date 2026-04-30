---
title: Contexts in Recommended Actions
description: A context enables agents to see recommendations for records from a table when certain rules are met. These recommendations can help agents by suggesting actions to take based on the record context.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Contexts in Recommended Actions

A context enables agents to see recommendations for records from a table when certain rules are met. These recommendations can help agents by suggesting actions to take based on the record context.

Contexts are created for tables, such as the Case \[sn\_customerservice\_case\] table or the Incident \[incident\] table. Creating a context includes the following steps:

-   Selecting a table.
-   Creating rules for the context. A rule shows recommendations to agents with certain roles for records that meet certain conditions.
-   Creating recommendations for the rules. A recommendation is a way to suggest a helpful action to an agent.

The Recommended Actions application includes a context record, Case Context, that you can use to create recommendations for cases.

The Recommended Actions application supports multiple context records per table. This enables users to create different experiences based on criteria such as user attributes or domains.

One context record per table can be active at a time. The Recommended Actions component can be configured in UI Builder to use the active context record. The recommendations and AI Search results adjust dynamically according to the configured active context.

## Context form

You can access context records by navigating to **All** &gt; **Recommended Actions** &gt; **Contexts**. The Contexts list displays a brief description of each context and the table that the context applies to.

The Context form includes the name and description of the context, the selected table, and a search application configuration for AI search. When you create a context, provide this information and save the record. After saving, the Context form displays the following related lists.

-   **Rules**: Displays the rules that have been created for the context, including the selected user roles. You can create a rule only from the Rules related list on the Context form.
-   **Recommendations**: Displays the recommendations associated with the context rules, including the action type and action. You can create a recommendation only from the Recommendation related list on the Rule form.
-   **Search result mapping**: Displays mappings between AI search outputs and Recommended Actions inputs.
-   **Inherited rules**: Displays the rules inherited from the parent context. The Inherited rules related list appears only for the contexts that have the parent context assigned. For more information on how the parent context rules are inherited by the child context, see [Apply rules to tables extended from the context table](ra-csm-rules.md#section_rules-apply-extended-tables).
-   **Extended contexts**: Displays all the contexts which use the current context as a parent context. This related list appears only for the parent contexts.

The Contexts list includes an Active column. You can use this column to view and set the Active value for a context record. The Context form includes an **Active** field that you can use to activate or deactivate a context record.

**Note:** A table can have only one active context record at a time.

## Refresh interval field

The **Refresh interval** field on the Context form determines how frequently recommendations are refreshed for the context. The default value for this field is 12 hours and the minimum value is 10 minutes.

**Note:** You must configure the form view to display the **Refresh interval** field.

## Synchronous and asynchronous modes of evaluation for Recommended Actions

As an admin, you can configure the loading behavior at the context level for Recommended Actions, by choosing between synchronous and asynchronous modes. In synchronous mode, recommendations are loaded before the page becomes interactive, ensuring a complete view is available before any action is taken. In asynchronous mode, recommendations load in the background without blocking the user interface, allowing agents to start interacting with the record immediately. Each mode is tailored to meet different performance and user experience requirements.

The **Asynchronous Evaluation** check box in the Context form, when selected enables the agents to make updates and perform actions on the case or incident record while the recommendations load on the contextual side panel. By selecting this field, an admin or RA author can enable asynchronous processing for recommended actions.

The **sn\_nb\_action.async\_ra\_timeout** system property specifies the timeout duration \(in seconds\) for an asynchronous process to generate the recommendations. This value serves as a guideline for managing execution time and preventing excessive delays. The default value is set to 30 seconds, and the maximum value can be 180 seconds. If the generation of recommended actions takes more than 30 seconds, the **Retry** button on the contextual side panel appears. The retry process starts in synchronous mode - it runs directly during user interaction instead of processing asynchronously.

## Inheriting the rules and recommendations from hierarchical contexts

The parent context field appears only when the table selected in the Table field has one or more parent tables for which context is defined. Using the Parent context field, you can import it's active rules and recommendations into the extended context. When you click the search icon on this field, the list of contexts of parent tables is displayed. You can select any one parent context from the list. The rules that are inherited appear in the Inherited Rules related list. For more information on how to configure rules so that the recommendations are inherited by the extended context, see [Apply rules to tables extended from the context table](ra-csm-rules.md#section_rules-apply-extended-tables).

## Inheriting the rules and recommendations from hierarchical contexts

Consider the following tables and their contexts, rules, and recommendations. Table 1 is the parent table for Table 2 and Table 3. Table 3 is the parent table for Table 4. Table 2 is the parent table for Table 5.

|Table|Context|Rule|Recommendation|
|-----|-------|----|--------------|
|Table 1|Context 1 \(Active\)|Rule 1 \(Active\)|Recommendation 1|
|Table 2|Context 2 \(Inactive\)|Rule 2 \(Inactive\)|Recommendation 2A and Recommendation 2B|
|Table 3|Context 3 \(Active\)|Rule 3 \(Active\)|Recommendation 3|
|Table 4|Context 4 \(Active\)|Rule 4 \(Active\)|Recommendation 4|
|Table 5|Context 5 \(Active\)|Rule 5 \(Active\)|Recommendation 5|

In the Context form:

-   Scenario 1: When you add Context 3 in the Parent context field of Context 4, the Rule 3 and Recommendation 3 are inherited by Context 4.
-   Scenario 2: When you add Context 2 in the Parent context field of Context 5, the Rule 2 and its recommendation 2A and 2B aren’t inherited by Context 5 as the Rule 2 is inactive.

## Creating multiple context records for the same table

Starting with v14.0 of Recommended Actions, the **Avoid duplicate active entry for context** business rule allows the creation of more than one context per table. You can create more than one context for the same table. This enables you to configure precise recommendations for various types of records in the same table.

The following are use cases where you can create different contexts for the same table:

-   **Use case 1: Different roles may interact with the same table but need tailored actions or views.**

    Consider the Interaction table. The same interaction data can be worked upon differently based on the user persona.

    -   Context A: Show field recommendations for resolution, or related change tasks/catalog items, or standard knowledge articles for the IT Support Agent on the Interaction record page.
    -   Context B: Surface similar resolved case or relevant knowledge article recommendations for the Customer Service Support Agent on the Interaction record page.
-   **Use case 2: Each context may use a different Predictive Intelligence model or AI model variant for recommendations.**

    Enables testing and adoption of ML models in parallel without conflict.

    -   Context A: Use similarity model for Recommended Actions.
    -   Context B: Use classification model for categorization or assignment.
-   **Use case 3: Users may access the same record through different channels—chat, email, voice, etc., requiring tailored recommendations.**

    Entry points provide different signals and user intent.

    -   Context A: When the case is created via Chat Agent, recommend and share the KB article in chat action.
    -   Context B: When the case is accessed via Phone Support, surface KB articles and enable sharing via SMS channel.

## Configuring a context record for the Recommended Actions component

When configuring the Recommended Actions component in UI Builder, users with the Recommended Actions admin role \(next\_best\_action\_admin\) can set a component input property that maps the active context record to the component.

On the Config tab for the Recommended Actions component, enter the sys id of the active context record in the **Context Sys id** field. For more information about configuring UI Builder components, see [Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

**Note:** If the **Context Sys id** field is empty, the system uses the oldest context record for that entity to map to the Recommended Actions component.

## Case Context record

The Recommended Actions for Customer Service application adds the Case Context record for the Case table \[sn\_customerservice\_case\]. This record is active by default \(Active=true\). For more information on the Case Context record, see .

If an upgrade customer has one or more context records for the Case table available on their instance, the system runs a fix script that deactivates the out-of-box Case Context record \(sets the **Active** field to false\).

**Note:** Ensure that the correct context record for the Case table is active.


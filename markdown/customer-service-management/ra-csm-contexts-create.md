---
title: Create a context in Recommended Actions
description: Create a context for an individual table, such as the Case table. Contexts store information including the recommended actions that agents can use and the rules that determine when those actions are available.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a context in Recommended Actions

Create a context for an individual table, such as the Case table. Contexts store information including the recommended actions that agents can use and the rules that determine when those actions are available.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, or admin

## About this task

A context enables agents to see recommendations for a specific type of record when certain rules are met. These recommendations can help agents by suggesting actions to take based on the record context.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select **New** on the Contexts list.

3.  Fill in the fields on the form.

<table id="table_ecp_mh2_52c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the context.

</td></tr><tr><td>

Table

</td><td>

Table for which the context applies to.If you select a table that already has a context, then a warning message is displayed.

</td></tr><tr><td>

Description

</td><td>

Brief description about the context.

</td></tr><tr><td>

Active \(Optional\)

</td><td>

Check box to make the context active.

</td></tr><tr><td>

Asynchronous Evaluation

</td><td>

When selected, enables asynchronous mode of evaluating recommendations on the contextual side panel in the CSM Workspace. That is, this mode enables agents to work on the case or incident record while the recommendations load on the contextual side panel. For more information, see [Synchronous and asynchronous modes of evaluation for Recommended Actions](../concept/ra-csm-contexts.md#section-ra-async-eval).

</td></tr><tr><td>

Exclude fields

</td><td>

Fields of the context table that do not trigger the Recommendations refresh in the Configurable CSM Workspace, when these fields are updated. Add the context table fields that do not impact recommendations generation.

</td></tr><tr><td colspan="2">

Parent Context Config

</td></tr><tr><td>

Parent context

</td><td>

Enables you to choose which parent table's rules and recommendations must be applied to the context you are working with.**Note:**

-   This field appears when the selected table has a parent table with context defined.
-   This field does not show the parent context which have context inputs configured.
-   If parent context is set, the Context inputs related list does not appear.


</td></tr><tr><td>

Inherit exclusions from parent context

</td><td>

When selected, includes the exclusion fields of the parent context table to prevent the trigger of the Recommendations refresh in the CSM Configurable Workspace.**Note:** This field appears only when a context is added in the Parent context field.

</td></tr><tr><td colspan="2">

Contextual AI Search Config

</td></tr><tr><td id="entry-search-app-config">

Search Application Configuration \(Optional\)

</td><td>

Search application configuration that specifies AI Search as the search engine and the settings to use for the search.You can configure the search result display and refinement settings in the search application configuration. For more information, see [Search application configurations](https://www.servicenow.com/docs/access?context=defining-search-app-cfgs-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

The **\[CSM AIS\] Configurable Workspace Search Config** search application configuration is provided with the CSM Configurable Workspace store application. To access this configuration, navigate to **AI Search** &gt; **Search Experience** &gt; **Search Applications**.

For more information about AI search configurations, see [Configuring AI Search in Recommended Actions](../concept/ra-configuring-ai-search.md).

</td></tr><tr><td>

Default search term

</td><td>

Search term that appears by default.You can map the context input from the pill picker.

</td></tr><tr><td>

Grouping strategy \(Optional\)

</td><td>

Strategy for grouping recommendations.For example, you can define a grouping strategy to group recommendations that have similar criteria.

**Note:** You might need to configure the Context form to display the **Grouping strategy** field. This field is available by default for ITSM Workforce Optimization users.

</td></tr><tr><td>

Refresh interval \(Optional\)

</td><td>

This value determines how often recommendations are refreshed for the context. The default value for this field is 12 hours and the minimum value is 10 minutes.**Note:** You might need to configure the Context form to display the **Refresh interval** field.

</td></tr><tr><td>

Show relevancy score for results

</td><td>

Displays the relevancy score on the search results and recommendations in the Recommended Actions contextual side panel.

</td></tr><tr><td>

Top N results

</td><td>

Limits the number of search results displayed in the AI search tab of Recommended Actions to the top N results for improved precision and easier management. The number of results that appear is determined by the **Search Results Limit** value which can be updated by opening the Search Application in the [Search Application Configuration](ra-csm-contexts-create.md#entry-search-app-config).

</td></tr></tbody>
</table>4.  Select **Save**.

    After saving the context record, the system displays the Rules and Recommendations related lists.


## What to do next

-   Configure context inputs. For more information, see [Create a context input in Recommended Actions](ra-csm-create-context-inputs.md).
-   Use the Rules related list to view or create rules for this context. For more information on how to create a rule, [Create a rule in Recommended Actions](ra-csm-rules-create.md).
-   Use the Recommendations related list to view the recommendations related to the context rules. You can only create a recommendation from within the rule. For more information on how to create a recommendation within a rule, see [Create a recommendation in Recommended Actions](ra-csm-recommendations-create.md).
-   Use the Search result mapping related list to view or create mappings between AI search outputs and guidance inputs.

**Related topics**  


[Contexts in Recommended Actions](../concept/ra-csm-contexts.md)


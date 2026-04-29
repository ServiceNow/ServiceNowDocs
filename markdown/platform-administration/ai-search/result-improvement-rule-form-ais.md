---
title: AI Search Results Improvement Rule form
description: The AI Search Results Improvement Rule form contains information about result improvement rules defined in your search profiles for AI Search. Use this form when creating or modifying a result improvement rule.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Results Improvement Rule form

The AI Search Results Improvement Rule form contains information about result improvement rules defined in your search profiles for AI Search. Use this form when creating or modifying a result improvement rule.

For details on creating or editing result improvement rules, see [Create a result improvement rule](../task/create-result-improve-rule-ais.md).

<table id="table_y3f_rvd_qmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label for the result improvement rule.

</td></tr><tr><td>

Start Date

</td><td>

System time for the first date when the result improvement rule can activate. If left empty, this field is automatically set to the current date.

</td></tr><tr><td>

End Date

</td><td>

System time for last date when the result improvement rule can activate. After this date, the rule state changes to **Expired**. If left empty, this field is automatically set to 30 days from the **Start Date**.

</td></tr><tr><td>

Activate on all queries

</td><td>

Option to make the result improvement rule activate for every search query.

</td></tr><tr><td>

Language

</td><td>

Language for the result improvement rule. AI Search only evaluates activation for result improvement rules that have the same language as the search query or that have **All Languages** specified for this field.

</td></tr><tr><td>

State

</td><td>

Current state for the result improvement rule.-   **New**: The rule has never been published.
-   **Draft**: The rule is saved with unpublished changes.
-   **Published**: The rule is saved with all changes published.
-   **Expired**: The rule can't activate because its **End Date** is in the past. Publishing a search profile doesn't publish expired rules.

</td></tr><tr><td>

Marked for Deletion

</td><td>

Option indicating whether AI Search will delete the result improvement rule the next time you publish the search profile.

</td></tr><tr><td>

Apply only to Genius Results

</td><td>

Option to make the result improvement rule only operate on Genius Result answers when activated.**Note:** When this option is selected, the result improvement rule can only contain block actions.

</td></tr><tr><td class="sub-head" colspan="2">

Triggers

</td></tr><tr><td>

Expand Synonyms For Query Conditions

</td><td>

Option for enabling synonym expansion for Query condition arguments. This field disappears if you select **Activate on all queries**. When expanding Query conditions, AI Search only considers active synonyms that are defined in the same search profile and that have a language matching the language of the result improvement rule.

</td></tr><tr><td>

Triggers

</td><td>

List of conditions that must be met for the result improvement rule to activate. This field disappears if you select **Activate on all queries**. Select one of the following fields as the subject for your condition:

-   **Keywords**: Operates on one or more keywords found in the user's search query. For example, a **\[Keywords\] \[are\] \[password\]** condition is satisfied by searches for `How do I change my password` or `password reset`.
-   **Query**: Operates on the user's full search query. As an example, a **\[Query\] \[is\] \[password reset\]** condition is satisfied by a search for `password reset`, but not by a search for `password reset steps`.
-   **User Context**: Operates on a user context element from the search user's ServiceNow AI Platform® session. The system displays the source table and field after the user context element name. As an example, a **\[User Context - Country \(sys\_user.country\)\] \[is\] \[Japan\]** condition is satisfied when the search user's User \[sys\_user\] record has **country** set to Japan.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)


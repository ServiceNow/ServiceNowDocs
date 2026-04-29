---
title: Configure navigation actions for NLQ Genius Result answer cards
description: Configure the navigation actions that trigger when a user selects View full table on an NLQ Genius Result action card. Each navigation action includes a redirection payload and can optionally include filters for a table's name, the NLQ source that returned the table, or the search profile used by the search application.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [NLQ Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure navigation actions for NLQ Genius Result answer cards

Configure the navigation actions that trigger when a user selects **View full table** on an NLQ Genius Result action card. Each navigation action includes a redirection payload and can optionally include filters for a table's name, the NLQ source that returned the table, or the search profile used by the search application.

## Before you begin

Role required: ais\_admin

## About this task

When you select **View full table** on an NLQ Genius Result answer card, the action performed depends on how the matching table was found. The default actions are as follows.

-   For a table found by an Analytics Overview table query, the table displays in list view.
-   For a table found by a CMDB table query, the CMDB workspace opens.

As a search administrator, you can customize the actions available for NLQ Genius Result answer cards.

## Procedure

1.  Navigate to the AI Search NLQ Navigation \[ais\_nlq\_navigation\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `ais_nlq_navigation.list`.

    3.  Press Enter.

2.  Edit an existing navigation record or create a new one by selecting **New**.

3.  On the AI Search NLQ Navigation form, fill in the fields for your navigation action.

<table id="table_dcm_vl5_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Optional NLQ source filter for the navigation action. The action only operates for tables that satisfy this source filter. When this field is left empty, the navigation action operates for tables from any NLQ source that isn't specified in another navigation action's **Source** field.

 As an example, suppose you have two navigation actions: one with **Source** set to `CMDB_WS` and a second one with no **Source** field value.

-   When an NLQ Genius Result answer card previews a table returned by the CMDB NLQ source, selecting **View full table** triggers the first navigation action because the table name satisfies the action's NLQ source filter.
-   When an NLQ Genius Result answer card previews a table from the Analytics Overview NLQ source, selecting **View full table** instead triggers the second navigation action because the table's NLQ source doesn't satisfy the first action's NLQ source filter.
 -   Type: string
-   Default value: none.
-   Supported values:
    -   **AC**: The navigation action only operates for tables returned by the Analytics Overview NLQ source.
    -   **CMDB\_WS**: The navigation action only operates for tables returned by the CMDB NLQ source.


</td></tr><tr><td>

Action Payload

</td><td>

JSON payload for the navigation action. This field's value determines where AI Search redirects when you select **View full table** on an NLQ Genius Result answer card. When submitting the JSON payload for redirection, AI Search replaces the following references with relevant values:

-   **$\{logID\}**: Replaced with the NLQ transaction's ID as shown in system logs.
-   **$\{query\}**: Replaced with the query filter from the original search query that triggered the NLQ Genius Result.
-   **$\{table\}**: Replaced with the name of the table previewed on the NLQ Genius Result answer card.
-   **$\{utterance\}**: Replaced with the original search query that triggered the NLQ Genius Result.
 As an example, the default navigation action that opens a table in the CMDB workspace specifies this action payload that makes use of all four references:

```
{ "external": { "url": "now/cmdb/home/sub/smart-search-results/${table}/${utterance}/params/encoded-query/${query}/nlq-query-log/${logID}", "target": "_self" } }
```

 -   Type: JSON
-   Default value: none


</td></tr><tr><td>

Profile

</td><td>

Optional reference to a search profile record. The navigation action only operates in search applications that use the referenced search profile. When this field is left empty, the navigation action operates for any search application that doesn't use a search profile referenced in another navigation action's **Profile** field.

 As an example, suppose you have two navigation actions: one with **Profile** referencing the `Service Portal Default Search Profile` record and a second one with no **Profile** reference field value.

-   When you search in an application that uses the Service Portal Default Service Profile, selecting **View full table** on an NLQ Genius Result answer card triggers the first navigation action because the search profile in use is the one referenced in the action.
-   When you search in any other search application, selecting **View full table** instead triggers the second navigation action because the search profile in use isn't referenced in the first navigation action.
 -   Type: reference
-   Default value: none


</td></tr><tr><td>

Action

</td><td>

Name for the navigation action. -   Type: string
-   Default value: none


</td></tr><tr><td>

Table

</td><td>

Optional table filter for the navigation action. The action only operates for the table whose name matches this filter. When this field is left empty, the navigation action operates for any table that doesn't have its name specified in another navigation action's **Table** field.

 As an example, suppose you have two navigation actions: one with **Table** set to `my_custom_table` and a second one with no **Table** field value.

-   When an NLQ Genius Result answer card previews your custom table, selecting **View full table** triggers the first navigation action because the table name satisfies the action's table filter.
-   When an NLQ Genius Result answer card previews any other table, selecting **View full table** instead triggers the second navigation action because the table name doesn't satisfy the first action's table filter.
 -   Type: table\_name
-   Default value: none


</td></tr></tbody>
</table>4.  Select **Update** if you're editing an existing navigation action record, or **Submit** if you're creating a new one.


**Parent Topic:**[NLQ Genius Results](../concept/genius-result-nlq-ais.md)


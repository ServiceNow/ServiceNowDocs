---
title: Activate fuzzy numeric search in AI Search
description: Activate fuzzy numeric search to let users find indexed records by their Number field values without needing to enter alphabetic prefixes or leading zeroes.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-01-29"
reading_time_minutes: 2
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer]
---

# Activate fuzzy numeric search in AI Search

Activate fuzzy numeric search to let users find indexed records by their Number field values without needing to enter alphabetic prefixes or leading zeroes.

## Before you begin

Role required: admin

## About this task

This task is optional. You only need to perform it if you want to activate the fuzzy numeric search feature in AI Search.

Fuzzy numeric search allows numerical search terms to match indexed ServiceNow AI Platform® records by their Number field values. The fuzzy matching compares the numeric search term with each indexed record's Number, ignoring its alphabetical prefix and any leading zeroes. As an example, if you index knowledge article and problem records, a search for `23583` might return knowledge article KB00023583 and problem PRB00023583 as search results.

When fuzzy numeric search is activated, AI Search checks all-numeric search terms for fuzzy numeric matches when you search and when computing auto-complete suggestions for your search terms. For details on implementing and using auto-complete suggestions, see [Auto-complete suggestions in AI Search applications](../concept/auto-complete-ais.md#).

**Important:**

Fuzzy numeric search only searches records from numbered tables. These are tables with Number fields that have prefixes defined in the Number \[sys\_number\] table. To learn about record numbering and the Number table, see [Record numbering](../../field-administration/concept/c_ManagingRecordNumbering.md).

Child tables that inherit the Number field from their parent table can't be searched using fuzzy numeric search. Only tables that have their own Number field defined work with this feature.

Fuzzy numeric search only finds numeric field values in predefined fields named **number**. It doesn't search custom fields or predefined fields with other names.

To learn more about searching with fuzzy numeric search, see [Fuzzy numeric search in AI Search](../concept/fuzzy-numeric-search.md).

Fuzzy numeric search includes an indexing component which is activated by default and a query-time component which is deactivated by default. Admins can activate the query-time component by changing the value of the **glide.ais.query.enable\_fuzzy\_number\_match** system property.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Search for a system property record with name **glide.ais.query.enable\_fuzzy\_number\_match**.

    -   If a system property record with this name exists, open the record by selecting it.
    -   If no system property record with this name exists, select **New**, then enter `glide.ais.query.enable_fuzzy_number_match` as the new system property's **Name** and select `true | false` as its **Type**.
3.  In the System Property form's **Value** field, enter **true**.

4.  Save the modified System Property record by selecting **Submit** or **Update**.


## Result

Fuzzy numeric search is activated for users in all of your instance's AI Search applications.

**Parent Topic:**[Configuring AI Search](../concept/configuring-ais.md)


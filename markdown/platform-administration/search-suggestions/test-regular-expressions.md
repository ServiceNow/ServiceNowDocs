---
title: Test regular expression patterns in Search Suggestion Exclusion List Rule entries
description: Regular expression patterns are powerful and often require editing to get the correct behavior. When using regular expression patterns to exclude search strings, test the patterns thoroughly so as not to have unintended results.
locale: en-US
release: yokohama
product: Search Suggestions
classification: search-suggestions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Prevent the creation of suggestions in special cases, Configuring Search Suggestions, Search Suggestions, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Test regular expression patterns in Search Suggestion Exclusion List Rule entries

Regular expression patterns are powerful and often require editing to get the correct behavior. When using regular expression patterns to exclude search strings, test the patterns thoroughly so as not to have unintended results.

## Before you begin

Make sure you're familiar with Java's regular expression pattern syntax. To learn about regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

Role required: admin

## About this task

The Exclusion List Rule and Search Suggestion Relations \[m2m\_blacklist\_search\_suggestion\] table lists the suggestions eliminated from the Search Suggestion \[sys\_search\_suggestion\] table by entries in the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table.

## Procedure

1.  In your browser, navigate to `https://<instance name>.service-now.com/m2m_blacklist_search_suggestion_list`.

    A list of words excluded from search suggestions appears in the Exclusion List Rule and Search Suggestion Relations table. The Suggestion column shows the search string that was eliminated in the creation of suggestions.

2.  Add a regular expression pattern to the exclusion list table.

    For more information, see [Preventing suggestions in special cases](preventing-suggestions.md).

3.  In a search field, for example, on the ServiceNow® Service Portal, enter words that satisfy the regular expression pattern.

4.  Run the script that builds the search suggestions.

    For more information, see [Schedule the Build Search Suggestions script](schedule-search-suggestion-builds.md). Select **Execute Now** to run the script immediately.

5.  In the m2m\_blacklist\_search\_suggestion\_list table, select the menu icon ![](../image/hamburger-icon.png) for the Exclusion List column heading, then select **Group By Exclusion List** to see the regular expression patterns and what they eliminated.

6.  Review the suggestions in the table to see if the regular expression patterns removed the suggestions they should have and no more.

7.  In the sys\_search\_suggestion\_blacklist table, set an excluded regular expression pattern's **Active** field to **false**, then run the Build Search Suggestions script again to make sure that only excluded suggestions were removed.

8.  Revise the regular expression patterns if necessary and repeat the procedure.



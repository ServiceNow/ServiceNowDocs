---
title: Prevent the creation of suggestions in special cases
description: Disable generation of suggestions from specific search strings to keep unhelpful terms from appearing in suggestions or to prevent disclosure of personal or secure information.
locale: en-US
release: xanadu
product: Search Suggestions
classification: search-suggestions
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring Search Suggestions, Search Suggestions, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Prevent the creation of suggestions in special cases

Disable generation of suggestions from specific search strings to keep unhelpful terms from appearing in suggestions or to prevent disclosure of personal or secure information.

## Before you begin

Make sure you're familiar with Java's regular expression pattern syntax. To learn about regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html).

Role required: admin

## About this task

Search Suggestions generates auto-complete suggestions and search suggestions from the search strings that users enter. You may not want to create suggestions from all search strings. You can prevent the generation of suggestions using one of the following approaches:

-   Exclude words or regular expression patterns from auto-complete suggestions and search suggestions.

    For example, a user might search on `KB2938272`. This search string is too opaque to provide a meaningful suggestion. Or, someone might enter a social security number or phone number as search strings which shouldn't be surfaced as suggestions to anyone else. So, you might exclude all search strings that contain multiple numbers. Likewise, if someone uses an expletive in a search string, you may not want to surface that word in suggestions. The Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table contains the list of excluded words and regular expression patterns.

    **Note:** In the base system, the Search Suggestion Exclusion List table contains excluded words for English and language-independent regular expression patterns. Search Suggestions inserts additional language-specific excluded words into this table when you activate any of the following languages: Chinese, Czech, Dutch, Finnish, French, German, Hebrew, Hungarian, Italian, Japanese, Norwegian, Polish, Portuguese, Russian, Spanish, Swedish, Thai, or Turkish.

-   Assign roles to users that prevent the generation of suggestions from their search strings.

    There may be individuals whose searches shouldn't appear in search or auto-complete suggestions for privacy or security reasons. To prevent their searches from generating suggestions, assign them the suggestion\_exempt role. This role is unnecessary in most situations. Search Suggestions never shows who performed the initial search. To prevent people from seeing auto-complete suggestions and search suggestions, assign them the cannot\_read\_suggestions role.


## Procedure

1.  Navigate to the Search Suggestion Exclusion List \[sys\_search\_suggestion\_blacklist\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_search_suggestion_blacklist.list`.

    3.  Press Enter.

2.  To make a word or regular expression pattern active or inactive:

    1.  Select the term in the list that you want to activate or deactivate.

    2.  In the Search Suggestion Exclusion List form that appears, select or clear the **Active** option.

3.  To add a new excluded word or regular expression pattern:

    1.  Select **New**.

    2.  On the Search Suggestion Exclusion List form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Phrase|Word or regular expression pattern to exclude.|
        |Language|The language that the excluded word is in. Use the ISO 639-1 code for the language, such as "en" for English. Because regular expression patterns work for all languages, search suggestions ignores this field for regular expression patterns.|
        |Description|Explanation of why you excluded the word or regular expression pattern if it's not obvious. This field is especially important for regular expression patterns.|
        |Active|Option to remove the excluded word or regular expression pattern from suggestions.|
        |Type|Option that specifies whether the **Phrase** field represents one word or a regular expression pattern.|

        **Note:** If you use regular expression patterns, you should verify that they exclude the words you want. For more information, see [Test regular expression patterns in Search Suggestion Exclusion List Rule entries](test-regular-expressions.md).

4.  To assign someone a role that prevents them from seeing auto-complete suggestions and search suggestions, or to prevent their search strings from becoming suggestions:

    1.  Navigate to **All** &gt; **User Administration** &gt; **Users** and select the name of a user.

    2.  In the Roles related list, select **Edit**.

    3.  To prevent a user from seeing auto-complete suggestions and search suggestions, move **cannot\_read\_suggestions** from the Collections column to the Roles List column and select **Save**.

    4.  To prevent a user's search strings from generating auto-complete suggestions and search suggestions, move **suggestion\_exempt** from the Collections column to the Roles List column and select **Save**.



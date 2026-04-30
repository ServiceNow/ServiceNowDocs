---
title: Define a query filter for Now Assist Q&amp;A Genius Results
description: Define a Java regular expression pattern that a search must match to be eligible for triggering Now Assist Q&amp;A Genius Results. Searches that don't match this pattern don't return Genius Result answers from Now Assist Q&amp;A Genius Results.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist Q&amp;A Genius Results, Configuring Now Assist in AI Search, Now Assist in AI Search, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Define a query filter for Now Assist Q&amp;A Genius Results

Define a Java regular expression pattern that a search must match to be eligible for triggering Now Assist Q&amp;A Genius Results. Searches that don't match this pattern don't return Genius Result answers from Now Assist Q&amp;A Genius Results.

## Before you begin

The Now Assist in AI Search ServiceNow® Store application must be installed on your instance. For details on installing this application, see [Install Now Assist in AI Search](install-now-assist-ais.md).

Make sure that you're familiar with Java's regular expression pattern syntax. To learn about the regular expression pattern syntax, see [the Javadoc for the java.regex.util.Pattern class](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/regex/Pattern.html).

Role required: admin

## About this task

Now Assist Q&amp;A Genius Results send eligible knowledge article search results to the Now LLM Service for Q&amp;A Genius Result answer generation.

By default, the system only sends knowledge article results to the Now LLM Service when the search satisfies all of these conditions.

-   The search application is Service Portal, Virtual Agent, Employee Center, or global search.
-   The user's session language is English.
-   The search contains two or more terms.
-   The search matches the Java regular expression pattern defined by the **sn\_ais\_assist.u\_question\_regex** system property's value. This system property has no value set in the base system, so by default all search queries satisfy this condition.

You can customize the pattern match condition by defining your own Java regular expression pattern for use by Now Assist Q&amp;A Genius Result configurations.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Open the record for the **sn\_ais\_assist.u\_question\_regex** system property by selecting it from the list.

    If the system prompts you to change the application scope so that you can edit the record, select the provided link.

3.  In the system property's **Value** field, enter a Java regular expression pattern that you want Q&amp;A search queries to match.

    The Java regular expression match is case-insensitive. As an example, to restrict Q&amp;A answer expansion to search queries that start with a question keyword, you can set the property's value to `^(what|where|when|why|who|whom|which|how)\b`.

4.  Select **Update**.


## Result

Now Assist Q&amp;A Genius Results don't send knowledge article search results to the Now LLM Service for Q&amp;A answer generation unless the search query matches your Java regular expression pattern.

**Parent Topic:**[Now Assist Q&amp;A Genius Results](../concept/now-assist-qna-genius-results.md)


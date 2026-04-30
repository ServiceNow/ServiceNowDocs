---
title: Configure click-rank search relevance
description: Enhance the topic page search rank based on the clicks and usage of a topic by the employees.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [AI Search for Curated Experiences, Setup search experience, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure click-rank search relevance

Enhance the topic page search rank based on the clicks and usage of a topic by the employees.

## Before you begin

Role required: Admin

**Important:** The click-rank population of search results is available for the Xanadu family release and beyond. For Washington, the behavior doesn't work due to a limitation.

Ensure you understand the AI search and search suggestions.

## About this task

When employees search for topic pages, such interactions influence and improve future search rankings and the content discovery for the organizations. Determine click rank population for search results from the clicks and usage of the topic among employees.

## Procedure

1.  Understand the basics of search events and suggestions from [Analyze search relevancy](https://www.servicenow.com/docs/access?context=improve-search-results&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

2.  Navigate to **All** &gt; **Search Suggestions** &gt; **Search Events**.

3.  Review **Click rank** for search query and other details.

    Click rank shows which search result you selected.

    -   If you click the first result in the list of search results, the click rank value is 1. If you click the 6th result listed, the click rank value is 6.
    -   If you click multiple search results, the click rank is the highest listing value. For example, if you click the first result, return to the search page and click the 6th result, return to the search page and click the 4th result and find an answer, the click rank is 6 \(not 4\).
    A click rank of 0 means that you don't select any search result, or that you selected a result answer card in AI Search. Lower positive click rank values indicate that the top search results are the most relevant, so the goal is to reduce the average value for this field.


## Result

Based on this configuration, your employees can easily find the relevant content based on click rank and portal-specific search results.


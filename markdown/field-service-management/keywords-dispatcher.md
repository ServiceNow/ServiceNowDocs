---
title: Configure keyword searching in Dispatcher Workspace
description: Use specific keyword formatting, powered by ServiceNow Zing, to quickly locate tasks and resources in Dispatcher Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/keywords-dispatcher.html
release: australia
product: Field Service Management
classification: field-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dispatcher Workspace, CSM/FSM Configurable Workspace, Configure, Field Service Management]
---

# Configure keyword searching in Dispatcher Workspace

Use specific keyword formatting, powered by ServiceNow® Zing, to quickly locate tasks and resources in Dispatcher Workspace.

## How Zing search works

Dispatcher Workspace uses ServiceNow® Zing, ServiceNow®'s text indexing and search engine, to deliver fast results ranked by relevance. Zing search engine logic yields fast results and emphasizes relevancy scoring. Relevancy scores include frequency and proximity weighting. Scores also include weighting for specific indexed fields such as title, short description, and metadata. For more information on Zing, see .

## Indexing scope and prerequisites

Before relying on keyword search, review how your instance indexes tables, attributes, and values and confirm that the required tables are included. For more information, see .

Some fields are excluded from text indexing. For more information see the “Fields excluded from text indexing” table in .

If you use Territory planning then navigate to **All** &gt; **System Definitions** &gt; **Text index** and verify that you see the following tables:

-   `sn_tp_territory`
-   `sn_tp_territory_membership_override`

If you're using Territory planning and don't see the tables listed above, then complete Step 5e in .

## Language and punctuation considerations

Zing indexes words based on the language of your content. Review the rules for how Zing indexes words in .

Zing indexes some punctuation marks as part of some words to improve search results for common search terms. For more information, see .

## Supported keyword features in Dispatcher Workspace

Zing keywords in Dispatcher Workspace supports the following:

-   Boolean operators, like AND and OR, but they must be used in capital letters. There are more Boolean operators used as well, for more information, see .
-   Exact phrase searches denoted by quotation marks. For more information, see .
-   Single-character and multiple-character wildcards, denoted by characters like %. For more information, see .

The table below shows what tables Zing searches when you use keywords based on the setting or configuration you have.

|Table name|Only Dispatcher Workspace|Territories enabled|Crew plugin active|Equipment plugin active|Contractor plugin active|
|----------|-------------------------|-------------------|------------------|-----------------------|------------------------|
|sys\_user|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|
|sys\_user\_group|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|\[Omitted image "circle-check-fill-24.svg"\] Alt text:|
|sn\_tp\_territory| |\[Omitted image "circle-check-fill-24.svg"\] Alt text:| | | |
|sn\_tp\_territory\_membership| |\[Omitted image "circle-check-fill-24.svg"\] Alt text:| | | |
|sn\_fsm\_resource| | | |\[Omitted image "circle-check-fill-24.svg"\] Alt text:| |
|wm\_crew| | |\[Omitted image "circle-check-fill-24.svg"\] Alt text:| | |

For examples on how to use Zing keywords in Dispatcher Workspace, see [Searching in Dispatcher Workspace examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/field-service-scheduling/search-keyword-example.md).


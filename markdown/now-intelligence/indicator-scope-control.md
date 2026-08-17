---
title: Indicator scope control
description: Indicator Scope Control provides an admin-curated list that boosts selected Performance Analytics indicators in ambient AI search results, with optional custom descriptions to improve search accuracy. Create a Query Generation indicator configuration record to add a Performance Analytics indicator to the scope control boost list. The boost list can improve search rankings for high-quality indicators.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/indicator-scope-control.html
release: zurich
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 6
keywords: [Indicator Scope Control, Performance Analytics, AI search, ambient search, indicator boost, Query Generation, configure, Indicator Scope Control, Performance Analytics, boost, configuration]
breadcrumb: [Configure, Query Generation, ServiceNow Otto for Platform Analytics, Platform Analytics]
---

# Indicator scope control

Indicator Scope Control provides an admin-curated list that boosts selected Performance Analytics indicators in ambient AI search results, with optional custom descriptions to improve search accuracy.

If you use Performance Analytics and have a large indicator estate, you often accumulate low-quality indicators. These indicators can pollute ambient AI search results and reduce answer accuracy. Indicator scope control closes this quality gap. It provides you with the means to curate a list of high-quality indicators that receive a relevance boost in ambient AI searches.

The boost is additive, not restrictive: An empty list, a inactive feature toggle, or a scale factor of 1.0 does not prevent ambient AI search from functioning. The curation mechanism is similar to the Manual Segments feature, providing Query Generation administrators with an optional control for improving search quality without affecting existing functionality.

## Key benefits

-   **Improved search accuracy**

    Boost relevant indicators to rank higher, reducing the number of low-quality indicators in results.

-   **Optional and additive**

    Curation is optional. An empty or inactive list leaves search behavior unchanged.

-   **Admin-controlled quality**

    Administrators decide which indicators are trustworthy, eliminating low-quality data without deletion.

-   **Custom descriptions**

    Add optional descriptions to boost indicators, surfacing them via custom text that doesn't exist in the Performance Analytics indicator itself.

-   **Runtime tuning**

    Adjust the boost scale factor at runtime without a deployment, based on user feedback.


## How it works

Indicator Scope Control operates as follows:

1.  An administrator creates a row in the indicator scope configuration table, referencing a valid Performance Analytics indicator.
2.  Each configuration row can include an optional custom Description. When present, the description is indexed and matched during AI search along with the Performance Analytics indicator's own name, description, and breakdowns.
3.  At search time, if Indicator Scope Control is enabled and active configurations exist, the system runs two simultaneous searches. One search is against the full Performance Analytics indicator pool. The second search is against the curated Indicator Configuration table.
4.  Results from both searches are merged by indicator. Indicators present in the curated list receive a relevance boost \(multiplying their semantic similarity score by a configurable scale factor, default 1.05\).

    **Note:** To change the boost factor, create the system property **sn\_query\_gen.indicator.boost.scale\_factor** on the System Properties table and give it the value you want. To disable boosting, set the value to 1.0.

5.  Boosted indicators already present in the main Performance Analytics results rank higher. Boosted indicators absent from Performance Analytics results are added to the merged results.
6.  If the boost list is empty, inactive, or the scale factor is 1.0, the system only runs the search against the full Performance Analytics indicator pool.

Indicator Scope Control has no impact when it is not used:

-   When the feature property is off, behavior is byte-for-byte identical to the single-search path.
-   When the indicator scope configuration table is empty \(no active rows\), the single-search path is used without any overhead.
-   When the boost scale factor is `1.0`, scores pass through unchanged and the merge only removes duplicate results.

**Note:** Query Generation supports two independent boosts to indicators in results:

-   This admin-curated relevance boost. This boost multiplies `semanticSimilarity`, the numeric index of how well an indicator matches a query, by a preset number. This number is 1.05 by default, and can be changed by creating the **sn\_query\_gen.indicator.boost.scale\_factor** system property.
-   Previous-indicator injection. If previous replies in the exploration contain an indicator, `semanticSimilarity` for that indicator is set to 1. Doing so insures that the indicator survives the 12-indicator cap on what is sent to the LLM.

## Use cases

-   **Curate high-quality indicators**

    Organizations with large Performance Analytics estates can surface only their validated, well-maintained indicators, improving AI search results for all users.

-   **Surface indicators with custom context**

    Add a custom description to an indicator that is poorly described in Performance Analytics itself. AI search can then match user queries against your custom text.

-   **Gradual rollout**

    Start with an empty list or inactive feature toggle; enable and populate gradually as your team validates which indicators are trustworthy.

-   **Gradual indicator retirement**

    Instead of deleting low-quality indicators immediately, toggle them off from the boost list to reduce their prominence in search results while preserving the Performance Analytics records themselves.


## Considerations

-   **Misconfiguration is safe**

    A broken indicator reference, an empty configuration table, or a inactive boost list all fall back gracefully to the single-search behavior with no error surfaced to users.

-   **Duplicate indicators aren't allowed**

    The system prevents a second configuration row for an indicator that already has one. You can edit the existing row instead.

-   **Runtime control**

    Both the boost scale factor and the feature toggle are read from system properties, enabling runtime tuning without a deployment. Setting the scale factor to 1.0 does not trigger additional operations.

-   **Entry-point indicators unaffected**

    Indicators that are both on the boost list and passed as entry-point context \(via dashboard widgets or API\) are boosted and then pinned to the top with no conflict.


**Parent Topic:**[Configuring Query Generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/now-intelligence/configuring-query-generation.md)

**Related topics**  


[bundle-platadm.t_AddAPropertyUsingSysPropsList]

## Set up indicator scope control

Create a Query Generation indicator configuration record to add a Performance Analytics indicator to the scope control boost list. The boost list can improve search rankings for high-quality indicators.

### Before you begin

Role required: sn\_query\_gen.admin or higher

### About this task

Use this procedure to add a Performance Analytics indicator to the indicator scope control boost list. The boost list allows you to improve search ranking for high-quality indicators. You can create multiple configuration rows to boost different indicators.

### Procedure

1.  Navigate to **All** &gt; **Query Generation** &gt; **Administration** &gt; **Semantic Indicator Config**.

2.  Select the **New** button.

3.  Complete the following fields on the indicator configuration form:

    |Field|Description|
    |-----|-----------|
    |Indicator|Reference a valid PA indicator record. This field is required. The system prevents duplicate indicator records on this table.|
    |Active|Toggle this indicator on or off without deleting the configuration row. Default: on \(true\). Set to off \(false\) to exclude the indicator from the boost list while preserving the configuration for later reactivation.|
    |Description|Optional. Enter a custom admin-authored description \(up to 4000 characters\). When present, this description is indexed and matched during AI search along with the indicator's name, description, and breakdowns. Use this field to surface poorly described indicators or add context that doesn't exist in the indicator record itself. Leave empty if the indicator's existing description is sufficient.|

4.  Select **Submit** to create the table record.


### Result

The system saves the form successfully as a new record on the Indicator Configurations \[sn\_query\_gen\_indicator\_config\] table. The record inherits the domain from the referenced Indicator \[pa\_indicators\] record. The chosen indicator is immediately added to the boost list. It receives a relevance boost in ambient AI search results \(at the default scale factor of 1.05\). If you provided a custom description, it is indexed and available for search matching immediately.

### What to do next

To edit an existing configuration row, open the same row \(same sys\_id\) and make your changes. The system allows editing of existing rows. To add a different indicator, create a configuration row. You cannot register the same indicator twice.

To change the boost factor, create the system property `sn_query_gen.indicator.boost.scale_factor` on the System Properties table and give it the value you want. To disable boosting, set the value to 1.


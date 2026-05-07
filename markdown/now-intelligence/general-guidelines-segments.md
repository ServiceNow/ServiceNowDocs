---
title: Guidelines for segments
description: Follow these suggestions to help you use segments in the semantic layer effectively.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 4
breadcrumb: [Segments, Tuning the semantic layer, Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Guidelines for segments

Follow these suggestions to help you use segments in the semantic layer effectively.

## General guidelines for segments

-   Test segments by asking natural language questions that should match them. The segment should appear in **Query Generation** &gt; **Logs**.
-   Monitor query logs to verify segments are being matched correctly and to identify the most valuable segments.
-   Disable noisy auto-generated segments rather than trying to overfit with multiple manual ones.
-   Use natural phrasing that matches how your users actually speak.
-   Keep one segment per concept to avoid confusion.
-   Refine segment names and descriptions based on user feedback and usage patterns
-   Consider creating manual segments for recurring questions that are not handled well by the existing segments.

## Guidelines for manual segments

Manual segments are the recommended way to ship domain-specific saved searches with your application. They receive a priority boost over automated segments during search, and the LLM is instructed to retain all their filters unless completely irrelevant.

-   **Start with high-value, high-traffic tables**

    Focus manual segments on the tables your users ask about most. A handful of well-crafted segments on incident, sc\_req\_item, or your application's primary table will have more impact than broad coverage across rarely-queried tables.

-   **Pair every choice-heavy filter with a clear name**

    If your segment filters on choice values—for example, `state=6^priority<=2`—the segment name must translate those codes into business language. The LLM matches on the name, not the filter. "Resolved Critical and High Incidents" is searchable, but `state=6^priority<=2` is not.

-   **Use descriptions to disambiguate similar segments**

    If you ship multiple segments for the same table—for example, "Open Incidents" and "Open Critical Incidents"—descriptions are what help the LLM pick the right one. Without descriptions, the LLM may arbitrarily choose between two close matches.

-   **Keep filters focused**

    A segment with 15 filter conditions is hard for the LLM to reason about and likely to be truncated. If you have a complex use case, split it into multiple segments with simpler filters. The LLM can combine filters from different segments when constructing a query.

-   **Complement semantic descriptions with segments**

    Manual segments and semantic descriptions \(entity/column config\) work together. Descriptions help the LLM understand *what* a table and its columns represent. Segments help the LLM understand *how users typically filter* that table. For best results, ship both.

-   **Avoid duplicating automated segments**

    Before creating a manual segment, check whether an automated segment already covers the same filter. If one does but has a poor name, consider whether improving the source—for example, renaming the report—is a better approach than creating a duplicate manual segment.

-   **Review after deployment**

    After shipping, monitor which segments are being matched and whether the generated queries are correct. If a segment is matching but producing wrong results, the issue is usually the name being too generic or the filter being too broad. Iterate on the name and description first before adjusting system properties.


## Property tuning suggestions

Use these suggestions to adjust system properties when segments are not performing as expected. For a complete list of all segment properties and their defaults, see [Query Generation properties](querygen-properties.md).

-   **Segments are not matching user questions**

    Lower **segments\_match\_threshold** \(For example, set it to `0.60`\). The default `0.70` can be too strict for domain-specific terminology where the user's phrasing differs from the segment name. Start lower and tighten once you have enough segments.

-   **Manual segments are being overshadowed by automated ones**

    Increasing **manual\_segment\_scale\_factor** gives manual segments a stronger edge, but a higher boost does not necessarily mean better results. A poorly named manual segment boosted above a genuinely relevant automated segment will degrade query quality. Before adjusting the boost, first check whether the manual segment's name and description are well-written. That is usually the real fix. Only increase the factor if you're confident your manual segments are high quality and still losing to weaker automated matches.

-   **Too many irrelevant segments in the LLM prompt**

    Lower **segments\_result\_limit** \(for example, `6` or `8`\). Fewer segments in the prompt means less noise for the LLM, but also less coverage. Find the balance for your domain. Alternatively, raise **segments\_match\_threshold** if you're seeing low-quality matches slip through.

-   **Long filters getting truncated**

    Increase **max\_filter\_length** if your segments require complex filters. Be aware that longer filters consume more of the LLM's context window and may reduce overall generation quality. Consider splitting a complex segment into multiple focused segments instead.

-   **Batch search is disabled and manual segments are not surfacing**

    Enable the AI Search property **segments.ais\_batch\_fetch\_enabled**. Without batch search, manual and automated segments compete for the same result slots. Batch search gives each type a dedicated search, significantly improving manual segment coverage.


**Parent Topic:**[Segments in the Query Generation semantic layer](querygen-segments.md)

**Related topics**  


[Create a manual segment](../task/querygen-create-segment-manually.md)

[Manual segment data model and sync behavior](manual-segment-data-model-sync.md)

[Shipping manual segments via plugins](shipping-manual-segments-plugins.md)

[manual-segment-system-properties]


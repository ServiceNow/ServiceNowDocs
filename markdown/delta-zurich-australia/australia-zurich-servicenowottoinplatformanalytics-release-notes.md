---
title: Combined ServiceNow Otto in Platform Analytics release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for ServiceNow Otto in Platform Analytics from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-servicenowottoinplatformanalytics-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined ServiceNow Otto in Platform Analytics release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for ServiceNow Otto in Platform Analytics from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ServiceNow Otto in Platform Analytics release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ServiceNow Otto in Platform Analytics to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ServiceNow Otto in Platform Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ServiceNow Otto in Platform Analytics features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   **[Promote selected indicators in AI Search results](https://www.servicenow.com/docs/access?context=indicator-scope-control&family=australia&ft:locale=en-US)**

Add high-quality indicators that you identify to a list. The indicators on that list are given a boost in AI Search results for Query Generation.

-   **[View more indicator insights in Extended analysis](https://www.servicenow.com/docs/access?context=hidden-insights&family=australia&ft:locale=en-US)**

See directional trends over time and indicator target information in Extended analysis summaries.

-   **[Improvements to data visualizations in Query Generation responses](https://www.servicenow.com/docs/access?context=ask-expl-questions&family=australia&ft:locale=en-US)**
    -   Single-score charts now render sparklines by default.
    -   When a user query on indicator data does not specify a visualization type, the response returns the indicator's default chart type.
-   **[Now Assist renamed to ServiceNow Otto®](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&family=australia&ft:locale=en-US)**

The Now Assist Admin Console is now AI Admin Hub and many other changes have been made. This renaming is a work in progress.


-   **[Query indicator data](https://www.servicenow.com/docs/access?context=ai-data-explorer-implementation-checklist&family=australia&ft:locale=en-US)**

Get scores from automated indicators in your AI Data Explorer explorations. Only classic automated indicators, not Data snapshots, are supported.


-   **[Explorations not available from visualization or list for unsupported scope](https://www.servicenow.com/docs/access?context=launch-now-assist-explorer&family=australia&ft:locale=en-US)**

You can't open AI Data Explorer from a data visualization or list that shows data from a protected scope that is not supported.

-   **[Improvements to generated segments](https://www.servicenow.com/docs/access?context=querygen-segments&family=australia&ft:locale=en-US)**
    -   The names of automatically generated segments now include both the module name and the name of the application it belongs to.
    -   Improved logic to join conditions for segments generated from reports and report sources. More complex conditions such as global OR are now supported.

-   **[Explore data from protected scopes](https://www.servicenow.com/docs/access?context=enable-aide-secure-scope-apps&family=australia&ft:locale=en-US)**

Provide access to protected application scopes to AI Data Explorer and Query Generation, and you can use data from those application tables in explorations. \(Query Generation bundle 5.2\)

-   **[Improvements to how segments are handled](https://www.servicenow.com/docs/access?context=querygen-segments&family=australia&ft:locale=en-US)**

    -   Manual segments are re-ranked to take priority over automatically generated segments.
    -   Prompt changes made to better support manual segments.
    -   More segments are passed to the LLM to increase the chance of the correct segment getting selected. Twelve segments are passed instead of three.
    -   Segments longer than 2000 characters are dropped to prevent context window bloat.
\(Query Generation bundle 5.2\)

-   **[Query Generation support for Glide Lists](https://www.servicenow.com/docs/access?context=querygen-unsupported-field-types&family=australia&ft:locale=en-US)**

Query Generation now supports Glide List fields on tables.


-   **[Customize semantic metadata in configuration tables](https://www.servicenow.com/docs/access?context=customize-semantic-metadata&family=australia&ft:locale=en-US)**

Customize semantic descriptions and usage instructions in the table and column configuration tables. Unlike the previous method of editing Entity and Dimension records, these changes can be transferred between instances through update sets.

-   **[View recommended actions](https://www.servicenow.com/docs/access?context=expl-view-recommended-actions&family=australia&ft:locale=en-US)**

AI Data Explorer can suggest actions based on the insights that it generates in an exploration.

-   **[Ask questions about FX currency data](https://www.servicenow.com/docs/access?context=qg-supported-query-operations&family=australia&ft:locale=en-US)**

Query Generation now supports the FXCurrency \(Currency 2\) data type. This means that you can use AI Data Explorer to explore financial operations data, including those within Source-to-Pay Operations.

-   **[Benefit from improvements to segments](https://www.servicenow.com/docs/access?context=querygen-segments&family=australia&ft:locale=en-US)**

Segments are reusable definitions in Query Generation that provide non-obvious context to assist the semantic layer or LLM to select the correct dimension and values. Users can create manual segments via a new form. A scheduled job synchronizes manual and autogenerated segments. This job also cleans up segments to help surface the correct segments and reduce noise.

Manual segments are re-ranked to take priority over automatically generated segments.

Domain separation is also now supported, with a Domain field on the Segments table. Segments based on reports and filters inherit the source domain. Manual segments have domains that are passed up to the Segments table on synchronization. Segments aren't supported for modules on domain-separated instances.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ServiceNow Otto in Platform Analytics features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ServiceNow Otto in Platform Analytics features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ServiceNow Otto in Platform Analytics.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

Now Assist applications for Platform Analytics are either included by default or you can install them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ServiceNow Otto in Platform Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ServiceNow Otto in Platform Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ServiceNow Otto in Platform Analytics, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

-   \(June 2026 AI Data Explorer\) Keyboard navigation allows tabbing between the text editor and the icons.
-   \(June 2026 AI Data Explorer\) Users can use move up/move down control menu items to change the order of question/response nodes in the exploration. Previously they could only drag the nodes.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ServiceNow Otto in Platform Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ServiceNow Otto in Platform Analytics we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

The following highlights are specific to AI Data Explorer, which relies on Query Generation in the back end.

-   AI-Generated Insights: Ask questions in natural language and see them turned into documented insights and visualizations. AI guides your analysis and suggests follow-up questions to deepen your exploration. Switch between two powerful modes, Standard analysis and Extended analysis, to uncover hidden insights.
-   Integration with External Data: Extend supported data sources and enable seamless integration with external systems through Data Fabric tables to gain more complete insights across the company’s diverse data.
-   Document Editing and Organization: Shape your data story exactly as you need it. Collect, edit, and organize insights directly within your exploration.
-   Collaboration with Other Users: Transform data analysis by working simultaneously with colleagues in a shared space to refine analyses, align on insights, and accelerate data-driven decisions.
-   Smart Integration with Contextual Intelligence: Trigger AI Data Explorer instantly from any application, list, or data visualization. Doing so accesses powerful insights enhanced by contextual awareness and usage patterns to highlight the data that matter most to you.

 See [ServiceNow Otto for Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)


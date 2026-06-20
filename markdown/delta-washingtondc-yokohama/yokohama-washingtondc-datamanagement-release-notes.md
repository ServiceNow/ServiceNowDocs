---
title: Combined Data Management release notes for upgrades from Washington DC to Yokohama
description: Consolidated page of all release notes for Data Management from Washington DC to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-washingtondc-yokohama/yokohama-washingtondc-datamanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-20"
reading_time_minutes: 4
breadcrumb: [Products combined by family]
---

# Combined Data Management release notes for upgrades from Washington DC to Yokohama

Consolidated page of all release notes for Data Management from Washington DC to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Washington DC to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

A data management policy record is automatically created for each table that is configured with an archive rule or a table cleaner rule prior to the upgrade.

</td></tr><tr><td>

Yokohama

</td><td>

-   After upgrading a self-hosted instance to Yokohama, the sys\_physical\_table\_stats table doesn't display the latest data for table size, with the sample\_period\_start column showing dates prior to the upgrade. To see the correct table size, you can set the com.glide.stats.storage\_disk\_usage.information\_schema system property to true, which allows the statsGatherer job to use the information schema to generate the required database statistics.

-   A data management policy record is automatically created for each table that is configured with an archive rule or a table cleaner rule prior to the upgrade.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Data Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   **[Data Management policies](https://www.servicenow.com/docs/access?context=data-management-policies&family=xanadu&ft:locale=en-US)**

Access a holistic view of the data management rules that you configured for a table.

-   **[Support for multiple archive rules on one table](https://www.servicenow.com/docs/access?context=c_ArchiveData&family=xanadu&ft:locale=en-US)**

Create multiple archive rules for a single table using a data management policy.

-   **[Table cleaner performance improvements](https://www.servicenow.com/docs/access?context=table-cleaner&family=xanadu&ft:locale=en-US)**

Automatically delete older records more efficiently using the table cleaner.

-   **[Data Management usage dashboard](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=xanadu&ft:locale=en-US)**

View a summary of storage consumption on your instance and monitor the top 10 tables consuming the most data on your instance.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=yokohama&ft:locale=en-US)**

View a summary of storage consumption on your instance and manage the growth of data directly from the Data Management Console.

-   **[Table cleaner scalability improvements](https://www.servicenow.com/docs/access?context=deleting-older-records&family=yokohama&ft:locale=en-US)**

Automatically delete older or unwanted records at scale.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Data Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=yokohama&ft:locale=en-US)**

You can now access data usage on your instance by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console**.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Data Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Data Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Data Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

Data Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Yokohama

</td><td>

Data Management is a ServiceNow AI Platform feature that is active by default.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Data Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Data Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Data Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Data Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Washington DC

</td><td>

No updates for this release.

</td></tr><tr><td>

Xanadu

</td><td>

-   Define and access all the data management rules for a table from the data management policy page.
-   Create multiple archive rules for a table.
-   Access and configure the destroy rules for deleting archived records from the data management policy page.
-   Delete older records at scale with improved performance using the table cleaner.
-   View a summary of storage consumption on your instance.

 See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   View insights into storage consumption on your instance and implement data management policies directly from the Data Management Console.
-   Automatically delete older or unwanted records with improved table cleaner scalability.

 See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-washingtondc-yokohama/rn-combined-intro.md)


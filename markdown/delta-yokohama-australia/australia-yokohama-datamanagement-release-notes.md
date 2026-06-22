---
title: Combined Data Management release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Data Management from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-datamanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Data Management release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Data Management from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Data Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Data Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   After upgrading a self-hosted instance to Yokohama, the sys\_physical\_table\_stats table doesn't display the latest data for table size, with the sample\_period\_start column showing dates prior to the upgrade. To see the correct table size, you can set the com.glide.stats.storage\_disk\_usage.information\_schema system property to true, which allows the statsGatherer job to use the information schema to generate the required database statistics.

-   A data management policy record is automatically created for each table that is configured with an archive rule or a table cleaner rule prior to the upgrade.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Data Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=yokohama&ft:locale=en-US)**

View a summary of storage consumption on your instance and manage the growth of data directly from the Data Management Console.

-   **[Table cleaner scalability improvements](https://www.servicenow.com/docs/access?context=deleting-older-records&family=yokohama&ft:locale=en-US)**

Automatically delete older or unwanted records at scale.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=zurich&ft:locale=en-US)**

View a summary of data usage on your instance and manage the growth of data directly from the Data Management Console.

-   **[Monitor data usage at the table level](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=zurich&ft:locale=en-US)**

View a summary of data usage for an individual table and monitor data usage in associated tables that store attachments, audit records, and journal entries.

-   **[View data usage for logical tables](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=zurich&ft:locale=en-US)**

Monitor data usage for logical tables, including the Incident \[incident\], Problem \[problem\], and Change Request \[change\_request\] tables.

-   **[Identify which tables are driving the most growth in other tables](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=zurich&ft:locale=en-US)**

View tables contributing the most growth to the tables that store attachments, audit records, and journal entries.

-   **[Rule summary](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=zurich&ft:locale=en-US)**

Track the number of records in the backlog and view the execution history of a table's data management rules.


</td></tr><tr><td>

Australia

</td><td>

-   **[Archive data in object storage](https://www.servicenow.com/docs/access?context=c_ArchiveData&family=australia&ft:locale=en-US)**

Store archive records and attachments in columnar format in an object storage outside the primary instance, freeing up primary storage and improving query performance for active data. The object storage is exclusive to RaptorDB Professional V2.

-   **[Data Management rules wizard](https://www.servicenow.com/docs/access?context=data-management-policies&family=australia&ft:locale=en-US)**

Create and manage your archive, cleanup, and one-time delete rules in the Data Management Console.

-   **[Restore archive records in bulk](https://www.servicenow.com/docs/access?context=t_RestoreArchivedData&family=australia&ft:locale=en-US)**

Search for archived records and restore them in bulk to live tables from the Data Management Console.

-   **[Granular admin role](https://www.servicenow.com/docs/access?context=data-management-role-1&family=australia&ft:locale=en-US)**

Enable administrators to perform basic Data Management tasks by granting the data\_mgmt\_tools\_admin role instead of the full admin role.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Data Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Data Management Console](https://www.servicenow.com/docs/access?context=viewing-data-usage&family=yokohama&ft:locale=en-US)**

You can now access data usage on your instance by navigating to **All** &gt; **System Data Management** &gt; **Data Management Console**.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Data Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Data Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The Data Usage Visualization Console dashboard has been deprecated in the Zurich release. Instead, you can monitor the growth of data on your instance using the Data Management Console.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

Data Management is a ServiceNow AI Platform feature that is active by default.

</td></tr><tr><td>

Zurich

</td><td>

Data Management is a ServiceNow AI Platform capability that is active by default.

</td></tr><tr><td>

Australia

</td><td>

Data Management and system archiving are ServiceNow AI Platform capabilities that are active by default.

 The ability to store archive data in object storage is available with the installation of Live Archive, which requires a separate subscription. For details, see [\[Placeholder link text to key install-data-archiving-plugin\]](https://www.servicenow.com/docs/access?context=install-data-archiving-plugin&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Data Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Yokohama

</td><td>

-   View insights into storage consumption on your instance and implement data management policies directly from the Data Management Console.
-   Automatically delete older or unwanted records with improved table cleaner scalability.

 See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   View insights into storage consumption on your instance and manage data usage in the redesigned Data Management Console.
-   Monitor data usage in a logical table view.
-   View data usage for individual tables and their associated tables.
-   View a summary of the data management rules on a table.

 See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Store archive records and attachments in an object storage outside the primary instance.
-   Create and manage Data Management rules directly from the Data Management Console.
-   Search for archived records and restore them in bulk.
-   Enable users to complete administrative tasks in Data Management without the full admin role.

 See [Data Management](https://www.servicenow.com/docs/access?context=c_DataManagement&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


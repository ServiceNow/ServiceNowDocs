---
title: Combined Instance Data Replication release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Instance Data Replication from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-instancedatareplication-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 5
breadcrumb: [Products combined by family]
---

# Combined Instance Data Replication release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Instance Data Replication from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Instance Data Replication release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Instance Data Replication to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy sets](https://www.servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&family=yokohama&ft:locale=en-US).

 Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is comprised of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

</td></tr><tr><td>

Zurich

</td><td>

-   Improve the performance and processing efficiency of Instance Data Replication \(IDR\) by upgrading your replication sets to V2, which uses Hermes Messaging Service. For details, see [Upgrading legacy sets](https://www.servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&family=zurich&ft:locale=en-US).
-   Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table created before the upgrade are automatically truncated.

</td></tr><tr><td>

Australia

</td><td>

Log rotation is automatically enabled for the Replication Payload Error \[idr\_replication\_payload\_error\] table after the upgrade. By default, the log rotation schedule is composed of seven shards, with five days for each shard. All log entries in this table that are created before the upgrade are automatically truncated.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Instance Data Replication.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Scheduled seeding](https://www.servicenow.com/docs/access?context=set-up-scheduled-replication-idr&family=yokohama&ft:locale=en-US)**

Replicate data from a producer to a consumer at scheduled times each day.

-   **[Multiple seeding requests](https://www.servicenow.com/docs/access?context=seed-consumer-instance&family=yokohama&ft:locale=en-US)**

Run concurrent seeding requests across multiple replication sets, with up to one active request per set.

-   **[Automatically seed missing or mismatched records](https://www.servicenow.com/docs/access?context=compare-replicated-data&family=yokohama&ft:locale=en-US)**

Automatically seed missing or mismatched records when you create a data comparison request.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Monitor scheduled replication sets](https://www.servicenow.com/docs/access?context=instance-data-replication-dashboard&family=zurich&ft:locale=en-US)**

Monitor the progress your scheduled replication sets in the IDR Monitoring Dashboard.

-   **[Track scheduled replication requests](https://www.servicenow.com/docs/access?context=set-up-scheduled-replication-idr&family=zurich&ft:locale=en-US)**

Track the progress of scheduled replication requests in the Scheduled Replication Requests related list.


</td></tr><tr><td>

Australia

</td><td>

-   **[IDR Diagnostics page improvements](https://www.servicenow.com/docs/access?context=test-IDR-connectivity&family=australia&ft:locale=en-US)**

Access detailed test descriptions and results on the redesigned IDR Diagnostics page.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Instance Data Replication features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Seeding request improvements](https://www.servicenow.com/docs/access?context=exploring-instance-data-replication&family=yokohama&ft:locale=en-US)**

In V2 replication sets, the number of records in a seeding request is now unlimited.

-   **[Data comparison improvements](https://www.servicenow.com/docs/access?context=comparing-replicated-data&family=yokohama&ft:locale=en-US)**

In V2 replication sets, the number of records in comparison or reseeding counts is now unlimited.

-   **[Reseed missing attachments](https://www.servicenow.com/docs/access?context=comparing-replicated-data&family=yokohama&ft:locale=en-US)**

Attachments are now included in data comparison requests.

-   **[Seeding performance improvements](https://www.servicenow.com/docs/access?context=seed-consumer-instance&family=yokohama&ft:locale=en-US)**

Seeding throughput and message queue efficiency has been optimized in IDR.


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

Between your current release family and Australia, some Instance Data Replication features or functionality were removed.

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

-   The Key Management Service test has been removed from the IDR Diagnostics page.
-   The VAULT Service Status test has been removed from the IDR Diagnostics page.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Instance Data Replication features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Legacy replication sets are planned for deprecation by the Zurich release. To continue replicating data in Zurich, you must upgrade all legacy replication sets to V2. For details on upgrading legacy replication sets to V2 before the upgrade, see [Upgrading legacy sets](https://www.servicenow.com/docs/access?context=upgrading-legacy-replication-sets-v2&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Legacy replication sets have been deprecated in the Zurich release and are no longer supported.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Instance Data Replication.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Instance Data Replication is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see [Request an Instance Data Replication subscription](https://www.servicenow.com/docs/access?context=request-instance-data-replication&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Instance Data Replication is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see [Request a subscription](https://www.servicenow.com/docs/access?context=request-instance-data-replication&family=zurich&ft:locale=en-US).

</td></tr><tr><td>

Australia

</td><td>

IDR is a ServiceNow AI Platform feature that is available with activation of the IDR \(com.glide.idr\) plugin, which requires a separate subscription. For details, see [Request a subscription](https://www.servicenow.com/docs/access?context=request-instance-data-replication&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Instance Data Replication we have noted them here.

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

If any specific browser requirements were introduced or changed for Instance Data Replication we have noted them here.

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

Review details on accessibility information for Instance Data Replication, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Instance Data Replication we have noted them here.

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

If there are specific highlight considerations for Instance Data Replication we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Replicate data that's frequently updated in large tables on your instance by scheduling data replication.
-   Queue multiple seeding requests from your producer instance.
-   Reseed missing or mismatched records automatically when creating a data comparison request.

 See [Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Monitor the progress of all your scheduled replication sets.
-   Track the progress of scheduled replication requests within a scheduled replication set.
-   Access details of scheduled replication requests within a scheduled replication set.

 See [Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

View updated diagnostic test descriptions and results on the redesigned IDR Diagnostics page.

 See [Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)


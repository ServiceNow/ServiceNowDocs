---
title: Delta content crawls for external content connectors
description: Delta content crawls improve content crawl performance by only retrieving newly added, changed, or deleted items from an external content connector's source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/delta-content-crawls-external-content-connectors.html
release: australia
product: Search Administration
classification: search-administration
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 4
breadcrumb: [Explore, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Delta content crawls for external content connectors

Delta content crawls improve content crawl performance by only retrieving newly added, changed, or deleted items from an external content connector's source system.

## Delta content crawls overview

By default, an external content connector's content crawl examines all content items from its source system to determine which ones to retrieve and index for search. If the source system contains many items, a full content crawl can take a long time to complete. This remains true even if the number of items with actual updates is fairly small.

Starting with External Content Connectors 9.0, the External Content Connectors application supports delta content crawl operations for some external content connectors. When running a delta content crawl, an external content connector only examines, retrieves, and indexes newly added, changed, or deleted items from its source system. By ignoring unchanged items, delta content crawling can significantly reduce the time taken to crawl content from the source system. This means you can refresh your searchable content more often by running delta content crawls between your scheduled full or partial content crawls.

**Note:** Delta content crawls don't replace full content crawls. They're supplemental crawls that enable you to refresh searchable content more frequently in between full content crawls.

By default, delta content crawls aren't active for any external content connector. Connector admins can activate or deactivate delta content crawls for individual connectors of supported types. To view the activation procedure, see [Activate delta content crawling for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/activate-delta-content-crawling-external-content-connector.md).

**Note:** In External Content Connectors 9.0, delta content crawls are only supported for the [Google Drive external content connector.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/google-drive-external-content-connector.md)

## Scheduling of delta content crawls

When you activate delta content crawling for an external content connector, the system begins scheduling delta content crawls for that connector once it completes a full content crawl. Until that full content crawl is completed, no delta content crawls will be scheduled.

**Note:** If you upgrade to a new External Content Connectors major release, run a full content crawl in the new version for each connector that has delta content crawling activated. Full content crawls run in a previous External Content Connectors release don't retrieve all of the metadata needed for delta content crawling. As an example, after upgrading from External Content Connectors version 8.0 to version 9.0, you must complete a full content crawl in version 9.0 for each connector that has delta content crawls activated. Until you complete that full content crawl, delta content crawls won't run for the connector.

The system automatically schedules delta content crawls for connectors that have them activated. You can't override the automatic scheduling.

Scheduled delta content crawls aren't guaranteed to run at any particular time. The system may pause, delay, or skip a scheduled delta content crawl. In particular, delta crawls won't run if a full or partial content crawl is already running for the external content connector.

Delta content crawls have a time limit. If a delta content crawl doesn't complete within its specified time, the next delta content crawl attempts to pick up where the previous one stopped. If delta content crawls are consistently unable to keep up with changes made in the connector's source system, you may need to run more frequent full content crawls to keep your searchable content up-to-date with the source data.

## Interaction with other content crawls

Full, partial, and delta content crawls can't run in parallel. The system won't start a delta content crawl for a connector if it has a full or partial content crawl running.

If you try to start a one-time full or partial content crawl while a delta content crawl is running, the system offers you the following options:

-   Queue the one-time full or partial content crawl so that it doesn't start until the current delta content crawl completes.
-   Cancel the current delta content crawl and start the one-time full or partial content crawl immediately.

## Delta content crawl history

In the connector editor's **Crawl history** tab, a summary of delta content crawl activity over the last 30 days appears in the **Delta content crawls** section. Delta content crawl history doesn't appear in the **Crawl history** listing.

## Limitations of delta content crawls

Delta content crawls may not detect all relevant changes to items in the source system. As an example, a delta content crawl may not detect that a source system content item has been deleted. Other similar detection issues are specific to the connector type.

In all of these cases, running a new full connector content crawl detects the overlooked changes and brings your AI Search index up to date.

**Parent Topic:**[Exploring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/exploring-ext-cont-connectors.md)


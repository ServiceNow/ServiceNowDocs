---
title: Activate delta content crawling for an external content connector
description: Reduce content crawl time for your external content connector by enabling delta content crawls, which ignore unchanged content items from your source system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/activate-delta-content-crawling-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
breadcrumb: [Crawl, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate delta content crawling for an external content connector

Reduce content crawl time for your external content connector by enabling delta content crawls, which ignore unchanged content items from your source system.

## Before you begin

You must have completed a full content crawl for the selected external content connector. For details on creating and running content crawls, see [Create a content crawl for an external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/create-content-crawl-external-content-connector.md).

**Note:** If you upgraded from a previous version of the External Content Connectors application, you must have completed a new full content crawl in the new version. Full content crawls completed in a previous version don't retrieve all of the metadata needed for delta content crawling.

Role required: sn\_ext\_conn.xcc\_admin

## About this task

The External Content Connectors application supports delta content crawl operations for some external content connectors. When running a delta content crawl, an external content connector only examines, retrieves, and indexes newly added, changed, or deleted items from its source system. By ignoring unchanged items, delta content crawling can significantly reduce the time taken to crawl content from the source system. This means you can refresh your searchable content more often by running delta content crawls between your scheduled full or partial content crawls.

**Note:** Delta content crawls don't replace full content crawls. They're supplemental crawls that enable you to refresh searchable content more frequently in between full content crawls.

To enable delta content crawling for an external content connector, perform the following steps.

**Note:** In External Content Connectors 9.0, delta content crawls are only supported for the [Google Drive external content connector.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/google-drive-external-content-connector.md)

For full details on how delta content crawls behave and operate, see [Delta content crawls for external content connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/delta-content-crawls-external-content-connectors.md).

## Procedure

1.  Navigate to **All** &gt; **External Content Connectors** &gt; **External Content Admin Home**.

2.  In the Connectors list, select the record for the external content connector that you want to enable delta content crawling for.

3.  In the connector editor's **Manage crawls** tab, navigate to the **Default crawl schedules** section and select the **Delta content crawls** option.

4.  Select **Save default schedules**.


## Result

The system activates delta content crawling for the selected external content connector.

You can deactivate delta content crawling for the connector by deselecting the **Delta content crawls** option, then selecting **Save default schedules**.

**Parent Topic:**[Crawling content with External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/search-administration/using-ext-cont-connectors.md)


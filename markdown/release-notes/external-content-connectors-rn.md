---
title: External Content Connectors release notes
description: The ServiceNow External Content Connectors applications make content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online searchable using AI Search. See the following sections for release notes by version.Version 9.2 adds the Custom Connector Gateway external content connector, support for additional binary file formats, secure search for the Amazon S3 external content connector, and a more descriptive analytics metric name.Version 9.0 adds a connector health dashboard, an index inspector tool, regulatory market conformance for the Amazon S3 external content connector, and delta content crawl support for the Google Drive external content connector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/external-content-connectors-rn.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow AI Platform administration release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# External Content Connectors release notes

The ServiceNow® External Content Connectors applications make content and metadata from external content repositories such as Atlassian Confluence Cloud and Microsoft SharePoint Online searchable using AI Search. See the following sections for release notes by version.

## About External Content Connectors

-   Make content and metadata from your external document repositories searchable in AI Search applications.
-   Map your source system users to their ServiceNow AI Platform user accounts to preserve their access permissions for crawled content.
-   Schedule content and user permission crawls or run them manually as needed.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Install External Content Connectors by requesting the External Content Connectors Application Suite plugin from the ServiceNow Store. If you want to activate the ServiceNow product documentation external content connector or the Webcrawler external content connector, you must request activation of those plugins after the Application Suite is activated.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Browser requirements**

    For optimal performance, use External Content Connectors in the latest release of Google Chrome or Mozilla Firefox. Internet Explorer isn't supported.

-   **Additional requirements**

    Your instance needs inbound mTLS support to run external content connector crawls. If inbound mTLS support isn't already activated for your instance, it should be automatically activated after you install the External Content Connectors Application Suite plugin.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/now-platform-admin-rn-landing.md)

## Version 9.2

Version 9.2 adds the Custom Connector Gateway external content connector, support for additional binary file formats, secure search for the Amazon S3 external content connector, and a more descriptive analytics metric name.

### What's new

-   **Custom Connector Gateway external content connector**

    Retrieve content, metadata, and users from any source system using your own custom connector, running in your local or cloud environment. Send your retrieved data to a gateway connector running on your instance by submitting Custom Connector Gateway API requests to an ingest gateway host. The gateway connector indexes your retrieved data and makes it searchable in the ServiceNow AI Platform®.

-   **Support for Markdown and email message binary files and attachments**

    Extract searchable text from Markdown \(.md\) and email message \(.eml, .msg\) files and attachments retrieved by your external content connectors.


### What's changed

-   **Secure search for the Amazon S3 external content connector**

    The Amazon S3 external content connector adds support for secure search. The **Settings** tab for this connector includes a new **User mapping settings** screen. On this screen, you can select one of three permission modes for the connector and optionally configure user mappings. You can also configure user permission crawls for the connector if using a permission mode that requires them.

-   **Analytics for external content connectors**

    The **Quota usage** metric has been renamed **Connector limit** for clarity.


### Plugin information

-   **New plugins**

    External Content Connectors Custom Connector \(com.sn\_ext\_conn\_ccg\): Plugin for the Custom Connector Gateway external content connector. This plugin is included when you install the External Content Connectors Application Suite plugin.


## Version 9.0

Version 9.0 adds a connector health dashboard, an index inspector tool, regulatory market conformance for the Amazon S3 external content connector, and delta content crawl support for the Google Drive external content connector.

### What's new

-   **Connector health dashboard**

    View and resolve connector health issues using the connector health dashboard.

-   **Index inspector tool**

    Verify indexing status and error counts for individual content items using the index inspector tool. Optionally review additional item details, see which users and groups can view the item in secure search, and view retrieval and indexing errors for the item.

-   **Advanced connection settings for the Amazon S3 external content connector**

    Optionally specify advanced connection settings including the AWS region and Amazon S3 endpoint you want the connector to use. You can also specify a list of Amazon S3 buckets to retrieve content from, or leave this list empty to enable auto-discovery of buckets.

-   **Delta content crawls for the Google Drive connector**

    Reduce content crawl time with delta content crawls. Unlike full content crawls, delta content crawls ignore unchanged content items in a connector's source system. Delta content crawls are supported for the Google Drive external content connector.


### What's changed

-   **Crawl schedules tab renamed**

    In the external content connector editor, the **Crawl schedules** tab has been renamed to **Manage crawls**.



---
title: Update a data asset
description: Edit catalog asset metadata to add business context, improve discoverability, and provide additional information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/update-data-asset.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Governing the Data Catalog, Data Catalog, Workflow Data Fabric]
---

# Update a data asset

Edit catalog asset metadata to add business context, improve discoverability, and provide additional information.

## Before you begin

Role required: data steward \(**df\_data\_steward**\)

## About this task

Enrich assets with descriptions, business context, and organizational metadata to help users understand what the data represents and how to use it. Some fields are auto-populated from source systems and are read-only to maintain data integrity with the source.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the **Data catalog** icon.

3.  Select a data asset to open its details page.

4.  From the form context menu, select **Edit**.

5.  Update the general details.

    -   Name: Name of the data asset.
    -   Description: Description of the asset.
    -   Summary: Brief summary of the asset.
6.  Update the governance details.

    -   Lifecycle status: Current state of the data asset. Possible values are: Approved, Deprecated, Draft, In review, Rejected.
    -   Status message: Description of why the data asset is in its current status.
    -   Owner: Person responsible for business decisions about the data. Adding or removing an owner sends the owner an email notification.
    -   Steward: Person responsible for data quality and governance. Adding or removing a steward sends the steward an email notification.
7.  Update the classification details.

    -   Domain: Terms that represent the logical grouping of related data assets \(like customer or product data\). For details about creating domains, see [Create catalog domains](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-domains-dc.md).
    -   Tags: Non-hierarchical label or keyword that provides context and descriptive metadata, making data easier to organize, locate, and manage. For details about creating tags, see [Create catalog tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-tags-dc.md).
    -   Related terms: Glossary terms connected to this data asset.
8.  Select **Save**.

    \[Omitted image "dc-data-asset-edits.png"\] Alt text: Data asset form showing editable fields and the Save button


**Parent Topic:**[Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/manage-data-catalog.md)


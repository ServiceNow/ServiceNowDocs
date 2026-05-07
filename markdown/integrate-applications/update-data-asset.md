---
title: Update a data asset
description: Edit catalog asset metadata to add business context, improve discoverability, and provide additional information.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Governing the Data Catalog, Data Catalog, Workflow Data Fabric]
---

# Update a data asset

Edit catalog asset metadata to add business context, improve discoverability, and provide additional information.

## Before you begin

Role required: Data Steward \(df\_data\_steward\)

## About this task

Enrich assets with descriptions, business context, and organizational metadata to help users understand what the data represents and how to use it. Some fields are auto-populated from source systems and are read-only to maintain data integrity with the source.

## Procedure

1.  Navigate to **All** &gt; **Workflow Data Fabric** &gt; **Workflow Data Fabric Home**.

2.  Select the Data catalog icon in the left sidebar.

3.  Select the data asset you want to edit.

4.  From the form context menu select the edit option.

5.  Update the general details.

    -   Name: Update the name of the data asset.
    -   Description: Provide a description for the asset.
    -   Summary: Provide a brief summary.
6.  Update the governance details.

    -   Lifecycle status: Current state of the data asset. Possible values are: Approved, Deprecated, Draft, In review, Rejected.
    -   Status message: Description of why the data asset is in its current status.
    -   Owner: Person responsible for business decisions about the data.
    -   Steward: Person responsible for data quality and governance.
7.  Update the classification details.

    -   Domain: Terms that represent the logical grouping of related data assets \(like customer or product data\). For details about creating domains, see [Create catalog domains](create-domains-dc.md).
    -   Tags: A non-hierarchical label or keyword that provides context and descriptive metadata to a piece of data, making it easier to organize, locate, and manage. For details about creating tags, see [Create catalog tags](create-tags-dc.md).
    -   Related terms: Glossary terms connected to this data asset.
8.  Select **Save**. ![Edit a data asset](../image/dc-data-asset-edits.png)


**Parent Topic:**[Governing the Data Catalog](../concept/manage-data-catalog.md)


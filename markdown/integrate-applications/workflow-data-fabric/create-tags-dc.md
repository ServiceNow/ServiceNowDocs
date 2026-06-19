---
title: Create catalog tags
description: Create tags that can be applied to data assets for classification and categorization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/create-tags-dc.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Governing the Data Catalog, Data Catalog, Workflow Data Fabric]
---

# Create catalog tags

Create tags that can be applied to data assets for classification and categorization.

Create and manage catalog tags 

## Before you begin

Role required: Data Steward \(df\_data \_ steward\)

## About this task

Catalog tags are metadata labels that you can apply to data assets to enable classification, categorization, and discovery. Tags provide a flexible way to describe data characteristics, business context, data quality, sensitivity levels, or any other attributes relevant to your organization.

You can search and filter data assets based on applied tags, making it easier to find data assets that meet specific criteria or share common characteristics. \[Omitted image "dc-tag-manager.png"\] Alt text: View list of catalog tags

## Procedure

1.  Navigate to **All** **&gt; Workflow data Fabric** **&gt; Data Catalog**.

2.  Select a data asset to open its details page.

3.  Select **Edit**.

4.  In the Classification section, select the + icon next to Tags.

    The Tag Manager opens.

5.  Select **Add**.

6.  Complete the tag form with the tag name and description.

    The tag name can’t be edited once it is saved.

7.  Select **Create**.

    The tag is created and appears in the Tag Manager list. From here, you can edit the tag description or delete the tag.

8.  Select the tag in the tag manager list to edit its description.

9.  Locate the tag that you want to delete and select the delete icon.

    The system displays whether the tag is applied to any assets before allowing deletion.


## Result

The tag is created and appears in the Tag Manager list. The tag is now available to apply to any data asset in the catalog.

## What to do next

After creating tags, apply them to data assets in the Tags field of the Classification section when editing a data asset. For details, see [Update a data asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/update-data-asset.md).

**Parent Topic:**[Governing the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/manage-data-catalog.md)


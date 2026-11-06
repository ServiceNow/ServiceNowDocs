---
title: Creating and publishing product offering versions
description: As a product catalog manager, you can create and publish the product offering versions that list enhanced products and services that you can offer to your customers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/telecom-media-technology/creating-publishing-product-offering-somt.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Creating and publishing product offering versions

As a product catalog manager, you can create and publish the product offering versions that list enhanced products and services that you can offer to your customers.

## Overview of product offering versions

You create versions of product offerings by combining new versions of product, service, and resource specifications. Proper versioning enables your customer service agents to know what the latest versions of your product and service offering. This information enables you to sell more expensive, complementary, upgraded, or related products to your customers.

## Creating versions of product offerings

When you create a product offering version, complete these steps:

1.  Create and assign a version number in each of the product, service, or resource specifications or product offering records that are affected by the changes. To reflect the engineering changes that were made to the physical product, edit the following data that is associated with the product offering version:
    -   Characteristics
    -   Characteristic options
    -   Product specifications
2.  Create the required specification relationships, decomposition rules, and attribute mappings for each specification in the new version. To learn more, see [Creating and publishing specification versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/creating-publish-specification-versions-somt.md).
3.  Create the product offering, and then publish it when you update your product catalog.
4.  Retire or archive old or unused specifications, and product offerings. To learn more, see [Retiring and archiving specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/retiring-archiving-specifications-somt.md). To learn about the difference between retiring and archiving a product offering, see [Product offering life cycle states](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/creating-publishing-product-offering-somt.md).

## Updates and validations that are performed when you create and publish a product offering version

When you create a version for a published product offering, the ServiceNow AI Platform® copies the following data into, or populates, the new product offering record with the following data:

1.  Copies the following fields with these basic product offering details:
    -   **Product Specification**
    -   **Contract Term**
    -   **Monthly Recurring Charges**
    -   **Non Recurring Charges**
    -   **Description**
    -   **Offering Catalog**
    -   **Distribution Channel**
    -   **Start** and **End** date
    -   **Product code** and **Product line**
    -   **Cost to Company**
    -   **Composite**, **Installation Required**, and **Location-specific** indicators
2.  Populates the following fields with the detailed information that you enter for the new product offering version:
    -   **Version**. The next incremental number appears.
    -   **Display Name**. The display name is the system-assigned concatenation of the product offering name and its current version number. You can overwrite this field.
    -   **Initial Version**. The name of the base version of the product offering appears but can't be changed.
    -   **Previous Version**: The name of the product offering is as it was in the previous version.

When you publish the updated product version, additional validations are performed on your edits. To learn more, see the Updating and validating copied rules for a new specification version section in [Create and publish a specification version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/telecom-media-technology/create-publish-new-specification-somt.md).

## Product offering life cycle states

A product offering moves through its life cycle states in order. You can't skip a state. A retired offering can also be published again.

Retiring and archiving differ in what happens to the offering afterward. A retired offering stays in the operational tables but isn't available for ordering. An archived offering is removed from the operational tables but isn't permanently deleted.

|State|Description|Next action|
|-----|-----------|-----------|
|In Draft|The product offering is being modeled and isn't ready for ordering. This is the default state of a new product offering. You can't set the state when you create the offering.|**Publish**|
|Published|The product offering is available for ordering, including new and MACD orders.|**Retire**|
|Retired|The product offering remains in the operational tables but isn't available for ordering. The record is read-only, and the system never deletes it. Retire an offering that you might want to reuse later, for example, to create a version from it. You can also publish a retired offering again.|**Archive** or **Publish**|
|Archived|The product offering is removed from the operational tables but isn't permanently deleted.|None|

**Important:** You can archive only a retired product offering. To archive a published offering, retire it first.


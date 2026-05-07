---
title: Creating and publishing product offering versions
description: As a product catalog manager, you can create and publish the product offering versions that list the improved products and services that you can offer to your customers in a product catalog.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 2
breadcrumb: [Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Creating and publishing product offering versions

As a product catalog manager, you can create and publish the product offering versions that list the improved products and services that you can offer to your customers in a product catalog.

## Overview of product offering versions

You create product offering versions for an existing product that you're improving. You typically create versions of product offerings by combining new versions of product, service, and resource specifications. Proper versioning enables your customer service agents to know what the latest versions of your product and service offerings are when they sell more expensive, complementary, upgraded, or related products to your customers.

## Creating versions of product offerings

When you create a version of a product offering, do the following actions:

1.  Create and assign a version number in each of the product, service, or resource specifications or product offering records that are affected by the changes. To reflect the engineering changes that were made to the physical product, edit the following data that is associated with the product offering version:
    -   Characteristics
    -   Characteristic options
    -   Product specifications
2.  Create the required specification relationships, decomposition rules, and attribute mappings for each specification in the new version. To learn more, see [.](creating-publish-specification-versions-somt.md)
3.  Create the product offering, and then publish it when you update your product catalog.
4.  Retire or archive old or unused specifications, and product offerings. To learn more, see [Retiring or archiving versioned specifications and product offerings](retiring-archiving-specifications-somt.md).

## Updates and validations that are performed when you create and publish a product offering version

When you create a version for a currently published product offering, the ServiceNow AI Platform® copies the following data into, or populates, the new product offering record with the following data:

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

When you publish the updated product version, additional validations are performed on your edits. To learn more, see the Updating and validating copied rules for a new specification version section in [Create and publish a specification version](../task/create-publish-new-specification-somt.md).


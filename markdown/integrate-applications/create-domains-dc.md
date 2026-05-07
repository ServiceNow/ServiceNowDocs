---
title: Create catalog domains
description: Organize data assets by creating hierarchical domain structures that represent business areas, departments, or data categories.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Governing the Data Catalog, Data Catalog, Workflow Data Fabric]
---

# Create catalog domains

Organize data assets by creating hierarchical domain structures that represent business areas, departments, or data categories.

## Before you begin

Role required: Data Steward \(df\_data \_ steward\)

## About this task

Catalog domains help you organize data assets into logical groupings based on business areas, departments, or data types. Domains provide a hierarchical classification system that makes it easier for users to discover and navigate related data assets.

You can create root domains at the top level and subdomains \(child domains\) under existing domains to build multi-level organizational structures that reflect your business taxonomy. ![View list of domains](../image/dc-domain-manager.png)

## Procedure

1.  Navigate to **All** **&gt; Workflow data Fabric** **&gt; Data Catalog**.

2.  Select a data asset to open its details page.

3.  Select **Edit**.

4.  In the Classification section, select the + icon next to Domains.

    The Domain Manager opens.

5.  Select **Add**.

6.  Complete the domain form.

    -   Name: Enter the domain name.
    -   Description: Enter a description \(maximum 1000 characters\).
    -   Parent Domain: Select None \(root domain\) to create a root domain, or select an existing domain to create a subdomain.
7.  Select **Create**.

    The domain is created and appears in the Domain Manager list. From here, you can add child domains and edit or delete a domain.

8.  Locate the domain for which you want to create child domains and select **Add child domains**

9.  Locate the domain that you want to edit and select **Edit domain**.

    Changing the parent domain moves the domain and all its subdomains to a new location in the hierarchy.

10. Locate the domain that you want to delete and select **Delete domain**.

    Before deleting a domain, you must first remove all of its child domains.


## What to do next

After creating domain, apply them to data assets in the Domains field of the Classification section when editing a data asset. For details, see [Update a data asset](update-data-asset.md).

**Parent Topic:**[Governing the Data Catalog](../concept/manage-data-catalog.md)


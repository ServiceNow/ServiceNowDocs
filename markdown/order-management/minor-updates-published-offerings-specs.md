---
title: Minor changes to published product offerings and specifications
description: As a product catalog admin, you can make minor changes to published product offerings and specifications without creating a new version, including updating eligible fields and adding optional characteristics or future-effective optional child offerings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/minor-updates-published-offerings-specs.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Minor changes to published product offerings and specifications

As a product catalog admin, you can make minor changes to published product offerings and specifications without creating a new version, including updating eligible fields and adding optional characteristics or future-effective optional child offerings.

Minor changes can include updates to supported fields or eligible additions to a published entity. For a published product offering, you can add an optional characteristic or an optional child offering without creating a new version of the parent offering. When you add an optional child offering, specify a future effective date on the relationship to control when the child becomes available for transactions.

**Note:** Changes to fields other than those identified as minor, and changes that don’t meet the conditions for an optional characteristic or optional child relationship, require you to generate a new version of the product offering or specification.

## How minor  changes are processed 

The following sections describe the minor changes that you can make to published product offerings and specifications. Updates to supported fields and optional characteristics are applied when you save the record. An optional child-offering relationship is saved without creating a new version of the parent offering, but the child offering becomes available for transactions based on the relationship’s effective date.

At runtime, the system compares the transaction date with the effective date of the child-offering relationship. The child offering isn’t available for transactions dated before the effective date. It is available for transactions dated on or after the effective date. This evaluation applies to new-purchase and modify, add, change, or disconnect transactions.

If  you’re  using the  CPQ Configurator, minor changes are handled  as  follows: 

-   Minor changes to simple products are synchronized automatically.
-   Minor  changes  to  configurable products  require synchronization.  In the  CRM Workspace, the  **Save**  and  **Update Configuration ** buttons  are displayed  when you make  minor  changes to  a  product offering.  Selecting   **Update  Configuration ** synchronizes  the configurable  product  offering  with  its  corresponding blueprint.
-   If any blueprints  have a  reference  to a  simple or configurable product  with  minor  changes, you must  synchronize  those blueprints. 

**Related topics**  


[Using product catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/using-product-catalog.md)

[Product Catalog Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-managment.md)


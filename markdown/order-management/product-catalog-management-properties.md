---
title: Product Catalog Management properties
description: System properties available with Product Catalog Management that enable you to test and manage the visibility of product offerings and specifications to catalog consumers before they're published.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/product-catalog-management-properties.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Product Catalog Management reference, Lead-to-cash foundation, Reference, Sales Customer Relationship Management]
---

# Product Catalog Management properties

System properties available with Product Catalog Management that enable you to test and manage the visibility of product offerings and specifications to catalog consumers before they're published.

<table id="table_product-catalog-management-properties"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_prd\_pm.supported\_language\_translations

</td><td>

-   Type: String
-   Default value: Empty
-   Other possible values: Comma-separated list of language ISO codes. For example, en,fr,de.
-   Location: System Property \[sys\_properties\] table
-   Learn more: [Enable localized product catalogs and product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-multi-locale-catalogs.md).

</td></tr><tr><td>

sn\_prd\_pm.enable\_extended\_product\_lifecycle

</td><td>

-   Type: Boolean
-   Default value: false
-   Other possible values: true. Turns on the In Test and Staged life cycle statuses for product offerings and specifications.
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_prd\_pm.enable\_product\_lifecycle\_prepublish\_visibility

</td><td>

-   Type: Boolean
-   Default value: false
-   Other possible values: true. Makes In Test and Staged product offerings and specifications visible to catalog consumers before they're published. Has no effect unless sn\_prd\_pm.enable\_extended\_product\_lifecycle is also turned on.
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>For more information, see [Enable extended life cycle states for product offerings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/enable-extended-lifecycle-states.md).

**Parent Topic:**[Product Catalog Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/product-catalog-management-reference.md)

**Related topics**  


[Validating product offerings before publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/extended-product-lifecycle-states.md)

[36e0738cf8938e71ff603b1a07014fedcf33c1e8.dita](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/order-management/move-offering-spec-states.md)


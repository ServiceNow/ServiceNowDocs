---
title: Components installed with Product Catalog Management
description: Several types of components are installed with activation of the Product Catalog Management plugin, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-13"
reading_time_minutes: 2
breadcrumb: [Product Catalog Management reference, Lead-to-cash foundation, Reference, Sales Customer Relationship Management]
---

# Components installed with Product Catalog Management

Several types of components are installed with activation of the Product Catalog Management plugin, including tables and user roles.

## Roles installed

<table id="table_roles_pcm"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Characteristics viewer

 \[sn\_prd\_pm.characteristics\_viewer\]

</td><td>

Reads characteristics and characteristic values.

</td><td>

None

</td></tr><tr><td>

Characteristics writer

 \[sn\_prd\_pm.characteristics\_writer\]

</td><td>

Granular role for creating characteristics and characteristic values.

</td><td>

sn\_prd\_pm.characteristics\_viewer

</td></tr><tr><td>

External product viewer

 \[sn\_prd\_pm.external\_product\_viewer\]

</td><td>

Reads Product Specification Name and Product Offering Name at the field level.

</td><td>

sn\_prd\_pm.characteristics\_viewer

</td></tr><tr><td>

Product catalog admin

 \[sn\_prd\_pm.product\_catalog\_admin\]

</td><td>

Creates, reads, and updates products, resources, services, product, service, and resource categories, characteristics, and characteristic options.

 Exports and imports catalog entities and set up any catalog-related system properties.

</td><td>

-   sn\_prd\_pm.characteristics\_writer
-   sn\_prd\_pm.product\_catalog\_manager
-   import\_admin
-   sn\_gd\_core.decision\_tree\_author
-   sn\_gd\_guidance.guidance\_manager
-   decision\_table\_admin
-   cmdb\_read
-   sn\_export\_entities.export\_user
-   ais\_admin
-   category\_manager

</td></tr><tr><td>

Product catalog manager

 \[sn\_prd\_pm.product\_catalog\_manager\]

</td><td>

Creates, reads, and updates product specifications, resource specifications, and service specifications.

</td><td>

-   sn\_tmt\_core.inbound\_queue\_read
-   decision\_table\_admin
-   sn\_prd\_pm.product\_catalog\_viewer
-   model\_manager
-   sn\_configrule\_mgt.rule\_writer
-   sn\_customerservice.customer\_data\_viewer
-   sn\_csm\_ctxrul\_mgt.rule\_matrix\_writer

</td></tr><tr><td>

Product catalog viewer

 \[sn\_prd\_pm.product\_catalog\_viewer\]

</td><td>

Views products, resources, services, product, service, and resource categories, characteristics, and characteristic options.

</td><td>

-   canvas\_user
-   decision\_table\_reader
-   sn\_prd\_pm.product\_model\_characteristic\_viewer
-   sn\_gd\_core.decision\_tree\_user
-   sn\_prd\_pm.characteristics\_viewer

</td></tr><tr><td>

Product model characteristic granular viewer

 \[sn\_prd\_pm.product\_model\_characteristic\_granular\_viewer\]

</td><td>

Views records in the Product Model Characteristics table where the product model's Customer Visible field is true.

</td><td>

None

</td></tr><tr><td>

Product model characteristic viewer

 \[sn\_prd\_pm.product\_model\_characteristic\_viewer\]

</td><td>

Granular role for viewing records in the Product Model Characteristics table.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_tables_pcm"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Catalog Category

 \[sn\_prd\_pm\_catalog\_category\_relationship\]

</td><td>

Stores relationships between catalogs and categories.

</td></tr><tr><td>

Category To Category Relationship

 \[sn\_prd\_pm\_category\_category\_relationship\]

</td><td>

Stores relationships between categories.

</td></tr><tr><td>

Characteristic

 \[sn\_prd\_pm\_characteristic\]

</td><td>

Stores characteristic records.

</td></tr><tr><td>

Characteristic Option

 \[sn\_prd\_pm\_characteristic\_option\]

</td><td>

Stores the options available for a characteristic.

</td></tr><tr><td>

Quantity Mapping

 \[sn\_prd\_pm\_characteristic\_option\_quantity\_mapping\]

</td><td>

Stores quantity mapping records for characteristic options.

</td></tr><tr><td>

Characteristic Relationship

 \[sn\_prd\_pm\_characteristic\_relationship\]

</td><td>

Stores relationships between characteristics.

</td></tr><tr><td>

Characteristic Group

 \[sn\_prd\_pm\_configuration\]

</td><td>

Stores characteristic group records.

</td></tr><tr><td>

Distribution Channel

 \[sn\_prd\_pm\_distribution\_channel\]

</td><td>

Stores distribution channel records.

</td></tr><tr><td>

Needs Template

 \[sn\_prd\_pm\_needs\_template\]

</td><td>

Stores needs template records.

</td></tr><tr><td>

Needs Template Relationship

 \[sn\_prd\_pm\_needs\_template\_relationship\]

</td><td>

Stores relationship records for needs templates.

</td></tr><tr><td>

Product Price

 \[sn\_prd\_pm\_pricing\]

</td><td>

Stores pricing records for products.

</td></tr><tr><td>

Product Characteristics

 \[sn\_prd\_pm\_product\_characteristics\]

</td><td>

Stores characteristics associated with a product.

</td></tr><tr><td>

Product Model Characteristic

 \[sn\_prd\_pm\_product\_model\_characteristic\]

</td><td>

Stores characteristics associated with a product model.

</td></tr><tr><td>

Product Offering

 \[sn\_prd\_pm\_product\_offering\]

</td><td>

Stores product offering records.

</td></tr><tr><td>

Product Offering Catalog

 \[sn\_prd\_pm\_product\_offering\_catalog\]

</td><td>

Stores catalog records for product offerings.

</td></tr><tr><td>

Product Offering Category

 \[sn\_prd\_pm\_product\_offering\_category\]

</td><td>

Stores category records for product offerings.

</td></tr><tr><td>

Product Offering Category Relationship

 \[sn\_prd\_pm\_product\_offering\_category\_relationship\]

</td><td>

Stores relationships between product offering categories.

</td></tr><tr><td>

Product Offering Characteristic

 \[sn\_prd\_pm\_product\_offering\_characteristic\]

</td><td>

Stores characteristics associated with a product offering.

</td></tr><tr><td>

Product Offering Family

 \[sn\_prd\_pm\_product\_offering\_family\]

</td><td>

Stores product offering family records.

</td></tr><tr><td>

Needs Based Offering Recommendation

 \[sn\_prd\_pm\_product\_offering\_recommendation\]

</td><td>

Stores recommendation records for product offerings based on customer needs.

</td></tr><tr><td>

Product Offering Relationship

 \[sn\_prd\_pm\_product\_offering\_relationship\]

</td><td>

Stores relationships between product offerings.

</td></tr><tr><td>

Product Offering Relationship Characteristic

 \[sn\_prd\_pm\_product\_offering\_relationship\_characteristic\]

</td><td>

Stores characteristics for product offering relationships.

</td></tr><tr><td>

Product Offering Relationship Group

 \[sn\_prd\_pm\_product\_offering\_relationship\_group\]

</td><td>

Stores group records for product offering relationships.

</td></tr><tr><td>

Unit of Measure

 \[sn\_prd\_pm\_product\_offering\_uom\]

</td><td>

Stores unit of measure records for product offerings.

</td></tr><tr><td>

Product Specification

 \[sn\_prd\_pm\_product\_specification\]

</td><td>

Stores product specification records.

</td></tr><tr><td>

Resource Specification

 \[sn\_prd\_pm\_resource\_specification\]

</td><td>

Stores resource specification records.

</td></tr><tr><td>

Service Specification

 \[sn\_prd\_pm\_service\_specification\]

</td><td>

Stores service specification records.

</td></tr><tr><td>

Specification

 \[sn\_prd\_pm\_specification\]

</td><td>

Stores specification records.

</td></tr><tr><td>

Specification Category

 \[sn\_prd\_pm\_specification\_category\]

</td><td>

Stores category records for specifications.

</td></tr><tr><td>

Specification Product Instance Mapping

 \[sn\_prd\_pm\_specification\_char\_product\_instance\_mapping\]

</td><td>

Stores mapping records between specification characteristics and product instances.

</td></tr><tr><td>

Specification Characteristic

 \[sn\_prd\_pm\_specification\_characteristic\]

</td><td>

Stores characteristic records for specifications.

</td></tr><tr><td>

Specification Relationship

 \[sn\_prd\_pm\_specification\_relationship\]

</td><td>

Stores relationship records between specifications.

</td></tr><tr><td>

Template

 \[sn\_prd\_pm\_template\]

</td><td>

Stores template records.

</td></tr><tr><td>

Template Characteristic

 \[sn\_prd\_pm\_template\_characteristic\]

</td><td>

Stores characteristic records for templates.

</td></tr><tr><td>

Template Characteristic Option

 \[sn\_prd\_pm\_template\_characteristic\_option\]

</td><td>

Stores characteristic option records for templates.

</td></tr><tr><td>

Unit of Measure

 \[sn\_prd\_pm\_uom\]

</td><td>

Stores unit of measure records.

</td></tr><tr><td>

Unit of Measure Class

 \[sn\_prd\_pm\_uom\_class\]

</td><td>

Stores unit of measure class records.

</td></tr><tr><td>

Product Visuals

 \[sn\_prd\_pm\_visuals\]

</td><td>

Stores visual asset records for products.

</td></tr></tbody>
</table>**Parent Topic:**[Product Catalog Management reference](product-catalog-management-reference.md)


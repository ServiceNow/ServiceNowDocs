---
title: Components installed with Pricing Management
description: Several types of components are installed with activation of the Pricing Management plugin, including tables, user roles, and scheduled jobs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/components-installed-with-pricing-management.html
release: australia
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 3
breadcrumb: [Pricing Management reference, Configure, price, quote, Reference, Sales Customer Relationship Management]
---

# Components installed with Pricing Management

Several types of components are installed with activation of the Pricing Management plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_fpw_5qb_ngc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Price list administrator\[sn\_csm\_pricing.pricelist\_administrator\]

</td><td>

Create and update pricing entities, set up or edit pricing-related system properties, and view transaction logs.

</td><td>

-   sn\_csm\_pricing.pricelist\_manager
-   sn\_export\_entities.export\_user
-   sn\_csm\_ctxrul\_mgt.context\_rule\_administrator
-   import\_admin

</td></tr><tr><td>

Price list manager\[sn\_csm\_pricing.pricelist\_manager\]

</td><td>

Create and update pricing entities such as price lists and price list lines.

</td><td>

sn\_csm\_pricing.pricelist\_writer

</td></tr><tr><td>

Price list writer\[sn\_csm\_pricing.pricelist\_writer\]

</td><td>

Granular role that has read, write, and delete access to pricing entities. To delete a pricing entity such as a price list or cost book, the pricing entity must be in Draft state.

</td><td>

-   decision\_table\_crud\_api
-   decision\_rule\_author
-   sn\_csm\_ctxrul\_mgt.rule\_matrix\_writer
-   sn\_csm\_pricing.pricelist\_viewer
-   personalize\_decision\_table\_input

</td></tr><tr><td>

Pricing integrator\[sn\_csm\_pricing.pricing\_integrator\]

</td><td>

Role required to access pricing features through the Pricing REST API when using the CPQ Configurator.

</td><td>

None

</td></tr><tr><td>

Pricing integrator internal\[sn\_csm\_pricing.pricing\_integrator\_internal\]

</td><td>

Role required to access pricing features through the Pricing REST API when using the CPQ Configurator.

</td><td>

None

</td></tr><tr><td>

Sales agreement price list writer

 \[sn\_csm\_pricing.sales\_agreement\_pricelist\_writer\]

</td><td>

Granular role that has read, write, and delete access to pricing entities. Write access only for Sales Agreement price lists.

</td><td>

None

</td></tr><tr><td>

Price list viewer\[sn\_csm\_pricing.pricelist\_viewer\]

</td><td>

Granular role that has read access to pricing entities such as price lists, price list lines, attribute adjustments, cost books, cost book lines, and rule matrices.

</td><td>

-   sn\_prd\_pm.product\_catalog\_viewer
-   sn\_customerservice.customer\_data\_viewer
-   sn\_csm\_ctxrul\_mgt.rule\_matrix\_viewer
-   sn\_csm\_ctxrul\_mgt.context\_variable\_viewer

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_un4_cvm_wgc"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedule job to populate code field on pricing entities

</td><td>

Populates the Code field on pricing entity records. The Code field is a mandatory, indexed identifier on price lists, price list lines, cost books, cost book lines, adjustment types, pricing plans, and pricing plan steps. Run this job to add a Code value to records that were created before the field existed. The job is active and runs only when you run it, not on a schedule.

</td></tr></tbody>
</table>## Tables installed

<table id="table_jpw_5qb_ngc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Price List

 \[sn\_csm\_pricing\_price\_list\]

</td><td>

Stores named price lists scoped to an account, a currency, and a date range.

</td></tr><tr><td>

Price List Line

 \[sn\_csm\_pricing\_price\_list\_line\]

</td><td>

Stores the per-product-offering price rows that belong to a price list, including the list price, floor price, and ceiling price.

</td></tr><tr><td>

Cost Book

 \[sn\_csm\_pricing\_cost\_book\]

</td><td>

Stores named cost books scoped to a currency and a date range.

</td></tr><tr><td>

Cost Book Line

 \[sn\_csm\_pricing\_cost\_book\_line\]

</td><td>

Stores the per-product-offering cost rows that belong to a cost book.

</td></tr><tr><td>

Pricing Adjustment Type

 \[sn\_csm\_pricing\_pricing\_adjustment\_type\]

</td><td>

Stores the adjustment types that the pricing engine can apply, such as markup amount, markup percent, markdown amount, markdown percent, and price override.

</td></tr><tr><td>

Pricing Plan\[sn\_csm\_pricing\_pricing\_plan\]

</td><td>

Stores the pricing steps used by the pricing engine to retrieve and calculate product pricing.

</td></tr><tr><td>

Pricing Plan Step

 \[sn\_csm\_pricing\_pricing\_plan\_step\]

</td><td>

Stores one step in a pricing plan, including its action, its sequence, an optional rule matrix, an optional extension point, and the header and line conditions that control when the step runs.

</td></tr><tr><td>

Attribute Adjustment

 \[sn\_csm\_pricing\_attribute\_adjustment\]

</td><td>

Stores the price and cost modifiers that apply to a product offering for a given set of characteristics. This table is installed only when the Product and Pricing Rules plugin \(sn\_csm\_price\_mtrx\) is also installed.

</td></tr><tr><td>

Pricing Engine Request

 \[sn\_csm\_pricing\_pricing\_engine\_request\]

</td><td>

Stores the request and the response for each pricing engine call, so that you can audit and replay a call.

</td></tr><tr><td>

Pricing Context Data

 \[sn\_csm\_pricing\_context\_data\]

</td><td>

Stores the pricing context that the pricing engine builds for a request.

</td></tr><tr><td>

Pricing Engine Cache

 \[sn\_csm\_pricing\_engine\_cache\]

</td><td>

Caches the pricing engine response for each pricing line item, so that unchanged lines aren't recalculated.

</td></tr><tr><td>

Pricing Engine Parallel Execution

 \[sn\_csm\_pricing\_engine\_parallel\_execution\]

</td><td>

Stores one record for each slice of lines when the pricing engine runs in parallel for a large request.

</td></tr><tr><td>

Pricing Dependency Tracker

 \[sn\_csm\_pricing\_dep\_tracker\]

</td><td>

Tracks the source lines that a target line depends on, so that the pricing engine can invalidate and recalculate the right lines.

</td></tr><tr><td>

Derived Price Rules Cache

 \[sn\_csm\_pricing\_der\_rules\_cache\]

</td><td>

Caches the result of evaluating the derived-price rule matrix for a pair of source and target product offerings, so that the pricing engine does not evaluate the matrix again on every request.

 Caching is controlled by the sn\_csm\_pricing.derived\_price\_cache\_enabled system property, which is true by default. Set it to false to make the pricing engine evaluate the matrix live for every request. Cached results expire after the number of hours set in the sn\_csm\_pricing.derived\_price\_cache\_ttl\_hours system property, which is 72 by default.

</td></tr></tbody>
</table>**Parent Topic:**[Pricing Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/price-management-reference.md)


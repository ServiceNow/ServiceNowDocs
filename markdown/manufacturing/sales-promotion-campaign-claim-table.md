---
title: Sales Promotion Campaign Claim tables
description: This section explains the sales promotion campaign claims tables in Manufacturing Commercial Operations.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sales promotion campaign data model, Data model, Reference, Manufacturing Commercial Operations]
---

# Sales Promotion Campaign Claim tables

This section explains the sales promotion campaign claims tables in Manufacturing Commercial Operations.

## Sales Promotion plugin

The sales promotion feature adds or modifies the existing tables:

-   Expense Line \[fm\_expense\_line\]
-   Case \[sn\_customerservice\_case\]
-   Case Line \[sn\_case\_line\]

The sales promotion plugin adds the following tables.

<table id="table_ywt_vgz_r2c"><thead><tr><th>

Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sales Promotion\[sn\_sales\_prm\_mgmt\_sales\_promotion\]

</td><td>

Stores the sales promotion details, which includes promotion name, start and end date of the promotion, incentive type, and incentive percentage. The checklist template provides the details of the documents required during the approval process.

</td></tr><tr><td>

Promotion Type\[sn\_sales\_prm\_mgmt\_promotion\_type\]

</td><td>

Stores the promotion type details. Possible types are the following: -   trading promotion
-   senior citizen promotion
-   veteran promotion

.

</td></tr><tr><td>

MCO Input Set\[sn\_mfg\_cmn\_mco\_input\_set\]

</td><td>

Stores the grouping information for input attributes.

</td></tr><tr><td>

MCO Input Attribute\[sn\_mfg\_cmn\_mco\_input\_attributes\]

</td><td>

Stores the attributes or input variables for an input group.

</td></tr><tr><td>

Applicable Product\[sn\_sales\_prm\_mgmt\_applicable\_product\]

</td><td>

Stores the product details which are applicable for the target sales promotion campaign. It can be based on the specific model \(manufacturer\) or asset \(lot or serial number\) level.

</td></tr><tr><td>

Claim Case\[sn\_claim\_cmn\_case\]

</td><td>

Stores the input provided by the dealer to the manufacturer when the claim request is raised. This information is retrieved from the Promotion input table.

</td></tr><tr><td>

Visibility Criteria\[sn\_sales\_prm\_mgmt\_visibility\_criteria\]

</td><td>

Stores and displays the dealer name for which the target sales promotion is applicable.

</td></tr><tr><td>

Sales Promotion Claim Case\[sn\_sls\_prm\_clm\_mgt\_case\]

</td><td>

Stores the claim case and claim case line progress state information. For example, if the claim case is in the draft, submitted, review, or approved states.

</td></tr><tr><td>

Sales Promotion Claim Case Line\[sn\_sls\_prm\_clm\_mgt\_case\_line\]

</td><td>

Stores the information about the claim, such as the claim date, amount claimed, status of the claim, and asset.

</td></tr><tr><td>

Expense Line\[fm\_expense\_line\]

</td><td>

Automatically populates the short description of expense lines with the work order short description when expense lines are manually created from work orders.

</td></tr><tr><td>

Claim Case Line\[sn\_claim\_cmn\_case\_line\]

</td><td>

Stores the details of the items pertaining to a claim header.

</td></tr><tr><td>

Case\[sn\_customerservice\_case\]

</td><td>

Stores the case records created and submitted by the dealer.

</td></tr><tr><td>

Case Line\[sn\_case\_line\]

</td><td>

Stores the case line item records.

</td></tr></tbody>
</table>To learn more about the Case and Case Line, see [Case Lines and Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-case-mgmt-case-lines.md).

**Parent Topic:**[Sales promotion campaign data model](sales-promotion-campaign-claims.md)


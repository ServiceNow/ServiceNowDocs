---
title: Reconciliation and product results
description: Field descriptions for the reconciliation results, product results, and software product results.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Software license usage, Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Reconciliation and product results

Field descriptions for the reconciliation results, product results, and software product results.

## Reconciliation results

Reconciliation results are listed in the navigation path **Software Asset** &gt; **Reconciliation** &gt; **Historical Results**

<table id="table_lrw_slt_ty"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique identifying number that is generated during the reconciliation process.

</td></tr><tr><td>

Last reconciled

</td><td>

Date of last reconciliation run.

</td></tr><tr><td>

Ran for

</td><td>

All publishers, or specific publishers.

</td></tr><tr><td>

Publishers

</td><td>

Only shown if publishers were specified on which to run reconciliation.

</td></tr><tr><td>

Group

</td><td>

Group specified on which to run reconciliation. Values include None, Country, Department, Company, Region, and Cost Center.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup specified on which to run reconciliation. Values include None, Country, Department, Company, Region, and Cost Center.

</td></tr><tr><td>

Status

</td><td>

Status of the reconciliation.-   Completed
-   In Progress
-   Failed

</td></tr><tr><td>

Progress

</td><td>

Percent complete and progress bar for the reconciliation run.

</td></tr><tr><td>

Progress summary

</td><td>

Specific step within the reconciliation process.**Note:** This list column is not shown by default. You can personalize your list column settings to add it, if desired.

</td></tr></tbody>
</table>## Software product results

You can access Software Models, Unlicensed Installs, and Removal candidates related lists from a product result record.

A product result for a licensable product is generated after reconciliation even if there are no software models defined for the product.

**Note:** A Software Model Results record is only created when a software model or entitlement exists for the product.

For licensable products, a software model is automatically created for any unlicensed installs, subscriptions, or options in the Product Results list that do not have an entitlement by default. See [properties](sam-properties.md) to change the **com.snc.samp.automaticsmrcreation** property setting. You can also set the **com.snc.samp.automaticsmcreation** property to have a software model created automatically for not-licensable products, if desired.

To view more information about a specific software product result, select an entry from the Product Results list. Refer to the following table for field descriptions.

<table id="table_bnb_zqv_pz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Unique product result number that is generated during the reconciliation process.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software.

</td></tr><tr><td>

Product

</td><td>

Name of software product.

</td></tr><tr><td>

Group

</td><td>

Group to which the product result belongs.

</td></tr><tr><td>

Subgroup

</td><td>

Subgroup to which the product result belongs.

</td></tr><tr><td>

Latest

</td><td>

Indicates whether this product result is from the most recent reconciliation run.

</td></tr><tr><td>

Reconciliation result

</td><td>

Unique reconciliation result number that is generated during the reconciliation process.

</td></tr><tr><td>

Status

</td><td>

Status of the product.-   Compliant
-   Not Compliant

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating non-compliance based on the lowest number of rights needed.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of rights not being used. The sum of all Over Licensed amount values from every software model result.

</td></tr><tr><td>

Potential savings

</td><td>

Estimated cost of savings if software installations are reclaimed. The sum of all potential savings from all removal candidates.

</td></tr><tr><td>

Licensed installs

</td><td>

Total number of installations that are licensed for the product.

</td></tr><tr><td>

Unlicensed installs

</td><td>

Total number of installations that are unlicensed for the product.

</td></tr><tr><td class="sub-head" colspan="2">

Software Model Results

</td></tr><tr><td>

Status

</td><td>

Status of the software model.

</td></tr><tr><td>

Software model

</td><td>

Name of the software model.

</td></tr><tr><td>

Unlicensed installs

</td><td>

Total number of installations that are unlicensed for the associated software product.

</td></tr><tr><td>

True-up cost

</td><td>

Estimated cost of remediating non-compliance based on the lowest number of rights needed.

</td></tr><tr><td>

Over-licensed amount

</td><td>

Estimated cost of rights not being used.

</td></tr><tr><td>

Potential savings

</td><td>

Estimated cost saved if reclamation candidates are reclaimed.

</td></tr><tr><td class="sub-head" colspan="2">

Licensed Installs

</td></tr><tr><td>

Display name

</td><td>

Name of the licensed software installation.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software product.

</td></tr><tr><td>

Version

</td><td>

Version of the software product.

</td></tr><tr><td>

Discovery model

</td><td>

Software discovery model that represents the installed software product.

</td></tr><tr><td>

Installed on

</td><td>

Device on which the product is installed.

</td></tr><tr><td>

Assigned to

</td><td>

User to which the product is assigned.

</td></tr><tr><td class="sub-head" colspan="2">

Unlicensed Installs

</td></tr><tr><td>

Display name

</td><td>

Name of the unlicensed software installation.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software product.

</td></tr><tr><td>

Version

</td><td>

Version of the software product.

</td></tr><tr><td>

Installed on

</td><td>

Device on which the product is installed.

</td></tr><tr><td>

Assigned to

</td><td>

User to which the product is assigned.

</td></tr><tr><td class="sub-head" colspan="2">

Unlicensed Subscriptions**Note:** This related list is only shown if the software product is a subscription.

</td></tr><tr><td>

Publisher

</td><td>

Publisher of the software product associated with the unlicensed subscription.

</td></tr><tr><td>

Product

</td><td>

Name of the software product associated with the unlicensed software subscription.

</td></tr><tr><td>

User

</td><td>

Name of the user associated with the unlicensed software subscription.

</td></tr><tr><td>

User principal name

</td><td>

Email address of the associated user.

</td></tr><tr><td>

Software model

</td><td>

Software model associated with the unlicensed software subscription.

</td></tr><tr><td>

Subscription profile

</td><td>

Integration profile associated with the unlicensed software subscription.

</td></tr><tr><td class="sub-head" colspan="2">

Unlicensed Users**Note:** This related list contains SAP system users and is only shown for SAP publisher.

</td></tr><tr><td>

Display name

</td><td>

Unique display name.

</td></tr><tr><td>

User

</td><td>

User in the SAP system.

</td></tr><tr><td>

SAP user id

</td><td>

SAP ID of the user with access to an SAP system.

</td></tr><tr><td>

Email

</td><td>

SAP user email.

</td></tr><tr><td>

Names

</td><td>

First and last names of the SAP user.

</td></tr><tr><td>

User type

</td><td>

The type of user in the SAP system.-   Dialog
-   System

</td></tr><tr><td>

License type

</td><td>

The named user type value assigned to the user in the specified SAP system.

</td></tr><tr><td>

Named user type

</td><td>

Normalized named user type assigned to the user in the specified SAP system.

</td></tr><tr><td>

SAP client

</td><td>

SAP client from which the user information was pulled.

</td></tr><tr><td class="sub-head" colspan="2">

Removal Candidates

</td></tr><tr><td>

Number

</td><td>

Removal candidate number.

</td></tr><tr><td>

Name

</td><td>

Name of the removal candidate.

</td></tr><tr><td>

Justification

</td><td>

Justification for becoming a removal candidate.-   Low Usage \(default\)
-   Unallocated
-   Unlicensed
-   Restricted Software

</td></tr><tr><td>

Product

</td><td>

Name of the product.

</td></tr><tr><td>

Publisher

</td><td>

Name of the publisher.

</td></tr><tr><td>

State

</td><td>

State of the removal candidate.-   Attention Required
-   Ready
-   Awaiting User
-   Awaiting Approval
-   Approval
-   Awaiting Revocation
-   Closed Complete
-   Closed Skipped

</td></tr><tr><td>

Potential savings

</td><td>

Savings to be gained from reclaiming unused software installations.

</td></tr></tbody>
</table>**Parent Topic:**[Software license usage](../concept/sam-license-workbench.md)


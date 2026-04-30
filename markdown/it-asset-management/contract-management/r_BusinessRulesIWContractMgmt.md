---
title: Business rules installed with Contract Management
description: Business rules are added with Contract Management.
locale: en-US
release: yokohama
product: Contract Management
classification: contract-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Components installed with Contract Management, Contract Management, IT Asset Management]
---

# Business rules installed with Contract Management

Business rules are added with Contract Management.

<table id="table_hmk_t3f_4r"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Calculate projected costs \(Reports\)

</td><td>

Contract \[ast\_contract\]

</td><td>

Calculates the projected monthly and annual costs for a contract when costs or payment schedule changes.

</td></tr><tr><td>

Calculate totals with tax

</td><td>

Contract \[ast\_contract\]

</td><td>

Calculates the **Tax cost** and **Total cost** fields for a contract when the contract is created or updated.

</td></tr><tr><td>

Contract history

</td><td>

Contract \[ast\_contract\]

</td><td>

Stores history when the start, end, or terms and conditions of a contract change.

</td></tr><tr><td>

Create approval record

</td><td>

Contract \[ast\_contract\]

</td><td>

Updates contract **Terms and Conditions** and starts the contract approval workflow when a contract is sent for review.

</td></tr><tr><td>

Flag terms and conditions

</td><td>

Terms and Conditions \[clm\_m2m\_contract\_and\_terms\]

</td><td>

Sets the **Use** flag on a Terms and Conditions record to **true** after the record is associated with a contract or to **false** after the record is disassociated from a contract.

</td></tr><tr><td>

Activate count for manual licenses

</td><td>

Software License Instance \[ast\_license\_software\_instance\]

</td><td>

Calculates and updates the number of computers a particular license is installed on when a software license instance is created or deleted.

</td></tr><tr><td>

Manage contract lifecycle

</td><td>

Contract \[ast\_contract\]

</td><td>

This business rule: -   Updates the end date of a contract when a contract extension has been approved.
-   Renews the contract, updating its start date, end date, and base cost \(if cost adjustments must be applied\) when a contract renewal has been approved and the renewal has reached its start date.
-   Runs the condition checks to evaluate if dates need to be changed when a contract is approved, or an extension or renewal is approved, or the start or end dates have changed.

</td></tr><tr><td>

Post outage to news

</td><td>

Service \[cmdb\_ci\_service\]

</td><td>

Posts a news article on the knowledge table when there is an outage.

</td></tr><tr><td>

Update contract cost per asset

</td><td>

Asset Covered \[clm\_m2m\_contract\_asset\]

</td><td>

Updates the cost per unit value based on the total cost and number of assets associated to the contract.

</td></tr><tr><td>

Update contract lifetime cost

</td><td>

Contract Rate Card \[fm\_contract\_rate\_card\]

</td><td>

Calculates the lifetime cost of the contract by calculating the sum of the contract expense lines.

</td></tr><tr><td>

Updates after contract dates change

</td><td>

Contract \[ast\_contract\]

</td><td>

Updates the **Date added** and **Date removed** fields for all assets and users associated with a contract if the contract end date changes.

</td></tr><tr><td>

Updates after rate card dates change

</td><td>

Contract Rate Card \[fm\_contract\_rate\_card\]

</td><td>

Updates the related contract assets and users linked to the rate card when the end date is changed.

</td></tr><tr><td>

Verify contract’s start and end dates

</td><td>

Contract \[ast\_contract\]

</td><td>

Validates contract start and end dates and contract renewal start and end dates.

</td></tr><tr><td>

Verify purchase agreement discount price

</td><td>

Contract \[ast\_contract\]

</td><td>

For contracts with the contract model **Purchase Agreement**, the business rule validates that the **Discount** field does not contain a value less than zero or greater than 99.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Contract Management](r_ComponentsInstalledWContractMgmt.md)


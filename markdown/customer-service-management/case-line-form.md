---
title: Case line item form
description: The case line item form displays details about a case line item on a case record.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-28"
reading_time_minutes: 3
breadcrumb: [Case lines and workflows, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case line item form

The case line item form displays details about a case line item on a case record.

Agents can use the case line item form to create a new case line item record and to view and edit an existing case line item record. When editing, agents can:

-   Change the reason code
-   Change the Priority, Assigned to, and Contact

To access a case line item record, navigate to **All** &gt; **Customer Service** &gt; **Cases** &gt; **All Line Items** and select a record. Users with the following roles can access this list: system administrator, customer service agent, and customer service manager.

The case line item form includes the following related lists:

-   Case Line Tasks
-   Case Line Characteristics

<table id="table_vyg_gzg_lvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The automatically generated record number. The prefix for numbers from the Case Line table is **CSL**.

</td></tr><tr><td>

Parent case

</td><td>

The parent case for the case line item record. This field is mandatory.

</td></tr><tr><td>

Parent case line

</td><td>

The parent case line for the case line item record. This field supports the case lines hierarchy.

</td></tr><tr><td>

Top case line

</td><td>

The top case line for the case line item record. This field supports the case lines hierarchy.

</td></tr><tr><td>

Account

</td><td>

The name of the company that the case is opened for.

</td></tr><tr><td>

Contact

</td><td>

The name of the customer contact for the case.

</td></tr><tr><td>

Product offering

</td><td>

This field is a reference to the Product Offering table \[sn\_prd\_pm\_product\_offering\].

</td></tr><tr><td>

Product specification

</td><td>

This field is a reference to the Product Specification table \[sn\_prd\_pm\_product\_specification\].

</td></tr><tr><td>

Product model

</td><td>

This field is a reference to the Product Model table \[cmdb\_model\].

</td></tr><tr><td>

Short description

</td><td>

A brief description of the case line item record.

</td></tr><tr><td>

State

</td><td>

A case line item record can be in any of the following states:-   Draft
-   New
-   Work in Progress
-   Awaiting Info
-   Resolved - Accepted
-   Resolved - Denied
-   Canceled

If all of the case line items on a record are in one of the following terminal states, the system syncs the record state to the case line item state:

-   Resolved - Accepted
-   Resolved - Denied
-   Canceled

Actions such as **Submit Case** and **Assign to me** change the state of the case and the case lines.

</td></tr><tr><td>

Priority

</td><td>

The priority of the case line record:-   1 - Critical
-   2 - High
-   3 - Moderate
-   4 - Low
-   5 - Planning

</td></tr><tr><td>

Assigned to

</td><td>

The agent assigned to the case line item record.

</td></tr><tr><td>

Request reason code

</td><td>

The reason for the requested change. Can be different for each case line item.-   Increase Demand
-   Change in Contract
-   Initial input incorrect
-   None

</td></tr><tr><td>

Sold product

</td><td>

This field is a reference to the Sold Product table \[sn\_install\_base\_sold\_product\].

</td></tr><tr><td>

Install base

</td><td>

This field is a reference to the Install Base Item table \[sn\_install\_base\_item\].If the **Account** field is populated, this field displays the install base items for the selected account.

</td></tr><tr><td>

Asset

</td><td>

This field is a reference to the Asset table \[asset\].If the **Account** field is populated, this field displays the assets for the selected account.

If the **Product model** field is populated, this field displays the assets associated to the selected product model.

If both the **Account** and **Product model** fields are populated, this field displays the assets associated with selected account and product model.

</td></tr><tr><td>

Resolution code

</td><td>

A code that indicates the resolution state of the case line item record.-   Change approved
-   Added replacement product

</td></tr><tr><td>

Resolution Notes

</td><td>

The agent can use this field to specify how they reached the decision to either accept or deny a change to a case line item.

</td></tr><tr><td>

Contributor Users

</td><td>

This field is populated when a case line task is assigned to a case task agent.

</td></tr><tr><td>

Contributor Groups

</td><td>

This field is populated when a case line task is assigned to a case task agent.

</td></tr><tr><td>

Work notes

</td><td>

Enables users to post work notes to the record.

</td></tr></tbody>
</table>
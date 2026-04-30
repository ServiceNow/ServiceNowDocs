---
title: Create an investment entity
description: Create an entity for investments through which you can receive or allocate funds.
locale: en-US
release: xanadu
product: Investment Funding
classification: investment-funding
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Investment Funding administration, Investment Funding, Strategic Portfolio Management]
---

# Create an investment entity

Create an entity for investments through which you can receive or allocate funds.

## Before you begin

Role required: sn\_invst\_pln\_v2.investment\_admin

## Procedure

1.  Navigate to **All** &gt; **Investment Funding** &gt; **Setup** &gt; **Investment Entities**.

2.  Click **New**.

3.  On the form, fill in the fields.

    **Note:** The **Entity** tab in the form is replaced by the **Owner** tab when the **Generic** option is selected.

<table id="table_mng_sgd_phb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the investment entity.

</td></tr><tr><td>

Active

</td><td>

Option for indicating the status of the investment entity.

 You can create investments only for active investment entities.

</td></tr><tr><td>

Description

</td><td>

Short description of the investment entity.

</td></tr></tbody>
</table>    When the **Generic** option is not selected:

<table id="table_m3x_bzd_5jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Transaction table on which funding is enabled.

</td></tr><tr><td>

Condition

</td><td>

Condition to filter data from the table enabled for funding.

 For example, you could enable funding for the Project table and add a filter condition to list only projects that are in the Ready state.

</td></tr><tr><td>

Owner field

</td><td>

Any user field in the transaction table mapped to the investment owner field.

 The user on the mapped field is automatically assigned as the investment owner when you are creating an investment.

 For example, for a Project investment entity, you could map the Project manager field as the investment owner field.

</td></tr></tbody>
</table>    When the **Generic** option is selected:

<table id="table_zzw_dzd_5jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Owner table

</td><td>

User table mapped as the investment owner field.

</td></tr><tr><td>

Owner filter

</td><td>

Condition to filter users that are listed in the **Owner** field in the Investment form to select the investment owner.

 For example, for a Project investment entity, you could create a filter to list only users with the Project manager role.

 By default, the **Active is true** filter is set, which means that only active users are listed for selection.

</td></tr></tbody>
</table>4.  Click the **Unlock fundable entities** icon to enable the selection of entities that can be funded by the current entity.

    For example, a portfolio entity can fund a program, a program can fund a project, a project can request from a program, and a program can request from a portfolio.

5.  Add the entities to the **Fundable entities** list.

    If no value is selected, all entities are considered to be enabled for funding.

6.  Click **Submit**.


## What to do next

-   Create funding artifacts to [create a business rule to synchronize investment and investment entity owners](enable-funding-owner-sync.md) or to [add a related link on the investment target form](create-funding-artifacts.md).
-   Create [a top-level investment](create-top-level-investment.md) or [an investment](create-investment.md) for an investment entity.

-   **[Enable synchronization of investment and investment entity owners](enable-funding-owner-sync.md)**  
Create a business rule for an investment entity that synchronizes the investment owner with the investment entity owner. If you update the name of the investment entity owner, the owner of the corresponding investment and the **Viewable by** field for the investment is automatically updated.
-   **[Access investments directly from an investment target](create-funding-artifacts.md)**  
Create a related link to go directly to the My Funds page from an investment target.

**Parent Topic:**[Investment Funding administration](../concept/investment-funding-administration.md)


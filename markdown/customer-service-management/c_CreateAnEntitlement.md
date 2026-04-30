---
title: Create entitlements for CSM entities
description: Create an entitlement for a Customer Service Management entity such as an account, a consumer, or a product.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure entitlements, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Create entitlements for CSM entities

Create an entitlement for a Customer Service Management entity such as an account, a consumer, or a product.

## Before you begin

Role required: sn\_customerservice\_manager or admin

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Contracts** &gt; **Entitlements**.

    You can also create an entitlement from the **Entitlements** related list on the Account and Contract forms.

2.  Click **New** at the top of the Entitlements list.

3.  Fill in the fields on the Entitlement form.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the entitlement.

</td></tr><tr><td>

Product

</td><td>

The product model associated with this entitlement.

</td></tr><tr><td>

Account

</td><td>

The name of the account associated with this entitlement.

</td></tr><tr><td>

Consumer

</td><td>

The name of the consumer associated with this entitlement.

</td></tr><tr><td>

Contract

</td><td>

The contract number associated with this entitlement .

</td></tr><tr><td>

Asset

</td><td>

The asset tag number or the serial number of the asset associated with this entitlement.

</td></tr><tr><td>

Active

</td><td>

Check this box to enable the entitlement. Active entitlements are available for selection when creating a new case.

</td></tr><tr><td>

Channel

</td><td>

One or more communication channels associated with this entitlement. -   Email
-   Web
-   Phone
-   Chat


</td></tr><tr><td>

Install Base Item

</td><td>

The install base item associated with the entitlement. Configure the form layout to add the **Install Base Item** field.**Note:** This field is only available if the Customer Service Install Base Management plugin \(com.snc.install\_base\) is installed.

</td></tr><tr><td>

Sold Product

</td><td>

The sold product associated with the entitlement. Configure the form layout to add the **Sold Product** field.**Note:** This field is only available if the Customer Service Install Base Management plugin \(com.snc.install\_base\) is installed.

</td></tr><tr><td>

Business hours

</td><td>

The schedule associated with this entitlement.

</td></tr><tr><td>

Start date

</td><td>

The start date for this entitlement.

</td></tr><tr><td>

End date

</td><td>

The end date for this entitlement.

</td></tr><tr><td>

Total Units

</td><td>

The total number of units designated for this entitlement. This field is active if the **Per unit** check box is enabled.

</td></tr><tr><td>

Remaining Units

</td><td>

The number of available units that are remaining for this entitlement. This field is active if the **Per unit** check box is enabled. This field is updated using business rules.

-   When using cases as the unit type, the **Update case entitlement on Close** business rule updates this field when a case for a product, asset, company, or contract that has an associated entitlement is closed.
-   To use hours as the unit type, customers must create a separate business rule. For example, create a rule that is applied to the amount of time an agent spends on a case. When a case is resolved, deduct the hours spent from the total service hours available in the entitlement.


</td></tr><tr><td>

Unit

</td><td>

The type of unit being measured for this entitlement: **Cases** or **Hours**.

</td></tr><tr><td>

Per unit

</td><td>

Select this check box to enable unit counters. If enabled, the **Total Units** and **Remaining Units** fields are activated.

</td></tr></tbody>
</table>4.  Click **Submit**.



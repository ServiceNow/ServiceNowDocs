---
title: Entitlement form
description: Entitlement form enables you to add the details to create account, consumer, or product.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manufacturing Commercial Operations reference, Manufacturing Commercial Operations]
---

# Entitlement form

Entitlement form enables you to add the details to create account, consumer, or product.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The nName of the entitlement.

</td></tr><tr><td>

Product

</td><td>

The p&lt;roduct model that is associated with this entitlement.

</td></tr><tr><td>

Account

</td><td>

The nName of the account that is associated with this entitlement.

</td></tr><tr><td>

Consumer

</td><td>

NThe name of the consumer that is associated with this entitlement.

</td></tr><tr><td>

Contract

</td><td>

The cContract number that is associated with this entitlement.

</td></tr><tr><td>

Asset

</td><td>

The aAsset tag number or the serial number of the asset that is associated with this entitlement.

</td></tr><tr><td>

Active

</td><td>

Check this boxOption to enable the entitlement. Active entitlements are available for selection when creating a case.

</td></tr><tr><td>

Channel

</td><td>

One or more communication channels associated with this entitlement. Options include:-   Alert
-   Community
-   ebonding
-   In person
-   Phone
-   Email
-   Web
-   Virtual Agent
-   Chat

</td></tr><tr><td>

Business hours

</td><td>

The sSchedule associated with this entitlement.

</td></tr><tr><td>

Start date

</td><td>

The sStart date for this entitlement.

</td></tr><tr><td>

End date

</td><td>

The eEnd date for this entitlement.

</td></tr><tr><td>

Total Units

</td><td>

TThe total number of units designated for this entitlement. This field is active if the **Per unit** check boxfield is enabled.

</td></tr><tr><td>

Remaining Units

</td><td>

The nNumber of available units that are remaining for this entitlement. This field is active if the **Per unit** check boxoption is enabled. This field is updated using business rules.

-   To use cases as the unit type, the **Update case entitlement on Close** business rule updates this field when a case for a product, asset, company, or contract that has an associated entitlement is closed.
-   To use hours as the unit type, customers must create a separate business rule. For example, create a rule that is applied to the amount of time an agent spends on a case. When a case is resolved, deduct the hours spent from the total service hours available in the entitlement.

</td></tr><tr><td>

Unit

</td><td>

The tType of unit being measured for this entitlement. Options are: **Cases** or **Hours**.

</td></tr><tr><td>

Per unit

</td><td>

Select this check boxOption to enable unit counters. If enabled, the **Total Units** and **Remaining Units** fields are activated.

</td></tr><tr><td>

Install Base Item

</td><td>

The install base item associated with the entitlement.**Note:** Configure the form layout to add the **Install Base Item** field.

</td></tr><tr><td>

Sold Product

</td><td>

The sold product associated with the entitlement. **Note:** Configure the form layout to add the **Sold Product** field.

</td></tr></tbody>
</table>
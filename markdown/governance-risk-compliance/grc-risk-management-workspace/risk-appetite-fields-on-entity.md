---
title: Risk appetite fields on the Entity form
description: Learn about the risk appetite fields on the Entity form. Use these fields to define the risk appetite, evaluate all the possible risks, and set the boundaries for the acceptable and unacceptable risks in the Risk Management application.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Define the risk appetite for an entity, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Risk appetite fields on the Entity form

Learn about the risk appetite fields on the Entity form. Use these fields to define the risk appetite, evaluate all the possible risks, and set the boundaries for the acceptable and unacceptable risks in the Risk Management application.

See the following table for a description of the field values.

**Note:** The risk appetite fields that appear on the entity form depends on the advanced risk assessment properties set by the risk administrator.

<table id="table_g2y_bgb_pvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Override qualitative risk appetite

</td><td>

Option to override the qualitative risk appetite of the parent entity. By default, all entities inherit the risk appetite of the upstream entity in the entity form. When you select this option, you can define the risk appetite values for the current entity separately.**Note:** This field appears only when there’s an upstream entity available for the current entity.

</td></tr><tr><td>

Qualitative appetite

</td><td>

Risk appetite in numerical scale and rating terms. The qualitative appetite is compared with the qualitative risk rating to compute the qualitative appetite status. You can define the qualitative appetite based on the appetite scale set by the risk administrator. The default options are as follows:-   1 - Averse
-   2 - Minimalist
-   3 - Cautious
-   4 - Open
-   5 - Hungry

 A risk administrator can change or create the risk appetite scales based on the organization's requirement. For more information, see [Set up a risk appetite scale](../../grc-risk/task/set-up-risk-appetite-scale.md).

 After you define the qualitative appetite, you can copy it to the downstream entities.

 **Note:** A risk user and risk reader with the sn\_risk\_advanced.qualitative\_risk\_appetite\_reader role can only view the qualitative appetite and qualitative tolerance values on the form and in other places.

</td></tr><tr><td>

Quantitative appetite

</td><td>

Risk appetite in quantitative terms. The quantitative risk appetite can be measured and expressed in monetary values. The quantitative appetite is the amount of loss that an organization is willing to risk. For example, an organization decides to have $10,000 \(US dollars\) as a target non-performing asset \(NPA\) for this year, which means that the organization defines $10,000 \(US dollars\) as the quantitative risk appetite.The quantitative appetite is compared with the annual loss expectancy \(ALE\) to compute the quantitative appetite status.

 **Note:** A risk user and risk reader with the sn\_risk\_advanced.quantitative\_risk\_appetite\_reader role can only view the quantitative appetite and the quantitative tolerance values on the form and in other places.

</td></tr><tr><td>

Qualitative tolerance

</td><td>

Risk tolerance in numerical scale and rating terms. The risk tolerance is the standard deviation from the defined risk appetite. The qualitative tolerance is compared with the qualitative risk rating to compute the qualitative appetite status. The qualitative tolerance should be greater than the defined qualitative appetite. You can define the qualitative tolerance based on the appetite scale that is set by the risk administrator. The default options are as follows:-   1 - Averse
-   2 - Minimalist
-   3 - Cautious
-   4 - Open
-   5 - Hungry

 A risk administrator can modify or create the risk appetite scales based on the organization's requirement. For more information, see [Set up a risk appetite scale](../../grc-risk/task/set-up-risk-appetite-scale.md).

</td></tr><tr><td>

Quantitative tolerance

</td><td>

Risk tolerance in quantitative terms. The risk tolerance is the standard deviation from the defined risk appetite. The quantitative risk tolerance can be measured and expressed in monetary values. For example, an organization decides to have $15,000 \(US dollars\) as a target non-performing asset \(NPA\) for this year, which means that the organization defines $15,000 as the quantitative risk tolerance.The quantitative tolerance is compared with the annual loss expectancy \(ALE\) to compute the quantitative appetite status.

 **Note:** The quantitative tolerance should be greater than the defined quantitative appetite.

</td></tr><tr><td class="sub-head" colspan="2">

Risk appetite status

</td></tr><tr><td>

Qualitative appetite status

</td><td>

Qualitative appetite status of the entity. The qualitative appetite status is calculated by comparing the defined qualitative appetite with the qualitative appetite that is mapped to the final risk rating. A risk administrator can map the appetite scales to the risk rating criteria for the final assessment type in the risk assessment methodology \(RAM\).**Note:** The primary RAM that is associated with the entity class is considered for status calculation.

 For example, if you define the qualitative appetite as 2-Minimalist and the qualitative tolerance as 4-Open, then the following statuses appear:

-   For a qualitative risk rating of 1- Averse or 2-Minimalist, the appetite status is within appetite.
-   For a qualitative risk rating of 3-Cautious or 4-Open, the appetite status is outside the appetite.
-   For a qualitative risk rating of 5-Hungry, the appetite status is outside the tolerance.

</td></tr><tr><td>

Quantitative appetite status

</td><td>

Quantitative appetite status of the entity. The annual loss expectancy \(ALE\) values are compared with the defined quantitative appetite to calculate this appetite status.**Note:** The aggregated ALE value from the primary RAM that is associated with the entity class are considered for the status calculation.

 For example, if you define the quantitative appetite as $1000 \(US dollars\) and the quantitative tolerance as $1500, then the following statuses appear:

-   For ALE equal to or less than $1000, the appetite status is within the appetite.
-   For ALE ranges from $1001 to $1500, the appetite status is outside the appetite.
-   For ALE more than $1500, the appetite status is outside the tolerance.

</td></tr><tr><td>

Appetite status

</td><td>

Overall appetite status. The overall appetite status considers the worst-case scenario between the qualitative and quantitative status. For example, if the qualitative appetite status is within the appetite and the quantitative appetite status is outside the appetite, then the overall appetite status is outside the appetite.

</td></tr></tbody>
</table>**Parent Topic:**[Define the risk appetite for an entity](../task/define-risk-appetite-on-entity.md)


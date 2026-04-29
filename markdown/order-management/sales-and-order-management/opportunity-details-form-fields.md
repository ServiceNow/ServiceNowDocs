---
title: Opportunity details form
description: Field descriptions for editing or reviewing details on the Opportunity form for Opportunity Management.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Opportunity Management reference, Lead and opportunity management, Reference, Sales and Order Management]
---

# Opportunity details form

Field descriptions for editing or reviewing details on the Opportunity form for Opportunity Management.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

The system-generated number of the opportunity starting with the prefix OPTY.

</td></tr><tr><td>

Primary Quote

</td><td>

A Primary Quote within an opportunity.

</td></tr><tr><td>

Account

</td><td>

Company name of the customer account.

</td></tr><tr><td>

Industry

</td><td>

Name of the industry. For example, Telecommunications or Manufacturing or Healthcare or Banking.

</td></tr><tr><td>

Contact

</td><td>

Name of the individual in the company that you interact with.

</td></tr><tr><td>

Estimated Deal Size

</td><td>

Amount of potential opportunity.

</td></tr><tr><td>

Deal type

</td><td>

Indicates the type of deal associated with the opportunity:-   Direct: The seller engages directly with the customer, with no intermediary partner involved.
-   Indirect: The seller engages the customer through an intermediary, such as a reseller, service provider, or distributor.

</td></tr><tr><td>

Probability %

</td><td>

Estimated percentage of the sales opportunity's success.

</td></tr><tr><td>

Route to market

</td><td>

Identifies the exact sales channel used to execute the deal:-   Direct
-   Reseller
-   Service Provider
-   Distributor

</td></tr><tr><td>

Amount

</td><td>

Total opportunity amount.**Note:** If an opportunity doesn’t have any line items, then the amount picks up the same value as the **Estimated Deal Size**. When opportunity line items are added, the amount value changes as the value is picked up from **Total TCV**.

</td></tr><tr><td>

Sales Cycle Type

</td><td>

Type of sales, for example NEWCUST, RENEW, or UPSELL.

</td></tr><tr><td>

Weighted Amount

</td><td>

Total revenue adjusted by the probability percentage.The **Weighted Amount** for an opportunity is calculated by multiplying the **Probability %** with the **Amount**. For example, if the probability percentage for an opportunity is 10 \(0.1%\) and the amount is 100$, the weighted amount is 0.1 X 100 = 10.00.

</td></tr><tr><td>

Stage

</td><td>

Phases of the opportunity. For example, Qualify, Develop Propose, Negotiate, Closed-Won, or Closed-Lost.

</td></tr><tr><td>

Opportunity Group

</td><td>

Logical grouping of related opportunities.

</td></tr><tr><td>

Forecast Category

</td><td>

Forecast classification of the opportunity.

</td></tr><tr><td>

Territory

</td><td>

Sales territory associated with the opportunity. Used to assign responsibility, control access, and support reporting and forecasting.

</td></tr><tr><td>

Owner

</td><td>

Sales agent or sales representative assigned to this opportunity.

</td></tr><tr><td>

Channel partner

</td><td>

An external organization involved in selling, influencing, or supporting an opportunity as part of an indirect sales.

</td></tr><tr><td>

Short Description

</td><td>

Brief description of the opportunity.

</td></tr><tr><td>

Description

</td><td>

Description of the opportunity.

</td></tr></tbody>
</table><table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Currency

</td><td>

Currency of the price list, for example USD for US dollars.

</td></tr><tr><td>

Price List

</td><td>

Default price list for the opportunity.

</td></tr><tr><td>

Term \(months\)

</td><td>

Subscription period of the opportunity line item.The default term is 12 months.

</td></tr><tr><td>

Total one-Time Price

</td><td>

Total price of all one-time products or services in the opportunity.

</td></tr><tr><td>

Total MRR

</td><td>

Total monthly recurring revenue \(MRR\) amount for all recurring products and services.

</td></tr><tr><td>

Total ARR

</td><td>

Total annual recurring revenue \(ARR\) amount for all recurring products and services each year.

</td></tr><tr><td>

Total ACV

</td><td>

Total annual contract value \(ACV\), which is the yearly amount revenue for all products and services from a customer contract.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Total Renewal Amount|The sum of all renewal amounts associated with the opportunity. Represents revenue from renewing existing contracts.|
|Total Upsell/Downsell Amount|The net sum of all upsell and downsell amounts on the opportunity. Represents incremental increase or decrease in contract value compared to the existing contract.|
|Total TCV|Total contract value \(TCV\), which is the total amount of revenue from a customer contract expected over the lifetime of the contract.|
|Total Net New Amount|The cumulative net new price associated with the opportunity, excluding renewal portions of existing contracts|
|Total One‑Time Price|The total price of all one‑time \(non‑recurring\) products or services included in the opportunity.|

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Win reason

</td><td>

A predefined choice that captures the primary reason an opportunity was won. Used to record why the customer selected the solution and to support win/loss analysis and reporting. The choices are:-   Brand and reputation
-   GenAI capabilities
-   Ease of implementation
-   Security, Risk and compliance
-   Ability to customize
-   Product features and functionality
-   Upsell/cross sell merged opportunity
-   Partner support
-   Executive relationships
-   Others - please specify
-   I don't know
-   Consolidation

</td></tr><tr><td>

Loss reason

</td><td>

A predefined choice that captures the primary reason an opportunity was lost or resulted in no decision. Used to analyze deal losses and identify patterns across competitors, products, or pricing. The choices are:-   Customer not ready
-   Lack of GenAI capabilities
-   Security, Risk and compliance did not fit customer's needs
-   Inability to customize
-   Product features and functionality did not fit customer's needs
-   No longer funded
-   Price too high for value gained
-   Product has too many issues
-   Lack of partner support
-   Account went silent
-   Contract consolidated
-   Others - please specifyI don't know

</td></tr><tr><td>

Lost to

</td><td>

Identifies the competitor to whom the opportunity was lost. The list is populated from competitors already associated with the opportunity. Used for competitive analysis and reporting.

</td></tr><tr><td>

Outcome notes

</td><td>

Free‑text notes used to capture additional context or supporting details for the win or loss outcome, beyond the selected reason. Remains visible for both won and lost opportunities.

</td></tr></tbody>
</table><table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Identifies the source from where the opportunity originated. The options are:-   Lead: Indicates that the opportunity originated from a lead record.
-   Direct: Indicates that the opportunity was created directly by a sales user without an originating lead, for example through direct customer engagement or outbound sales activity.
-   Partner: Indicates that the opportunity originated from a partner, such as a reseller, distributor, or alliance partner who identified or referred the deal.
-   Other: Indicates that the opportunity originated from a source that does not fall into the standard Lead, Direct, or Partner categories. Used when the source cannot be clearly classified.

</td></tr><tr><td>

Lead

</td><td>

The lead record associated with the opportunity, indicating the originating lead from which the opportunity was created.

</td></tr><tr><td>

Score

</td><td>

A system‑derived or user‑assigned value used to indicate the relative quality or priority of the opportunity.

</td></tr><tr><td>

Rating

</td><td>

A qualitative assessment of the opportunity, typically used to classify opportunity attractiveness or health. The classifications are:-   Cold: Indicates low engagement or low likelihood of progression. The opportunity shows limited momentum, minimal customer activity, or weak buying signals.
-   Warm: Indicates moderate engagement and emerging buying interest. The opportunity is progressing, but key signals or commitments are still developing.
-   Hot: Indicates strong engagement and a high level of buying intent. The opportunity shows clear momentum with positive signals toward closure.
-   Super Hot: Indicates very strong engagement and an imminent likelihood of closure. The opportunity demonstrates sustained momentum, high confidence, and near‑term action.

</td></tr><tr><td>

Contract start date

</td><td>

The date on which the customer contract associated with the opportunity begins.

</td></tr><tr><td>

Estimated Closed Date

</td><td>

The expected date on which the opportunity is projected to close. Used for pipeline planning and forecasting.

</td></tr><tr><td>

Actual Closed Date

</td><td>

The date on which the opportunity was actually closed, either as won or lost.

</td></tr><tr><td>

Consolidated opportunity

</td><td>

Indicates that the opportunity is part of an account or contract consolidation, where multiple source opportunities are merged into a single target opportunity for execution and reporting.

</td></tr><tr><td>

Contract end date

</td><td>

The date on which the customer contract associated with the opportunity ends.

</td></tr><tr><td>

Customer Preferences

</td><td>

The customer's preferred mode of communication:-   Do Not Call
-   Do Not Email
-   Do not Share

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Opened By|Identifies the user who initially opened or created the opportunity record in the system.|
|Created|Displays the date and time when the opportunity record was created in the system. This value is system‑generated and cannot be edited.|
|Work Notes|Internal notes used to capture additional information, updates, or context related to the opportunity. Work notes are intended for internal use and are not visible to customers.|

**Parent Topic:**[Opportunity Management reference](../concept/opportunity-management-reference.md)


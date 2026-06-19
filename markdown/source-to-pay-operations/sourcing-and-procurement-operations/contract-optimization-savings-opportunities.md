---
title: Contract optimization savings opportunities
description: The Contract Optimization Opportunity Finder Agent identifies opportunities to reduce costs by renegotiating price escalations, renewal caps, and payment terms on supplier contracts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/contract-optimization-savings-opportunities.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-05-15"
reading_time_minutes: 3
keywords: [contract optimization, price escalation, renewal cap, payment terms, savings opportunity]
breadcrumb: [Savings opportunities, Spend and Savings Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Contract optimization savings opportunities

The Contract Optimization Opportunity Finder Agent identifies opportunities to reduce costs by renegotiating price escalations, renewal caps, and payment terms on supplier contracts.

The Contract Optimization Opportunity Finder Agent analyzes supplier contracts that have an attached document to extract clause-level data and identify opportunities to reduce future spend. Two savings levers are currently supported: price escalation and renewal caps, and payment terms. For each lever, the agent calculates the savings available from renegotiating the existing terms and displays the finding as a savings opportunity .

## Price escalation and renewal cap opportunities

Many supplier contracts include clauses that allow the supplier to increase prices each year or at each renewal. Over multi-year terms, even small escalation percentages can compound into significant additional spend. The agent identifies contracts where renegotiating the escalation or renewal cap can produce measurable savings.

For each in-scope contract, the agent forecasts contracted spend under the current escalation clause and models an alternative scenario where the escalation is reduced. The default alternative scenario applies a 25 percent reduction relative to the original escalation percentage. This reduction is fixed and is not configurable.

The forecast period is derived from the contract validity or payment terms. If the contract document does not provide a duration, the agent defaults the forecast period to one year.

The agent calculates the cumulative difference between the baseline forecast and the negotiated forecast over the forecast period. For example, a contract with a $20M annual baseline and a 7 percent annual escalation produces a 3-year forecast of $64.3M. Reducing the escalation to 3 percent produces a forecast of $61.8M. The cumulative savings of $2.5M is the value shown on the opportunity.

A price escalation or renewal cap opportunity captures the following information:

-   The contract analyzed and the supplier on the contract.
-   The current escalation percentage extracted from the contract document.
-   The proposed renegotiated escalation or renewal cap.
-   The cumulative estimated savings over the forecast period.
-   The contracts linked as source records for the eventual pipeline project.

When you act on the opportunity, the linked contract is attached to the draft pipeline project as a previous contract so that the sourcing team can carry the source evidence into renegotiation.

## Payment terms opportunities

Payment terms set the timing of supplier invoice payments, such as Net 30 or Net 60. Extending payment windows or capturing early payment discounts can improve working capital. The agent analyzes contract clauses and historical payment data to identify contracts where these levers can produce financial benefit.

For contracts that have an attached document, the agent extracts the existing payment terms and any early payment discount clauses. The agent compares the current payment window against an extended window \(typically 30 days longer\) and calculates the working capital benefit using a configurable treasury rate. Where an early payment discount clause exists, the agent also models the savings from taking the discount.

The agent uses a configurable treasury rate, also called cost of capital, to estimate the value of extending payment windows. The rate is stored in the system property **sn\_spend\_gen\_ai.savings\_opportunity.cost\_of\_capital** \(default value: 9 , expressed as a percentage\). An administrator with the sn\_spend\_mgmt.category\_manager\_admin role can read and update this property.

If the remaining contract validity is less than one year, the agent prorates the savings estimate to reflect the actual time remaining on the contract.

A payment terms opportunity captures the following information:

-   The contract analyzed and the supplier on the contract.
-   The existing payment terms and the proposed extended payment terms.
-   The early payment discount terms when present in the contract clauses.
-   The estimated annual savings from the proposed change, calculated using the configured treasury rate.

**Parent Topic:**[Savings opportunity identification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/savings-opportunity-identification.md)


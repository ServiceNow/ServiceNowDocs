---
title: Chief Procurement Officer Dashboard indicators
description: Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Procurement Officer \(CPRO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Chief Procurement Officer Dashboard indicators

Indicators provide the data used in most of the dashboard’s visualizations. The indicators are used across the dashboard.

This dashboard employs Automated and Formula indicators. For more information about configuring these indicators, see

-   [Automated indicators](../../performance-analytics/concept/automated-indicators.md)
-   [Formula indicators](../../performance-analytics/concept/formula-indicators.md)

<table id="table_zcc_dry_mgc"><thead><tr><th>

Column

</th><th>

Indicator

</th><th>

Source plugin

</th><th>

Indicator type

</th><th>

Indicator source / Formula calculation / Additional conditions

</th></tr></thead><tbody><tr><td>

Spend

</td><td>

CPRO: Total spend - YTD

</td><td>

sn\_cpro\_dashboard

</td><td>

Automated

</td><td>

PurchaseOrder.Standard.All \(Purchase Order\)Calculation: Sum \(total\_amount\)

</td></tr><tr><td>

Spend

</td><td>

CPRO: Total Savings - YTD

</td><td>

sn\_cpro\_dashboard

</td><td>

Automated

</td><td>

PurchaseOrderLine.Standard.All \(Purchase Order Line\)

</td></tr><tr><td>

Spend

</td><td>

Purchase Order - Total Line Amount

</td><td>

sn\_spend\_pa

</td><td>

Formula

</td><td>

\[\[Order Line Revisioned Line Amount\]\] - \[\[Order Line Total Line Amount\(History Line\)\]\]

</td></tr><tr><td>

Spend

</td><td>

CPRO: Monthly Total Saving

</td><td>

sn\_cpro\_dashboard

</td><td>

Formula

</td><td>

\[\[CPRO: Total Savings - YTD / By month AVG +\]\]

</td></tr><tr><td>

Requisitions

</td><td>

Number of Open Purchase Requisition

</td><td>

sn\_spend\_pa

</td><td>

Automated

</td><td>

Source: PurchaseRequisition.Open

</td></tr><tr><td>

Requisitions

</td><td>

Number of Total \(ATF\) Purchase Requisition

</td><td>

sn\_spend\_pa

</td><td>

Automated

</td><td>

Source: PurchaseRequisition.Created.Daily

</td></tr><tr><td>

Requisitions

</td><td>

CPRO: Aging Purchase Requisitions

</td><td>

sn\_cpro\_dashboard

</td><td>

Automated

</td><td>

Source: PurchaseRequisition.Open \(Purchase Requisition\)

</td></tr><tr><td>

Requisitions

</td><td>

CPRO: Number of Total \(ATF\) Purchase Requisition Monthly

</td><td>

sn\_spend\_pa

</td><td>

Formula

</td><td>

\[\[Number of Total \(ATF\) Purchase Requisition / By month SUM +\]\]

</td></tr><tr><td>

Sourcing

</td><td>

CPRO: Overdue Sourcing Requests

</td><td>

sn\_spend\_pa

</td><td>

Formula

</td><td>

\[\[Number of Open Sourcing Request &gt; \[PSM\] Due Date Breakdown = Overdue\]\]

</td></tr><tr><td>

Sourcing

</td><td>

Number of Open Sourcing Request

</td><td>

sn\_spend\_pa

</td><td>

Automated

</td><td>

Source: SourcingRequest.Open

</td></tr><tr><td>

Negotiations

</td><td>

Number of Open Negotiations

</td><td>

sn\_spend\_pa

</td><td>

Automated

</td><td>

Source: Negotiation.Open

</td></tr><tr><td>

Negotiations

</td><td>

CPRO: Negotiation Outcomes - YTD

</td><td>

sn\_cpro\_dashboard

</td><td>

Automated

</td><td>

Source: Negotiation.Closed \(Negotiation\)

</td></tr><tr><td>

Contracts

</td><td>

CPRO: Renewing Contracts

</td><td>

sn\_spend\_pa

</td><td>

Automated

</td><td>

Source: CPRO: Renewal Contracts

</td></tr><tr><td>

Contracts

</td><td>

Number of Expiring Contracts

</td><td>

sn\_spend\_pa

</td><td>

Automated

</td><td>

Source: RequisitionToContract.Open

</td></tr></tbody>
</table>
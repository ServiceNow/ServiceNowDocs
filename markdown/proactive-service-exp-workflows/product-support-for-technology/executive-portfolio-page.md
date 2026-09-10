---
title: Executive Portfolio view
description: The Executive Portfolio page provides account teams and leadership with a real-time view of account portfolio performance. Use this page to identify at-risk revenue, track renewal readiness, monitor product adoption, and understand customer experience trends.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/proactive-service-exp-workflows/product-support-for-technology/executive-portfolio-page.html
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-08-12"
reading_time_minutes: 2
breadcrumb: [Explore, Proactive Service Experience Workflows, Product Support for Technology]
---

# Executive Portfolio view

The Executive Portfolio page provides account teams and leadership with a real-time view of account portfolio performance. Use this page to identify at-risk revenue, track renewal readiness, monitor product adoption, and understand customer experience trends.

## About the Executive Portfolio page

The Executive Portfolio page gives account teams a single, filterable view of portfolio health across revenue, renewal risk, and adoption. It shows how much revenue is retained, at risk, or shifting over time, along with upcoming renewals and recent changes in account health. It also highlights gaps in feature adoption, usage of underutilized capabilities, and progress toward full deployment. Together, these insights help leadership spot urgent risks and prioritize retention and growth efforts.

\[Omitted image "executive-portfolio-view.png"\] Alt text: Portfolio overview tab with account health distribution chart, renewal timeline, and financial metrics cards.

## Benefits

The Executive Portfolio provides the following benefits:

-   Removes fragmented data silos by combining account health, financial, and product usage in a single workspace.
-   Make faster decisions with a unified view of revenue, renewal risk, and adoption data.
-   Engage customers proactively by spotting health changes and at-risk renewals in real time.
-   Prioritize retention and growth efforts by identifying adoption gaps and underutilized capabilities early.

.

## Roles

<table id="table_pgk_wfq_fkc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_tech\_exp.executive\_portfolio\_viewer

</td><td>

Grants access to the Executive portfolio for success and sales users.**Note:** To view the sales data, you must add the portfolio role with the sales agent role \(sn\_sales\_common.sales\_agent\).

</td></tr></tbody>
</table>## Filters

Filter indicator cards by the following dimensions. Select one filter at a time.

<table id="table_wxn_sgj_fkc"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Geo

</td><td>

Filters indicator data by geography. Data from the Territory \[sn\_tp\_territory\] table Geography field.**Note:** Selection process permits only one filter at a time. However, when you select **Geo**, you can then select a region.

</td></tr><tr><td>

Region

</td><td>

Filters indicator data by region. Data from the Territory \[sn\_tp\_territory\] table Name field.

</td></tr><tr><td>

Industry

</td><td>

Filters indicator data by industry. Data from the Customer Account \[customer\_account\] table Market Segment field.

</td></tr></tbody>
</table>## Tabs

The Executive Portfolio view contains the following tabs:

<table id="table_l3t_tdq_fkc"><thead><tr><th>

Tab

</th><th>

Details

</th></tr></thead><tbody><tr><td>

Portfolio overview

</td><td>

A snapshot of revenue retention, renewal risk, and growth opportunities across the entire portfolio. For more information, see [Portfolio overview tab fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/executive-portfolio-overview-tab.md).

</td></tr><tr><td>

Financials

</td><td>

A detailed breakdown of Total Annual Recurring Revenue \(ARR\), retention rates, at-risk revenue, and quarterly revenue movement. For more information, see [Executive Portfolio Financials tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/executive-portfolio-financials-tab.md).

</td></tr><tr><td>

Adoption and health

</td><td>

A view into account health trends, feature adoption gaps, product usage, and customer satisfaction. For more information, see [Executive Portfolio Adoption and health tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/executive-portfolio-adoption-health-tab.md).

</td></tr><tr><td>

All accounts

</td><td>

A drill-down list of individual accounts underlying the portfolio-level metrics. Shows the following details:-   Annual Contract Value
-   Account Health
-   6 week health score
-   Risk Signal
-   Last touchpoint
-   Renewal date

</td></tr></tbody>
</table>## Navigation

To open the Executive portfolio page, select executive portfolio icon \(\[Omitted image "icon-executive-portfolio.png"\] Alt text: Executive Portfolio Icon.\) from the CSM/FSM Configurable Workspace or Service Operations Workspace.

**Parent Topic:**[Exploring the Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/explore-assurance-workflows.md)


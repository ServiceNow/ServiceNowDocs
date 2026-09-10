---
title: Technology Account 360
description: Use the Technology Account 360 to get a unified view of customer or partner account details combining account health, financial, product usage, and open tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/proactive-service-exp-workflows/product-support-for-technology/technology-account-360.html
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: concept
last_updated: "2026-08-12"
reading_time_minutes: 3
breadcrumb: [Explore, Proactive Service Experience Workflows, Product Support for Technology]
---

# Technology Account 360

Use the Technology Account 360 to get a unified view of customer or partner account details combining account health, financial, product usage, and open tasks.

Technology Account 360 gives insight about customer account such as information related to tasks, escalations, account health, financial, and various metrics associated with your customer's account. Sales, service and success teams can examine the details to fast track the decision making and reach a resolution faster without switching between applications.

Technology Account 360 uses role-based views so that each persona sees the data relevant to their work. Success and service users see Account 360 data through the customer service agent role, and sales users see it through the sales agent role.

## Key benefits

Technology Account 360 provides the following benefits:

-   Removes fragmented data silos by combining account health, financial, and product usage in a single workspace.
-   Supports faster decision-making and more proactive engagement for sales, service, and success personas.
-   Lays the foundation for AI-driven workflows that support account growth, retention, and value.
-   Actions to create touchpoints, escalations, and risk signals
-   Data visualizations including breakdown charts and performance indicators.

\[Omitted image "tech-account-360.png"\] Alt text: Overview tab view of Technology Account 360.

## Roles

<table id="table_pgk_wfq_fkc"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_ind\_tsm\_sdwan.app\_eng

</td><td>

Grants access to Account 360 for customer support users.

</td></tr><tr><td>

sn\_acct\_lc.customer\_success\_agent

</td><td>

Grants access to Account 360 for success and sales users.**Note:** To view the sales data, you must add the success role with the sales agent role \(sn\_sales\_common.sales\_agent\).

</td></tr></tbody>
</table>## Components

Account 360 includes the following components:

-   Account basic information such as Annual contract value, Next renewal date, Renewal ACV, and Success entitlement.
-   Tabs to view the account details such as health, financial, product adoption and open work items.
-   Contextual side panel to view the recommended next-best actions generated for the account, customer contact, team contact, and customer timeline.
-   UI actions to compose touchpoint and create escalations and risk signals.

|Tab|Details|
|---|-------|
|Overview|Touchpoints, escalations, milestones, and a daily account briefing. For more information, see [Technology Account 360 Overview tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/technology-account-360-overview-tab.md).|
|Account health|Health insights and performance indicators. For more information, see [Technology Account 360 Account health tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/technology-account-360-account-health-tab.md).|
|Financials|Financial insights, including the renewal confidence score. For more information, see [Technology Account 360 Financials tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/technology-account-360-financials-tab.md).|
|Product adoption|Onboarding and implementation records for the account, and product adoption insights. For more information, see [Technology Account 360 Product adoption tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/technology-account-360-product-adoption-tab.md).|
|Open work|Work insights, including breached and aged work items.For more information, see .[Technology Account 360 Open work tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/technology-account-360-open-work-tab.md).|

## Recommended actions

An AI-generated next-best-action panel that surfaces suggested actions for the account directly within Account 360. With the use of Recommended actions, you don't have to leave the record to determine what to do next.

Following are the key behaviors of recommended actions:

-   The panel opens even when no active recommendation exists yet.
-   Recommendation data is fetched and cached for the account, so reopening the panel doesn't trigger a fresh lookup every time.
-   The underlying logic uses the `ExecPortfolioRecommendedActions` script include and `SuccessRecommendationUtil`, and integrates with the platform's `ScriptingGeneratorFactory` pattern.
-   The panel can generate more than one recommendation per trigger, so if a single event is relevant to multiple accounts, each account receives its own suggestion.

For more information about how to use Technology Account 360, see [Reviewing customer or partner accounts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/reviewing-customer-accounts-360.md).

To customize the values of an indicator, see [Customize an indicator in the Technology Account 360 view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/customize-indicator-technology-account-360-view.md).

**Parent Topic:**[Exploring the Proactive Service Experience Workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/proactive-service-exp-workflows/product-support-for-technology/explore-assurance-workflows.md)


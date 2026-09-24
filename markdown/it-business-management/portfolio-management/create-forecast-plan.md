---
title: Legacy- Create and promote a forecast plan
description: As a portfolio manager, you can re-estimate \(forecast\) the portfolio budget for future periods based on the actual cost and changed project requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/create-forecast-plan.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Legacy- Forecast the budget for portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Create and promote a forecast plan

As a portfolio manager, you can re-estimate \(forecast\) the portfolio budget for future periods based on the actual cost and changed project requirements.

## Before you begin

**Note:** The content in this topic is applicable for customers upgrading from a previous release to Brazil. If you are a new customer, see [Scenario Planning for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio-planning-overview.md).

-   Role required: it\_portfolio\_manager
-   The **Portfolio Planning** field for the portfolio must be set to **Advanced** on the [Portfolio form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/t_CreateAPortfolio.md).
-   The [forecast period](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/forecast-period.md) for the fiscal period must be open to create the forecast plan for a portfolio. For example, the forecast period for FY17: Apr must be open to create a forecast plan in April. The PPS admin can open the forecast period for a fiscal period by navigating to **Project Administration** &gt; **Open/Close Forecast Periods**.
-   The [budget period](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/create-a-budget-period.md) for a fiscal period must be closed to open a forecast period for the corresponding fiscal period. The PPS admin can close the budget period for a fiscal period by navigating to **Project Administration** &gt; **Open/Close Budget Periods**.
-   Only one forecast period can be open at a time.

## Procedure

1.  Navigate to portfolio workbench and open the portfolio that you want to track.

2.  Click **Promote Forecast Plan** under **Step 4: Forecasting**.


## Result

-   The forecast plan for the portfolio is created and promoted for the selected forecast period. You can [re-promote the forecast plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/repromote-forecast-plan.md), if required.
-   A task with the status **Pending Approval** is created when the portfolio manager promotes the forecast plan. The status of the task is visible in Portfolio Workbench.

## What to do next

-   To view the task for the forecast plan, click the **Status** link. The finance reviews the portfolio forecast plans in the [Planning Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/financial-planning-workbench.md) and approves the plan.
-   To view a list of all the promoted forecast plans for the portfolio, click the **All Promoted Forecast Plans** link under step 4: Forecasting. The promoted forecast plans are listed for all forecast periods.
-   After the forecast plan is finalized and no further changes are expected, the forecast period must be closed.

**Parent Topic:**[Legacy- Forecast the budget for portfolio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/forecast-plan-for-portfolio.md)


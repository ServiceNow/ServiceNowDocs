---
title: Legacy- Portfolio budget object configuration
description: The planned cost of cost plans in portfolio when promoted by portfolio managers are converted to budget plans. The base system has a seeded read-only budget definition Portfolio Budget Planning Process used for the promotion of portfolio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-management/portfolio\_budget\_object\_configuration.html
release: brazil
product: Portfolio Management
classification: portfolio-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Legacy- View promoted portfolio budget plans in the planning workbench, Legacy- Plan the portfolio, Legacy portfolio workbench, Portfolio Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Legacy- Portfolio budget object configuration

The planned cost of cost plans in portfolio when promoted by portfolio managers are converted to budget plans. The base system has a seeded read-only budget definition Portfolio Budget Planning Process used for the promotion of portfolio.

**Note:** The content in this topic is applicable for customers upgrading from a previous release to Brazil. If you are a new customer, see [Scenario Planning for PPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/portfolio-planning-overview.md).

\[Omitted image "portfolio\_budget\_object\_configuration.png"\] Alt text: screenshot for Portfolio Budget Planning Process

The granularity of the promoted budget object is defined in the Define Structure step of the Portfolio Budget Planning Process budget definition. By default, the granularity of Project Definition is **Portfolio**, Project or Demand \(**Portfolio Task**\), and **Account Number**.

\[Omitted image "portfolio\_budget\_object\_configuration1.png"\] Alt text: screenshot for Define Structure step

If your organization needs more attributes \(such as cost center and cost plan name\) in the promoted portfolio budget object, you can define the additional mappings in the cost plan data source. Set up by dot walking the required attribute from the cost plan object. After the mapping is done, select the attribute in Define Structure of Portfolio Budget Planning Process and save it.

The promoted budget would include the selected attribute with **Portfolio**, Project or Demand \(**Portfolio Task**\), and **Account Number**. This attribute would also be visible in Portfolio Workbench.

**Note:** **GL Account Number** is automatically considered as one of the template columns.

\[Omitted image "portfolio\_budget\_object\_configuration2.png"\] Alt text: screenshot for Planning Data Field Source maps

## Additional columns in Workbench

While reviewing the promoted portfolios, you can pull the additional dot walked columns to workbench for visibility. Use the Portfolio Budget Planning Process Define structure to pull in the additional dot walked column, such as Portfolio Manager, and save the configuration. Once saved, the column is visible on the workbench.

\[Omitted image "additional\_columns\_in\_workbench1.png"\] Alt text: screenshot for Additional columns

\[Omitted image "additional\_columns\_in\_workbench2.png"\] Alt text: screenshot for Define Structure step

\[Omitted image "additional\_columns\_in\_workbench3.png"\] Alt text: screenshot for Plan View

**Parent Topic:**[Legacy- View promoted portfolio budget plans in the planning workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-management/view-ppm-portfolio-budget-plan-in-planning-workbench.md)


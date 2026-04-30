---
title: Success report dashboard
description: Get an overall view of all your engagement and team status overview, risk indicators, onboarding and adoption insights, and expansion and renewal metrics.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Success report dashboard overview, Customer success, Use, Customer Success Management]
---

# Success report dashboard

Get an overall view of all your engagement and team status overview, risk indicators, onboarding and adoption insights, and expansion and renewal metrics.

To view this page, follow these steps:

1.  Login as a user with either the `sn_acct_lc.success_manager` and `sn_acct_lc_customer_success_agent` roles.
2.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** to view the Success report page.

**Note:**

-   The engagements listed on the success report dashboard are based on the hierarchy of the logged in user. Users with the **sn\_acct\_lc.success\_manager** role can see an aggregate view of all engagements handled by all customer success managers in the hierarchy. Users with the **sn\_acct\_lc\_customer\_success\_agent** role can see an aggregate view of all their assigned engagements. For more details, see [Success report dashboard overview](account-lifecycle-success-report-overview.md).
-   Select filters from the following drop down lists and click **Apply** to narrow the list of engagements displayed:
    -   Contract values: Select one or more contract values from the drop down list. The local currency is automatically selected based on your system settings. The contract value ranges are based on the following properties in the **TechOnbConstants** script include:
        -   TechOnbConstants.CONTRACT\_VALUES\_ID
        -   TechOnbConstants.CONTRACT\_VALUES
    -   Customer success managers: The list of users displayed here is based on the role of the logged in user.
        -   Customer success agent: In this case, only the user who has logged in will be displayed.
        -   Customer success manager: All the customer success agents in the hierarchy are displayed.
    -   Industries: The list displayed is based on the customer accounts of all the engagements managed by customer success manager of the logged in user.

The Success report page contains the following tabs:

-   [Overview](account-lifecycle-success-report.md#section_iz5_3nl_kfc): Provides an overview of the team health and engagement metrics.
-   [Risk](account-lifecycle-success-report.md#section_wcb_g4l_kfc): Identifies potential issues that can impact engagement health.
-   [Adoption](account-lifecycle-success-report.md#section_ds3_bcy_lfc): Provides details on customer progress on onboarding and product adoption.
-   [Renewal](account-lifecycle-success-report.md#section_kby_w2y_lfc): Lists key metrics related to revenue growth opportunities and contract renewals.

![Success report landing page.](../image/account-lifecycle-success-report.png)

## Overview \(Success report\)

This tab provides a high-level overview of the success portfolio. You can click on any of the sections in this page to drill down to the Details page. It includes the following details:

-   Total engagements: Total number of engagements managed by the customer success manager.
-   YTD new engagements: The number of new engagements as of the current year.
-   Average engagements per CSM: The average number of engagements per customer success manager in the success portfolio.
-   Engagements with escalations: Shows a list of engagements with escalated accounts.
-   Engagements with upcoming QBRs: Shows a list of engagements with upcoming QBRs.
-   Engagement health by stage: Shows engagements grouped by the stage in the engagement lifecycle \(onboarding, adoption, and so on\).
-   Success manager tasks: Shows the tasks handled by the success managers grouped by status \(in progress, overdue, and so on\).

![Success report overview](../image/success-portfolio-over.png)

## Risk

This tab provides an identification of potential issues that could impact engagement metrics. It includes the following details:

-   Total contract value at risk: Total value of contract that has been impacted for all active risk signals
-   Red, yellow engagements: The number of engagements with a red or yellow perceived health score.
-   Renewals due soon in poor health: The number of engagements with a poor health score that are due for renewal.
-   Engagements with no touchpoints in 90 days: Engagements which have no upcoming touchpoints in the next 90 days.
-   Active risk signals: Shows the number of risk signals.
-   Top 5 Risk Signal Indicators: The top risk signal categories such as low adoption, poor health, and so on.
-   Risk signals by scope: Risk signals grouped by scope or state of the engagement such as adoption, onboarding, and so on.
-   Risk signals by probability: Risk signals grouped by probability such high, moderate, low, and so on.

![Success report risk](../image/success-portfolio-risk.png)

## Adoption

This tab shows the current customer adoption status. It includes the following details:

-   Engagements with overdue go-live date: Engagements with overdue go-live dates.
-   Engagements with active onboarding: List of engagements that are in the on-boarding stage of the engagement life cycle.
-   Engagements due to go-live in 30 days: List of all engagements that are due to go-live in 30 days.
-   Engagements with no success objectives: Engagements for which no success objectives have been defined.
-   Engagements with &gt;80% objective completion: List of engagements for which more than 80% of the success objectives have been completed.
-   Success objective progress: Success objectives grouped by state such as new, on-track, at risk, completed, and so on.
-   Engagements with low adoption score products: List of products with a low adoption score and the associated customer and business priority. See [Product adoption and capability usage](account-lifecycle-product-adopt.md) for details.

![Success report adoption](../image/success-portfolio-adopt.png)

## Renewal

This tab shows the renewal details for all contracts associated with the engagements. It includes the following details:

-   Engagements with renewals due in 90 days: List of engagements with contracts that are due for renewal in 90 days.
-   Opened renewals: List of all active or expired contracts where state equals:
    -   Under review
    -   Awaiting review
    -   Active and extension approved
-   Contracts on extension: Contracts where Extension is Approved and State is Active.
-   Renewals by stages: Renewals grouped by stage which can be one of the following:
    -   Awaiting review
    -   Renewal approved
    -   Renewal rejected
    -   Under review
-   YTD renewals and losses by month: Monthly breakdown of renewed and rejected contracts, year-to-date.

    **Note:** The date used to plot the x-axis on the graph is based on one of the following:

    -   If Sales Customer Relationship Management is installed, an opportunity is created for each contract. For opportunities with type **Renew**, the stage of the contract is set to **Closed won** or **Closed lost** indicating whether the contract had been renewed. The Actual Closed Date in the Opportunity record is used to plot the X axis. For more details, see [Opportunity Management](https://www.servicenow.com/docs/access?context=opportunity-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US).
    -   Date specified in the **Renewal finalized on** field in the Contracts table. The Renewals won and Renewals lost bar charts show the month in which the renewal was either approved or rejected.
-   Engagements with lost contracts: List of engagements with contracts that were rejected or not renewed.
-   YTD total contract value by month: Monthly breakdown of total contract value, year-to-date.

![Success report renewal](../image/success-portfolio-renewal.png)

**Parent Topic:**[Success report dashboard overview](account-lifecycle-success-report-overview.md)


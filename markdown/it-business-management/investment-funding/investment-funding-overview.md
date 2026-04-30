---
title: Investment Funding
description: ServiceNow Investment Funding enables you to plan and manage investments by allocating funds to investment entities such as Business Units, Products, Teams, and the like. Prioritize your investments based on business needs and strategic objectives of your organization.
locale: en-US
release: yokohama
product: Investment Funding
classification: investment-funding
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [Investment funding, Investments, Funds, Top-down funding, Bottom-up funding, Funding process]
breadcrumb: [Strategic Portfolio Management]
---

# Investment Funding

ServiceNow® Investment Funding enables you to plan and manage investments by allocating funds to investment entities such as Business Units, Products, Teams, and the like. Prioritize your investments based on business needs and strategic objectives of your organization.

You can use the Investment Funding \(sn\_invst\_pln\) application to do the following:

-   Create investments for entities.
-   Allocate funds to an investment to meet a business requirement or strategic objective.
-   Request funds from one or more funding sources to achieve business goals.

**Note:** Starting with the Rome release, Investment Funding will be found in the ServiceNow Store. The legacy plugins \(com.snc.investment\_planning, com.snc.investment\_planning\_pmo\) will be prepared for future deprecation in September 2022. The plugins will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

## Investment entities and investments

An investment contains information about funds, costs, benefits, business case, and goals. Use investments to allocate or request funds to meet defined business goals. An investment is associated to an investment entity.

An investment entity is a transaction table for funding. For example, you can create investment entities for records such as Projects, Teams, Business Units, Epics, and Portfolios.

Keeping the investment and investment entity separate provides the following advantages:

-   Your work activities are separate from the funding.
-   You can fund the same entity for different periods until the investment goals are met.

## Generic investments

A generic investment is an investment that is tied an owner without being associated to any entity. You can fund any entity or other generic investment from a generic investment.

For example, as the CEO of a company you might want to set aside some funds for a training or research initiative and there might not be a transaction table to enable such an entity. You could then create a generic entity to fund the investment.

## Top-down and bottom-up funding

In top-down funding, you distribute funds to investments based on business goals or as part of a business strategy.

In bottom-up funding, you request funds for your investments from one or more funding sources.

Investment Funding enables you to manage funds for both funding approaches.

## Domain separation in Investment Funding

[Domain separation](domain-separation-investment-funding.md) provides complete data isolation for domain-specific users. Investment Funding is compliant with domain separation at the **Data only** level.

-   **[Install Investment Funding](../task/activate-investment-funding.md)**  
You can install the Investment Funding application \(sn\_invst\_pln\_v2\) from ServiceNow Store if you have the admin role.
-   **[Upgrading legacy Investment Funding to Store application](upgrading-legacy-investment-funding-to-store.md)**  
If you are upgrading from the legacy Investment Funding, post installation of the Investment Funding application, you can migrate your existing data to the ServiceNow Store application tables. Also, you must update the reference tables for the **Investment** and **Funding Entity** fields to the ServiceNow Store application tables.
-   **[Investment Funding administration](investment-funding-administration.md)**  
The Investment Funding application requires you to do some initial administrative tasks for it to be fully functional.
-   **[Create a top-level investment](../task/create-top-level-investment.md)**  
Create a top-level investment for the investment entity record for which you want to receive and allocate funds.
-   **[Create an investment](../task/create-investment.md)**  
Create an investment to fund a target.
-   **[Co-owners for an investment](co-owner-for-investments.md)**  
Investment co-owners manage, request, and allocate funds on your behalf to the investments that you own. The co-owner has the same rights and permissions as the owner.
-   **[Request funds for an investment](../task/request-funds-for-investment.md)**  
Request funds from a funding source for your investment.
-   **[Plan fund allocations for investments](../task/plan-fund-allocations-for-investments.md)**  
Plan your fund allocations if you are not yet ready to finalize the allocation of your funds.
-   **[Allocate funds to an investment](../task/allocate-funds-to-investment.md)**  
Allocate funds to investments based on your business goals and available funds.
-   **[Enter actual spends for an investment](../task/enter-actuals-for-investment.md)**  
Enter actual spends for your investments to track fund utilization.
-   **[Reject a fund request](../task/reject-fund-requests.md)**  
You can reject an incoming fund request based on your business priorities or if you do not have sufficient funds.
-   **[Review the use of your funds](../task/track-funds.md)**  
Review the flow of your funds from your investment to other investments to make an informed decision when you allocate or request funds.
-   **[View past funding details](../task/view-past-funding-details.md)**  
View the past funding details of your investments.
-   **[Domain separation and Investment Funding](domain-separation-investment-funding.md)**  
Domain separation is supported in Investment Funding. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[Strategic Portfolio Management](../../it-business-management/reference/r_ITBusinessManagement.md)


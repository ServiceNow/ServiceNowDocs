---
title: Investment Funding release notes
description: Version history for the Investment Funding on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-investment-funding.html
release: store
topic_type: reference
last_updated: "2024-05-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Investment Funding release notes

Version history for the Investment Funding on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.1.1 - May 2024**
    -   Deprecated the following:
        -   'Investment Funding' Dashboard from Platform Analytics Dashboards.
        -   'View Past Funding Details' option from the 'Allocate Funds' page for an investment.
-   **Version 1.1.0 - February 2024**

    Fixed: Issue with Generic Bucket missing from investment entities in Investment Funding v2 during upgrade.

-   **Version 1.4.2 - July 2023**

    Fixed: Bug fixes for seamless experience to use the application.

-   **Version 1.4.1 - May 2023**

    Fixes: An issue preventing users from submitting funds for other investments. This occurred when a negative funding record existed for an investment, which exceeded the total available funds for that investment in the planned state.

-   **Version 1.4.0 - August 2022**
    -   Investment owners can add other users as co-owners to delegate the actions to Add funds, Request/Allocate Funds to their investments
    -   Better usability as users can see an indicator to differentiate the investments they own/co-own/have view-only permissions to in Top Level Investments and My Funds screens
-   **Version 1.3.0 - May 2022**
    -   Fixed:
        -   On migrating from legacy Investment Funding to Store app, cost plans and benefit plans created for Projects are being attached to Demands, for Projects created from Demands.
        -   On migrating from legacy Investment Funding to Store app, some of the Investment entity fields and roles are not migrated.
        -   In View/Request funds tab, Source name is not displayed completely.
        -   In Allocate Funds tab, details such as State, Number, Phase, Status, Business Unit etc., of the items being funded are not being displayed before any funds are allocated to them.
        -   In Allocate Funds tab, right click on items being funded doesn't show any options before any funds are allocated to them.
        -   For Investment Fund entities of type 'Generic bucket', selecting 'Reject' option on items which are allocated with funds is not responsive.
        -   For users with 'investment user' role, who doesn't have read access to the 'Active' field in sys\_user table, Financials tab in Project workspace doesn't load.
        -   Fixed an incorrect ACL for sn\_invst\_pln\_invst\_funding\_configuration.
-   **Version 1.1.0 - July 2021**

    Changed: Actuals from projects and demands are now automatically added to the corresponding investments when there is a single funded source.

-   **Version 1.0.1 - July 2021**
    -   New:
        -   The Investment Funding application and all its related components have been moved to the ServiceNow store.
        -   The Investment Funding \(com.snc.investment\_planning\) and Investment Funding for PPM \(com.snc.investment\_planning\_pmo\) plugins have been merged to become a single plugin called Investment Funding \(com.snc.investment\_funding\).


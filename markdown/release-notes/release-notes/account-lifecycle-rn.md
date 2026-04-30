---
title: Customer Success Management release notes
description: The ServiceNow Customer Success Management application helps you to streamline your onboarding process, define and track objectives and outcomes, identify and mitigate risks, and increase renewal rates. Customer Success Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Customer Success Management release notes

The ServiceNow® Customer Success Management application helps you to streamline your onboarding process, define and track objectives and outcomes, identify and mitigate risks, and increase renewal rates. Customer Success Management was enhanced and updated in the Zurich release.

## Customer Success Management highlights for the Zurich release

-   Account Lifecycle Events has been renamed to Customer Success Management.
-   Enable managers to see a high-level aggregate view of their entire customer portfolio.
-   Monitor adoption scores for sold products and track implementation progress for customer engagements.
-   View the engagement hierarchy and timeline of events.
-   Use the new metrics data source to calculate metric values dynamically based on the weighted sums of other metrics.
-   View the detailed information of risk level records in the risk occurrence timeline.
-   The activity stream component displays a list of the activities occurring on a risk signal and issue record.
-   The **Related Items** tab provides access to the Risk Signal and Issue related lists.
-   Determine the engagement health score from the Calculated data source.
-   Retrieve data from internal and external tables with the Table type data source.

See [Customer Success Management](https://www.servicenow.com/docs/access?context=account-lifecycle-events-landing&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US) for more information.

**Important:** Customer Success Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Calculate health score](https://www.servicenow.com/docs/access?context=account-lifecycle-setup-health-defn&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Starting with Customer Success Management 5.3.11, you can use the **Calculated** metric data source to determine the health score for an engagement. If you are upgrading from Customer Success Management 5.3.10 or earlier versions, you must run the `Set health migration status` script to enable the health score calculation using this data source.


-   **[Define a table data source](https://www.servicenow.com/docs/access?context=account-lifecycle-define-data-source-table&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Starting with Customer Success Management 5.3.11, you can use the **Table** type data source to retrieve and analyze data from internal and external tables. To retrieve data from external sources, you must install the Workflow Data Fabric Hub application and create data fabric tables.


-   **[Risk and issues page](https://www.servicenow.com/docs/access?context=account-lifecycle-risk-issues-page&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Use the risk timeline visualization to manage the risk occurrences.


-   **[Granular admin roles](https://www.servicenow.com/docs/access?context=account-lifecycle-success-roles&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    The granular admin role enables developers and administrators to complete administrative configuration tasks for Customer Success Management without requiring the full admin role.


-   **[Read-only field enhancements](https://www.servicenow.com/docs/access?context=account-lifecycle-read-only&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Read-only field protections have been moved from the client side to the server side. This move prevents users from updating read-only fields through client-side methods.


-   **[Success report dashboard](https://www.servicenow.com/docs/access?context=account-lifecycle-success-report-overview&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Use the Success report dashboard to see the overall view of all the engagements under your hierarchy and manage your entire customer portfolio. Monitor engagement metrics, risk indicators, and get insights into onboarding and adoption status, risk indicators, onboarding and adoption insights, and expansion and renewal metrics.


-   **[Product adoption and usage](https://www.servicenow.com/docs/access?context=account-lifecycle-product-adopt&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Measure product adoption trends and proactively guide users to achieve desired outcomes using products and services that have been purchased. Identify active and power users and areas where additional training or support is required due to low engagement.


-   **[Implementation record](https://www.servicenow.com/docs/access?context=account-lifecycle-imp-record&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Track the progress of a partner or customer implementing a product or a service. Get a centralized view of the implementation status, identify risks, and run playbooks to mitigate issues.


-   **[Engagement hierarchy](https://www.servicenow.com/docs/access?context=account-lifecycle-view-engage&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    View aggregate hierarchical data for an engagement. Make informed decisions, improve customer satisfaction through detailed tracking, identify risks early, and help prevent escalations.


-   **[Engagement timeline](https://www.servicenow.com/docs/access?context=account-lifecycle-touchpoint-planner&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    View a chronological list of critical events related to an engagement. Review timelines to recall past events, customer interactions, and identify any issues.


-   **[Contextual color bands](https://www.servicenow.com/docs/access?context=account-lifecycle-setup-color-banding&version=zurich&pubname=zurich-acct-lifecycle-events&ft:locale=en-US)**

    Associate thresholds and visual representations to health metric data. View product adoption and usage information relative to a specific product.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Activation information

Install Customer Success Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    The Customer Service Management application enables you to automate your onboarding and case monitoring processes and provides service agents with visibility into the customer systems and tools that you need to deliver proactive services to your customers.


-   **[Service Exchange](https://www.servicenow.com/docs/access?context=tmt-service-bridge-both-landing-page&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)**

    ServiceNow® Service Exchange connects multiple ServiceNow instances to provide seamless support and service experiences across the ecosystem, from enterprise customers to suppliers and system integrators. Service Exchange provides a frictionless experience that enables efficient collaboration and request processing while giving users the convenience of working in their own ServiceNow instance.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](technology-industry-rn-landing.md)


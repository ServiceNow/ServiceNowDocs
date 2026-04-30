---
title: Environmental, Social, and Governance Management release notes
description: The ServiceNow ESG Management application helps you to manage all your environmental, social, and governance \(ESG\) commitments. ESG Management was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 4
---

# Environmental, Social, and Governance Management release notes

The ServiceNow® ESG Management application helps you to manage all your environmental, social, and governance \(ESG\) commitments. ESG Management was enhanced and updated in the Xanadu release.

## ESG Management highlights for the Xanadu release

-   Track Scope 3 emissions from your value chain to gain knowledge of your environmental impact and promote compliance with evolving regulations.
-   Create fiscal calendars to accommodate your organization’s unique fiscal calendar, providing the flexibility to collect and report data according to the defined fiscal calendars.
-   Use the emission factors content in the ESG content accelerator.
-   Enable ESG administrators to define either a simple approval flow or an advanced approval flow for all the metrics and metric definitions.
-   Address off-cycle requests to collect data for existing metric definitions and metrics by creating ad hoc metric data tasks on manual metrics.

See [Environmental, Social, and Governance Management](https://www.servicenow.com/docs/access?context=esg-landing-page&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US) for more information.

**Important:** ESG Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Xanadu release

-   **[Track scope 3 emissions](https://www.servicenow.com/docs/access?context=scope-3-dashboard&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    Track Scope 3 emissions using the Scope 3 dashboard to fully grasp and manage your organization's environmental impact. These emissions constitute the largest part of your greenhouse gas output, stemming from indirect sources. This comprehensive understanding aids in regulatory compliance, and obtaining full carbon footprint disclosures. After you identify your scope 3 emission sources, you can take action to mitigate the largest sources of indirect emissions.

-   **[View emission factors in ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    Use the ESG content accelerator to automatically obtain the emission factors that are published by the standard sources. Emission factors are coefficients that quantify the emissions produced per unit of activity, material, or energy consumption. They’re crucial for calculating the amount of greenhouse gases \(GHGs\) or pollutants emitted into the atmosphere based on various activities.

-   **[Create fiscal calendars to collect metrics from different geographical locations](https://www.servicenow.com/docs/access?context=enable-custom-fiscal-year&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    Collect, aggregate, and report data according to your fiscal calendars that could be different from the standard Gregorian calendar. Many global organizations might have operations in different countries that could follow their own fiscal calendars. This feature enables the entities in other locations to collect data according to their own fiscal calendars.

-   **[Choose the approval flow for metrics](https://www.servicenow.com/docs/access?context=components-installed-with-esg&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    Set the sn\_esg.metric\_approval property to use either a simple approval flow for your metrics and metric definitions or use the GRC: Approver Configurator to define multiple levels of approvals based on the business rule definitions. This property has two choices.

    If you choose the **Simple** option, the Approval section is enabled both on the manual metric definition form and within the metrics. Using this section, you can designate approvers directly on the metric definition form. This option has a single level of approval.

    If you choose the **Advanced** option, the Approval section is unavailable on the manual metric definition form and within the metrics, helping to prevent you from assigning approvers there. Instead, approval can be obtained by setting the approval conditions, tables, and approvers in the GRC: Approver Configurator application. This application also enables you to define multiple levels of approvals.

-   **[Create ad hoc metric data tasks](https://www.servicenow.com/docs/access?context=create-an-adhoc-metric-data-task&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    Handle off-cycle requests for up-to-date information on existing metric definitions and metrics by creating ad hoc metric data tasks. These tasks address off-cycle requests and provide the latest information.

-   **[Metric data table](https://www.servicenow.com/docs/access?context=metric-data-table&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    Use the enhanced filters on the metric data table to filter your tasks. The filters help to show only the relevant and open tasks for data owners and approvers.

-   **[Identify the energy usage and emission of every asset](https://www.servicenow.com/docs/access?context=managing-sustainable-it&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    Use the Sustainable IT dashboard to explore models within a specific category and view the energy consumption of each asset model and all its assets, listed in descending order. This functionality provides deeper insights into your energy usage, helping you identify the models that are in use and are consuming the most energy.


## UI changes

-   **[Emission factor library](https://www.servicenow.com/docs/access?context=set-up-the-emission-factor-library&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    The emission factors are now available in the ESG Workspace.


## Changed in this release

-   **[ESG program manager role enhanced](https://www.servicenow.com/docs/access?context=components-installed-with-esg&version=xanadu&pubname=xanadu-environmental-social-governance&ft:locale=en-US)**

    The ESG program manager \(sn\_esg.program\_manager\) can now create, read, update, and delete emission factors.

-   **Changes in the metric tables**

    Enhanced the following metric related tables with read access control lists \(ACLs\):

    -   Metric definition
    -   Metric
    -   Metric data
    -   Metric data task
    -   Metric data task url
    With this change, the following changes are in effect:

    -   Metric level Approver user or Approver group: This means that the specified user or group designated as the approver can access only the particular metric and the tables specified for which they are the approver.
    -   Multi-level approval: This means that the specified user or group designated as the approver can access only those records in the metric related tables for which they are the approver.
    -   Enable enterprise owners to access metric records: This means that an enterprise owner can access any metric related record.

## Deprecations

-   Starting with the Xanadu release, the Global Reporting Initiative \(GRI\) content accelerator is deprecated. It will be hidden and no longer activated on new instances but will continue to be supported. The ESG content accelerator application provides the latest experience for this functionality.
-   Starting with the Xanadu release, the Sustainability Accounting Standards Board \(SASB\) content accelerator is deprecated. It will be hidden and no longer activated on new instances but will continue to be supported. The ESG content accelerator application provides the latest experience for this functionality.

## Activation information

Install ESG Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Features and changes by product](../new-features-changes.md)


---
title: Domain separation and Safe Workplace suite
description: The Safe Workplace suite applications support domain separation at the Basic level with the exception of Safe Workplace Dashboard.
locale: en-US
release: xanadu
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Safe Workplace, Health and Safety, Employee Service Management]
---

# Domain separation and Safe Workplace suite

The Safe Workplace suite applications support domain separation at the Basic level with the exception of Safe Workplace Dashboard.

With domain separation, you can separate data, processes, and administrative tasks into logical groupings called domains. You can then control aspects in each domain, including what users can see or whether they can access the data.

## Domain separation support

ServiceNow applications that support domain separation might support the separation of data and data routing only, have advanced business logic separation, or support customer-level administration of the application. ServiceNow applications are defined with incremental support levels from the perspective of actual use cases and the people who use them.

-   **Basic**
    -   Data is domain-separated.
    -   Logic exists to ensure proper data routing, caching, rollups, and aggregations.
    -   Global configuration is operational for multiple tenants
-   **Standard**
    -   Application properties are domain-aware as needed.
    -   Business logic can be domain-separated by the instance owner per tenant.
-   **Enhanced**: Data-driven process enables failsafe configuration by tenants through the UI to drive business logic.

For more detail on the support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works in Safe Workplace applications

The following applications use the Safe Workplace domain table:

-   Contact Tracing
-   Health and Safety Testing
-   Emergency Outreach \(Daily Contact Logs, Privacy Consent, and Privacy Consent \(common\)\)
-   Emergency Exposure Management

Admins must install the [Domain separation plugin](https://www.servicenow.com/docs/access?context=t_ActivateDomainSeparation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)before working with these application tables. Most of those tables contain a **sys\_domain** field so they are able to be domain-separated if they have data that needs to be partitioned by domain.

-   Core domain table: Included in the [Safe Workplace plugin](../../human-resources/concept/safe-workplace.md) is an sn\_imt\_core\_domain table. Domains in this table are iterated when scheduled jobs run.
-   Property table: The sn\_imt\_core\_property table extends the sys\_properties table and adds a sys\_domain field. Adding that field allows sys\_properties values to be overridden for a domain.

**Note:** Values are handled differently for `password2`​ fields than for other property types. Therefore, the value displays as blank in the domain-separated properties list view.

The following tables do not have the sys\_domain field:

-   app-imt-checkin

    -   sn\_imt\_checkin\_outreach\_sysauto\_script \(extends sysauto\_script\)
    -   sn\_imt\_checkin\_response\_criteria
    -   sn\_imt\_checkin\_response\_option\_for\_health
    -   sn\_imt\_checkin\_response\_option\_survey
    -   sn\_imt\_checkin\_response\_script
-   app-imt-diagnosis: task\_compliance\_result
-   app-imt-tracing

    -   sn\_imt\_tracing\_wifi\_access\_register\_job
    -   sn\_imt\_tracing\_wifi\_access\_register\_stage
-   app-imt-core: sn\_imt\_core\_sysauto\_script \(extends sysauto\_script\)

Scheduled jobs in applications with this level of domain separation run separately for each domain in the table. Scheduled jobs use the core table as the domain source table, and the **Domain Iterator** check box is automatically enabled by default when domain separation is installed. When the **Domain Iterator** option is enabled, the job can run in multiple domains.

The **Domain Source Table** value is also set to Safe Workplace Domains by default. If you don't see the tables, verify that the **Domain Iterator** and Safe Workplace Domains settings are selected, and refresh the instance.

![Domain iterator option selected in the Employee Readiness Core Scheduled Script Execution form.](../images/ds-iterator-checkbox.png "Domain iterator option selected in the Employee Readiness Core Scheduled Script Execution form")

## Parent-child domains

Domains that also contain a sub-domain or “child” domain are not supported in these applications. Running a job in a parent domain that has a child would mean running the job twice and thus processing the data more than once. You could add a parent domain or add just the child domain but not both.

## Working with domain-separated properties in the Safe Workplace Suite

When the Domain separation plugin is installed and you navigate to the Properties page in any of the four Safe Workplace domain-separated applications, their properties do not display by default. You must override properties for a domain before they appear in the list.

![Domain-separated properties list with no properties displaying.](../images/ds-properties-none.png "Domain-separated properties list with no properties displaying")

To display the properties, click **New** on the Properties page. In the form that creates a new domain-separated property, search in the reference field for the property you would like to override. Enter a specific prefix to narrow your search:

-   `sn_imt_core` for Employee Readiness Core
-   `sn_imt_diagnosis` for Emergency Exposure Management
-   `sn_imt_health_testing` for Health and Safety Testing
-   `sn_imt_tracing` for Contact Tracing

![Entering a prefix in the Property field to narrow the search.](../images/ds-search-prefix.png "Entering a prefix in the Property field to narrow the search")

The properties display with a full description of the overrides.

![System Properties list showing the property overrides.](../images/ds-prop-overrides.png "System Properties list showing the property overrides")

After you create your domain-separated property override, the form displays the domain-separated properties.

![List showing the domain-separated properties.](../images/ds-properties-list.png "List showing the domain-separated properties")

You can navigate back to the record form by selecting a property name in the list.

## Property functions

Learn more about how these properties function in the following topics:

-   [Health and Safety Testing properties](../../health-safety-testing/task/configure-health-safety-testing.md#)
-   [Contact Tracing properties](../../contact-tracing/task/configure-contact-tracing-properties.md)
-   [System properties for tracing systems in Emergency Exposure Management](../../business-continuity/reference/list-of-tracing-system-sys-properties.md)
-   [Employee Health and Safety Status properties](../../employee-readiness-core/task/config-emp-core-properties.md)

**Parent Topic:**[Safe Workplace](../../human-resources/concept/safe-workplace.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)


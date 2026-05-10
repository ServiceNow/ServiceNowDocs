---
title: Domain separation and Reporting
description: Domain separation is supported in reporting and relates to report creation and administration. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Domain separation and Reporting

Domain separation is supported in reporting and relates to report creation and administration. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Activation

To activate the domain separation plugin, see [Request domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_ActivateDomainSeparation.md).

## How domain separation works in Reporting

In Reporting, separated data includes report designs and report content. A report defined at the global level is visible to users in all child domains.

-   Reports created in the TOP domain are visible to users in the Joe's Company domain but not in the HR, CS, and IT child domains of Joe's Company.
-   Reports created in either the IT, CS, or HR child domains aren’t visible to users in the other child domains, but they are visible to users in the parent Joe's Company domain.
-   Reports created in the parent \(Joe's Company\) domain are available only to users in that domain, but not to users in the child domains.

![List of company departments in separate domains including IT, CS, and HR. IT, CS, and HR are child domains of Joe's Company.](../image/domains-list-example.png)

If you create a report in one domain and copy it to another, the report structure remains the same, but the report data is adjusted for the domain. For example, an Active Incident report shows all active incidents to a user in the parent domain, but only IT incidents to a user in the IT domain.

-   **[Enable domain separation on reports](../task/t_EnsureDomainSepOnAReport.md)**  
Activate the domain separation plugin to enable reports to display content based on data, rules, and settings from the logged-on user domain.

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

**Related topics**  


[Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md)

[Understanding domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparation.md)


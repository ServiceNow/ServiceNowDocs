---
title: Domain separation and Legal Service Delivery
description: Domain separation is supported for applications in Legal Service Delivery. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/legal-service-delivery/legal-domain-separation.html
release: zurich
product: Legal Service Delivery
classification: legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Domain separation and Legal Service Delivery

Domain separation is supported for applications in Legal Service Delivery. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Legal Service Delivery overview

Legal Service Delivery includes the following applications:

-   Legal Request Management
-   Legal Matter Management
-   [Gifts and Entertainment Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-gifts-and-entertainment/lsd-ge-landing-page.md)
-   Legal Conflict of Interest
-   Legal Digital Forensics
-   [Legal Invention Disclosure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-invention-disclosure/legal-invention-disclosure-landing.md)
-   [Legal Investigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-investigations/legal-investigations-landing-page.md)
-   Legal Simple Contracts
-   [Legal Simple Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-simple-privacy/legal-simple-privacy-landing-page.md)
-   Legal Stock Preclearance

All tables installed with the following applications can be domain-separated:

-   Legal Request Management
-   Legal Matter Management
-   [Gifts and Entertainment Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-gifts-and-entertainment/lsd-ge-landing-page.md)
-   Legal Conflict of Interest
-   Legal Digital Forensics
-   [Legal Invention Disclosure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-invention-disclosure/legal-invention-disclosure-landing.md)
-   [Legal Investigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-investigations/legal-investigations-landing-page.md)
-   Legal Simple Contracts
-   [Legal Simple Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/legal-simple-privacy/legal-simple-privacy-landing-page.md)
-   Legal Stock Preclearance

## How domain separation works in Legal Service Delivery

-   If an employee submits a legal service request, the request can be assigned to legal department users who are in the same domain as the employee.
-   Lawyers or paralegal staff can work only on those legal requests that have been created within the domain that they belong to.

**Related topics**  


[bundle-psec.domain-sep-landing-page]


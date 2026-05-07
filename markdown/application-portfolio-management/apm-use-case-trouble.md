---
title: Enterprise Architecture considerations
description: Consider these points while implementing the CSDM framework.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Enterprise Architecture and CSDM framework, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Enterprise Architecture considerations

Consider these points while implementing the CSDM framework.

-   Business services are what IT provides to the customer. A business service is a service type that is published to business users. A business service typically implements one or more business capabilities.

    Usually, business users order business services. Business users can select the desired offering and service commitment levels via the Service Catalog. For example, procurement, shipping, and finance.

    -   A business service is an operational CI.
    -   A business service must be a one-level service and not a hierarchy of business services.
    -   A business service can be used for impact in Incident, Problem, and Change and for approvals for Change.
    -   A business service must be focused on the consumer or seller.
-   A business capability is a high-level capability that supports a business model or fulfills a mission for your organization.

    A business capability typically describes a specific task that achieves one or more business outcomes. Business capabilities are often listed as verbs \(for example, manage financials or provide IT support services\). You can use business capabilities to rationalize and prioritize the cost of business applications and business services.

-   Using Technology Portfolio Management: The Software Asset Management Foundation plugin provides life-cycle data that Technology Portfolio Management uses. However, you can manage that data manually or get it from another source. Both products share the underlying tables, but are independent and you can use them separately.
-   For information about managing your application portfolio, see [Application Portfolio Management - Inventory Best Practices](https://community.servicenow.com/community?id=community_question&sys_id=8eb947e5db5cdbc01dcaf3231f96199f).
-   Applications and business applications use different tables and represent different elements.
    -   **Business application**
        -   Uses the Business Application table \[cmdb\_ci\_Business\_App\].
        -   Represents the single, logical, construct of the application that comprises application service, environment, software, and hardware in use.
    -   **Application**
        -   Uses the Application table \[cmdb\_ci\_appl\].
        -   Represents the specific version of software in use on a server \(often populated by Discovery or System Center Configuration Manager \(SCCM\)\).

For additional information about Enterprise Architecture, see [APM: Application Inventory - Most common questions.](https://www.servicenow.com/community/apm-forum/apm-application-inventory-most-common-questions/m-p/1034443#M202)

**Parent Topic:**[Enterprise Architecture \(EA\) and the CSDM framework](apm-use-case-product-view.md)


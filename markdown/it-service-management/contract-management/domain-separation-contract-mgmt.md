---
title: Domain separation and Contract Management
description: Domain separation is unsupported in Contract Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/contract-management/domain-separation-contract-mgmt.html
release: australia
product: Contract Management
classification: contract-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Contract Management, Asset Management common applications, IT Service Management]
---

# Domain separation and Contract Management

Domain separation is unsupported in Contract Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: No support

-   **Data-level separation**

    The Contract \[ast\_contract\] table includes a **Domain** field \(sys\_domain\). Domain separates contract records. Users in one domain can't view contracts created in a different domain.

-   **Business logic**

    Scheduled jobs, renewal processing, approval flows, and other automated processes in Contract Management do not respect domain separation. Domain separation for these automated processes is not supported.


**Warning:** Contract data is separated by domain, but automated contract processes might not respect domain boundaries. Test all automated workflows in your domain-separated environment before deploying to production.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

**Parent Topic:**[Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/contract-management/c_ContractManagement.md)

**Related topics**  


[Use the Asset Contract Overview module]()

[Components installed with Contract Management]()

[Contract approval flow]()

[Contract Management use]()

[Condition check definitions]()

[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)


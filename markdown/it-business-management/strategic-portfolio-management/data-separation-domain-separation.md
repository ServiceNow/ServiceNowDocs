---
title: Domain separation and Data Separation
description: Domain separation is supported for Data Separation. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-portfolio-management/data-separation-domain-separation.html
release: zurich
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Data Separation, Strategic Portfolio Management]
---

# Domain separation and Data Separation

Domain separation is supported for Data Separation. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/servicenow-ai-platform-security/domain-separated-apps.md).

**Parent Topic:**[Data Separation reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/data-separation-reference.md)


---
title: Domain separation and Asset Management
description: Domain separation is supported in Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/asset-management/domain-separation-asset-management.html
release: xanadu
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Asset Management, IT Service Management]
---

# Domain separation and Asset Management

Domain separation is supported in Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

-   **[Domain separation and lifecycle reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/asset-management/domain-sep-sam-lifecycle.md)**  
There are certain domain separation aspects to consider when running software lifecycle reports.

**Parent Topic:**[Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/asset-management/c_AssetManagement.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]


---
title: Domain separation and Asset Management
description: Domain separation is supported in Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-asset-management/asset-management/domain-separation-asset-management.html
release: yokohama
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Asset Management references, Asset Management, IT Asset Management]
---

# Domain separation and Asset Management

Domain separation is supported in Asset Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/domain-separated-apps.md).

**Parent Topic:**[Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-asset-management/asset-management/references-asset-management.md)

**Related topics**  


[Quick start test for Asset Management]()

[Installed with Asset Management]()

[Installed with Model Management]()

[Transfer order line fields]()

[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-security/domain-sep-landing-page.md)


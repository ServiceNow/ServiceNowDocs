---
title: Domain separation and DLP Incident Response
description: You can use domain separation with DLP Incident Response to separate the data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure, Data Loss Prevention Incident Response, Security Operations]
---

# Domain separation and DLP Incident Response

You can use domain separation with DLP Incident Response to separate the data, processes, and administrative tasks into logical groupings called domains. You can then control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## How domain separation works with DLP Incident Response

-   Create a user with the required sn\_dlir.admin and sn\_dlir.analyst roles in the respective domain.
-   Perform the DLP Incident Response configurations in the appropriate domain.

**Parent Topic:**[Installing and configuring DLP IR Incident Response](../concept/install-dlp.md)

**Related topics**  


[Install and configure the DLP Incident Response application](../task/install-data-loss-prevention.md)


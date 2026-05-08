---
title: Domain separation and data visualizations
description: Domain separation is supported for data visualizations and relates to the data visualizations themselves and which data is visible. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Domain separation and data visualizations

Domain separation is supported for data visualizations and relates to the data visualizations themselves and which data is visible. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see Application support for domain separation.

## Overview of domain separation

 To activate the domain separation plugin, see Request domain separation.

## How domain separation works in data visualizations

Separated data includes data visualization designs and data visualization content. A data visualization defined at the global level is visible to users in all child domains.

-   Data visualizations created in the TOP domain are visible to users in the Joe's Company domain and in the HR, CS, and IT child domains of Joe's Company.
-   Data visualizations created in either the IT, CS, or HR child domains aren’t visible to users in the other child domains, but they are visible to users in the parent Joe's Company domain.
-   Data visualizations created in the parent \(Joe's Company\) domain are available only to users in that domain, but not to users in the child domains.

![List of company departments in separate domains including IT, CS, and HR. IT, CS, and HR are child domains of Joe's Company.](../../reporting/image/domains-list-example.png)

If you create a data visualization in one domain and copy it to another, the data visualization structure remains the same, but the data visualization data is adjusted for the domain. For example, a data visualization with data from the Incident table where Active=true shows all active incidents to a user in the parent global domain, but only IT incidents to a user in the IT domain.

**Parent Topic:**[Configure data visualizations](configure-data-visualizations.md)


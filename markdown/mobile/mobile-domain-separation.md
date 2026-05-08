---
title: Domain separation and mobile
description: Domain separation is supported in mobile. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Domain separation and mobile

Domain separation is supported in mobile. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Overview

The mobile platform supports domain separation for all native clients. The mobile UI design clearly indicates the domain that a record is associated with.

Before extending the domain separation functionality to mobile, the feature must be enabled on the platform web-based interface. For further information on configuration, see Domain separation setup and administration.

## How domain separation works in mobile

You can use the company or account fields to display appropriate records by domain. These fields are available in tables when the domain separation plugin is enabled. Because each company or account is linked to a single domain, when you create a record, you can use these fields to specify the domain in which you want to create the record.

After the feature has been set up through the platform web-based interface, a two-part process is required to further extend the domain separation functionality on mobile. For additional information about configuring domain separation on mobile devices, contact Customer Service and Support.

**Note:** ITSM Mobile Agent contains an automatically configured domain separation feature. For more information, refer to the ITSM Mobile Agent documentation.

**Related topics**  


[bundle-psec.domain-sep-landing-page]


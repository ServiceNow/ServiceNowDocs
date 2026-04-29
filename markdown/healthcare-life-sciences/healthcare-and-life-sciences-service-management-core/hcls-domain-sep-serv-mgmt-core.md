---
title: Domain separation and Healthcare and Life Sciences Service Management Core
description: In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Healthcare and Life Sciences Service Management Core. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Domain separation and Healthcare and Life Sciences Service Management Core

Domain separation is supported for Healthcare and Life Sciences Service Management Core. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Healthcare and Life Sciences Service Management Core overview

Domain separation is available in the [Healthcare and Life Sciences data model](hcls-serv-mgmt-core.md) that is compatible with the Health Level Seven International \(HL7\) industry standard including the Fast Healthcare Interoperability Resources \(FHIR\) standard. The Healthcare and Life Sciences Service Management Core application includes domain separation for data tables including Patient \[sn\_hcls\_patient\] table, Appointment \[sn\_hcls\_appointment\] table, Immunization \[sn\_hcls\_immunization\] table, and others. In addition, domain separation is available for transactional data like healthcare tasks and healthcare cases.

## How domain separation works in Healthcare and Life Sciences Service Management Core

For customers using the Healthcare and Life Sciences Service Management Core application to raise healthcare-related requests, the domain is set from the logged-in user’s session, in the case or task created, and the associated healthcare data.

## Use cases

When healthcare providers have their healthcare data separated by domains, the healthcare requests and corresponding fulfillment tasks are associated with the respective customer domains.

**Parent Topic:**[Healthcare and Life Sciences Service Management Core reference](../reference/hcls-serv-mgmt-core-reference.md)


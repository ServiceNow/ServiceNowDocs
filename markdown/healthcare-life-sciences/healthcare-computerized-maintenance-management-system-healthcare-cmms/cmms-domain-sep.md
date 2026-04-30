---
title: Domain separation and Healthcare Computerized Maintenance Management System
description: If any conrefs are broken, re-add them from the doc/source/reuse/domain-separation/domain-separation-overview.dita file. In the short description, edit the first sentence to state whether domain separation is supported or not and add the application name. Keep the conref at the end that describes domain separation.Domain separation is supported for Healthcare Computerized Maintenance Management System \(Healthcare CMMS\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Healthcare CMMS reference, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Domain separation and Healthcare Computerized Maintenance Management System

Domain separation is supported for Healthcare Computerized Maintenance Management System \(Healthcare CMMS\). Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

The Healthcare CMMS application includes domain separation for transactional data like medical device cases including AEM, in-service, device issue cases, and out-of-service devices.

## How domain separation works in Healthcare CMMS

For customers using the Healthcare CMMS application to raise medical device requests, the domain is set from the logged-in user’s session, in the case created, and within the associated healthcare data.

## Use cases

When healthcare providers have their healthcare data separated by domains, the healthcare requests and corresponding fulfillment tasks are associated with the respective customer domains.

**Parent Topic:**[Healthcare Computerized Maintenance Management System reference](../reference/cmms-reference.md)


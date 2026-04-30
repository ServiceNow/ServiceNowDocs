---
title: Creating requests for medical devices
description: Create requests for setting medical devices in-services, reviewing alternative equipment maintenance \(AEM\), resolving medical device issues, or setting medical devices out-of-service from a service portal.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Creating requests for medical devices

Create requests for setting medical devices in-services, reviewing alternative equipment maintenance \(AEM\), resolving medical device issues, or setting medical devices out-of-service from a service portal.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

Your administrator can configure the option for creating medical device cases based on the service request type for a medical device. The submission form for each request type is configured by your administrator.

As a user with the sn\_hcls\_cmms.device\_service\_org\_contributor role, use the following options available by default from the Case menu on the Customer Service Portal page to place service requests for your medical devices:

-   **Medical device in-service**

    Request to set a medical device in-service and associate the device with a maintenance plan.

-   **Request AEM review**

    Request to review the current maintenance plan changes associated with a medical device model.

-   **Report medical device issue**

    Report medical device issues and request to perform corrective maintenance for resolving them.

-   **Medical device out-of-service**

    Request to set a medical device out-of-service.


After a request is submitted, a corresponding medical device case is created on the associated ServiceNow instance. A clinical engineer then works on the case. To learn more, see [Managing medical device cases in Workspace](cmms-managing-cd-workspace.md).


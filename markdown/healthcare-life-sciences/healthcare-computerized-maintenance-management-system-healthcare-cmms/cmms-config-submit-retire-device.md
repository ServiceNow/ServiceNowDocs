---
title: Configuring the process for submitting medical device out-of-service requests for medical devices
description: You can configure the process for submitting requests to set medical devices out-of-service from the service portal of your healthcare organization.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure medical device out-of-service, Configure, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Configuring the process for submitting medical device out-of-service requests for medical devices

You can configure the process for submitting requests to set medical devices out-of-service from the service portal of your healthcare organization.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

By default, the users with the sn\_hcls\_cmms.device\_service\_org\_contributor role can create medical device out-of-service cases from a Customer Service Portal page of a healthcare organization. The **Medical device out-of-service** option is available from the Case menu on the Customer Service Portal page to create medical device out-of-service cases.

As a user with the admin role, you can use the **Medical device out-of-service** record producer, which is available by default, or create your own record producer to enable creating medical device out-of-service cases from a service portal. You can include the record producer for creating medical device out-of-service cases in a service  catalog and display the service  catalog  as a module on the service portal page. You can then enable users with the sn\_hcls\_cmms.device\_service\_org\_contributor role to use the module for creating medical device out-of-service cases.

To learn about record producers and service catalogs, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and [Set up a service catalog](https://www.servicenow.com/docs/access?context=t_SetUpAServiceCatalog&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).


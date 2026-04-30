---
title: Configuring the process for submitting AEM requests
description: You can configure the process for requesting the review of alternative equipment maintenance \(AEM\) for the medical device models from a service portal of your healthcare organization.
locale: en-US
release: xanadu
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Healthcare CMMS for the review of AEM requests, Configuring Healthcare CMMS, Healthcare CMMS, Clinical Device Management, Healthcare and Life Sciences]
---

# Configuring the process for submitting AEM requests

You can configure the process for requesting the review of alternative equipment maintenance \(AEM\) for the medical device models from a service portal of your healthcare organization.

**Important:** Starting with the Xanadu release, Healthcare Computerized Maintenance Management System is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

By default, the users with the sn\_hcls\_cmms.device\_service\_org\_contributor role can create medical device AEM cases from a Customer Service Portal page of a healthcare organization. The **Request AEM review** option is available from the Case menu on the Customer Service Portal page to create medical device AEM cases.

As a user with the admin role, you can use the **Request AEM review** record producer, available by default, or create your own record producer to enable creating medical device AEM cases from a service portal. You can include the record producer for creating medical device AEM cases in a service  catalog and display the service  catalog  as a module on the service portal page. You can then enable users with the sn\_hcls\_cmms.device\_service\_org\_contributor role to use the module for creating medical device AEM cases.

To learn about record producers and service catalogs, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) and [Set up a service catalog](https://www.servicenow.com/docs/access?context=t_SetUpAServiceCatalog&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).


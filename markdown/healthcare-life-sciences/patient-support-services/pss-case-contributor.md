---
title: Setting up the process to create enrollment cases as a contributor
description: Set up the process for users with the contributor roles in CSM to create enrollment cases on a service portal.
locale: en-US
release: yokohama
product: Patient Support Services
classification: patient-support-services
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Patient Support Services, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Setting up the process to create enrollment cases as a contributor

Set up the process for users with the contributor roles in CSM to create enrollment cases on a service portal.

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

If the CSM Contributor User plugin \(com.snc.csm\_contributor\_user\) is installed in addition to the Patient Support Services application, the **Create an enrollment case** record producer is available from the Case menu on the Consumer Service Portal page to create enrollment cases. To enable users with the [contributor roles in CSM](https://www.servicenow.com/docs/access?context=csm-contributor-user-roles&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for creating enrollment cases, you can use the default record producer or create your own record producer.

As an administrator, you can include the record producer for creating enrollment cases in a service  catalog and display the service  catalog  as a module on the Consumer Service Portal page. Users with the contributor profile can then use the module to create enrollment cases.

For more information, see [Record Producer](https://www.servicenow.com/docs/access?context=c_RecordProducer&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Set up a service catalog](https://www.servicenow.com/docs/access?context=t_SetUpAServiceCatalog&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) . 


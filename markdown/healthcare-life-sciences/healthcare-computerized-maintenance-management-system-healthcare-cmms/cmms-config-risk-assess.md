---
title: Configuring the risk assessment questionnaire to set medical devices in-service
description: You can configure the risk assessment questionnaire to set all the medical devices in-service within a medical device model by using a risk assessment methodology.
locale: en-US
release: zurich
product: Healthcare Computerized Maintenance Management System \(Healthcare CMMS\)
classification: healthcare-computerized-maintenance-management-system-healthcare-cmms
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set medical devices in-service, Configure, Healthcare Computerized Maintenance Management System, Clinical Device Management, Healthcare and Life Sciences]
---

# Configuring the risk assessment questionnaire to set medical devices in-service

You can configure the risk assessment questionnaire to set all the medical devices in-service within a medical device model by using a risk assessment methodology.

**Important:** Healthcare Computerized Maintenance Management System is now deprecated and no longer supported or available for new activation. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

To use maintenance and servicing workflows or inventory and management workflows, please see [Clinical Device Management](clinical-device-mgmt-overview.md).

As a user with the admin role, you can configure a risk assessment methodology for assessing risks related to the patient safety identification and compliance risk management when setting a medical device in-service for your healthcare organization.

By default, the **Medical device risk assessment** methodology is available for assessing medical device risks. You can use the default risk assessment methodology to add a questionnaire for assessing device risks or create another risk assessment methodology. For more information, see [Configure a risk assessment methodology](https://www.servicenow.com/docs/access?context=configure-ram&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US).

Note the following points when configuring a risk assessment methodology for assessing medical device risks:

-   The risk assess type must be **Residual risk**.
-   The assessment context is configured for the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table.
-   The residual assessment is generated when you save a risk assessment methodology. You must then create and map the published manual factors or questionnaires to the generated residual assessment and publish the assessment and methodology.

    **Note:** The character limitations for manual factors are:

    -   100 chars for Manual factor \(question\)
    -   50 chars for Manual factor choice \(answer\)
-   The residual risk rating is mapped to the **Risk score** column \(field\) of the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table by default. Therefore, the risk score is displayed on the playbook to set medical devices in-service. You can modify the residual risk rating to another column \(field\) of the Medical device install base item \[sn\_hcls\_medical\_device\_install\_base\_item\] table.
-   The UI action for risk assessment can be configured for the ServiceNow AI Platform view. For more information, see the [Best practices to perform Any Object Assessment \[KB0826429\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0826429) article in the Now Support Knowledge Base.


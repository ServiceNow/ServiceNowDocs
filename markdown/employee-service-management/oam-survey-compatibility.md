---
title: Outlook Actionable Messages compatibility for surveys
description: Survey definitions must be compatible with Outlook Actionable Messages \(OAM\) to display surveys in the Microsoft Outlook application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/oam-survey-compatibility.html
release: xanadu
product: Employee Service Management
classification: employee-service-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow for Microsoft Outlook, Employee Service Management]
---

# Outlook Actionable Messages compatibility for surveys

Survey definitions must be compatible with Outlook Actionable Messages \(OAM\) to display surveys in the Microsoft Outlook application.

## Conditions for OAM compatibility

The survey definition must meet the following conditions to be compatible with OAM.

-   Outlook Actionable Messages must be selected in the survey definition. For more information, see .
-   The survey must be active and published.
-   The survey must not contain image scale questions with other question types. For more information, see .
-   The survey can only contain one image scale question.

**Note:** If the survey contains more questions than the value of the **sn\_ms\_oam.feedback\_survey\_question\_count** system property, the survey opens on the portal specified in the **sn\_ms\_oam.portal.suffix** property. For more information, see [Configure system properties to update the survey question limit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/configure-survey-question-limit.md).

**Parent Topic:**[ServiceNow for Microsoft Outlook reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/sn-ms-outlook-reference.md)


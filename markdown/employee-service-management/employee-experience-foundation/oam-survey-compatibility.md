---
title: Outlook Actionable Messages compatibility for surveys
description: Survey definitions must be compatible with Outlook Actionable Messages \(OAM\) to display surveys in the Microsoft Outlook application.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow for Microsoft Outlook, Unified Employee Experience, Employee Service Management]
---

# Outlook Actionable Messages compatibility for surveys

Survey definitions must be compatible with Outlook Actionable Messages \(OAM\) to display surveys in the Microsoft Outlook application.

## Conditions for OAM compatibility

The survey definition must meet the following conditions to be compatible with OAM.

-   Outlook Actionable Messages must be selected in the survey definition. For more information, see [Modify a survey definition](https://www.servicenow.com/docs/access?context=t_ModifySurveyDefinitions&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   The survey must be active and published.
-   The survey must not contain image scale questions with other question types. For more information, see [Survey question data types](https://www.servicenow.com/docs/access?context=r_SurveyQuestionDataTypes&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   The survey can only contain one image scale question.

**Note:** If the survey contains more questions than the value of the **sn\_ms\_oam.feedback\_survey\_question\_count** system property, the survey opens on the portal specified in the **sn\_ms\_oam.portal.suffix** property. For more information, see [Configure system properties to update the survey question limit](../task/configure-survey-question-limit.md).

**Parent Topic:**[ServiceNow for Microsoft Outlook reference](sn-ms-outlook-reference.md)


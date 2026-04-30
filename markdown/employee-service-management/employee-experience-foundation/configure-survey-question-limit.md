---
title: Configure system properties to update the survey question limit
description: Configure system properties to update the question limit for a survey to be displayed in Microsoft Outlook.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-12-01"
reading_time_minutes: 1
breadcrumb: [Configure, ServiceNow for Microsoft Outlook, Unified Employee Experience, Employee Service Management]
---

# Configure system properties to update the survey question limit

Configure system properties to update the question limit for a survey to be displayed in Microsoft Outlook.

## Before you begin

Role required: admin \(OR\) oam\_admin

## About this task

The **sn\_ms\_oam.feedback\_survey\_question\_count** system property controls the behavior of the survey card that is rendered in email messages on Microsoft Outlook. If the number of questions exceeds the value of this property, the survey opens on the portal specified in the **sn\_ms\_oam.portal.suffix** property.

## Procedure

1.  Navigate to the **All** menu and enter `sys_properties.list` in the navigation filter.

    The System Properties \[sys\_properties\] table appears.

2.  In the **Name** column, search for `sn_ms_oam.feedback_survey_question_count`.

3.  Select the **sn\_ms\_oam.feedback\_survey\_question\_count** property.

4.  Update the **Value** field with the number that you want to set as the survey question limit.

    The default value of the property is **2**.

5.  Select **Update**.



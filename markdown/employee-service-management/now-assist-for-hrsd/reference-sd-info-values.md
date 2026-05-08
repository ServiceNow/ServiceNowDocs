---
title: Sensitivity detection filters mapping
description: The sys\_gen\_ai\_filter table includes eight out-of-the-box filters that determines which topics are regarded as sensitive. Each filter is mapped to an HR service that is used to create a case and a chat queue.
locale: en-US
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: reference
last_updated: "2026-05-08"
reading_time_minutes: 1
breadcrumb: [Reference, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Sensitivity detection filters mapping

The `sys_gen_ai_filter` table includes eight out-of-the-box filters that determines which topics are regarded as sensitive. Each filter is mapped to an HR service that is used to create a case and a chat queue.

The filter to service and queue mapping is set by the `getFilterMetaData` function in the `SensitivityDetectionVAUtilSNC` script.

To modify the HR service used to create a case, update the HR service sysid that is associated to the filter in the `filterMap` object of the function.

To modify the live agent chat queue, update the text that is associated to the `queueType` object. The value is used to set the `liveagent_esc_pre_chat_category.`

Modify the condition that is associated with your `awa_queue`record so that you can check the value in this field.

|Filter|HR Service|Queue|
|------|----------|-----|
|Compensation and Career Advancement|Request accommodation|Employee relations|
|Employee Health Concerns|Request accommodation|Employee relations|
|Employee Personal issues|Report misconduct|Employee relations|
|Ethics, Safety, and Employee Behavior and workplace practices|Report misconduct|Employee relations|
|Performance, evaluation, and Support Concerns|General|General|
|Termination disputes &amp; Layoff Concerns|Request accommodation|Employee relations|
|Workplace misconduct: Workplace harassment, Violence, and discrimination|Report misconduct|Employee relations|
|Workplace Substance Abuse and Support|Report misconduct|Employee relations|

**Parent Topic:**[Reference for Now Assist for HR Service Delivery \(HRSD\)](reference-now-assist-hrsd.md)


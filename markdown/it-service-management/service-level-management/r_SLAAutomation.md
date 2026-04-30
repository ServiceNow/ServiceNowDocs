---
title: SLA calculation
description: SLAs are calculated and assessed by a business rule and scheduled jobs that run in the background.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Using Service Level Management, Service Level Management, IT Service Management]
---

# SLA calculation

SLAs are calculated and assessed by a business rule and scheduled jobs that run in the background.

The mechanisms that control SLA Workflow and SLA Automation are independent of each other. You may have a requirement to send out email notifications from the SLA Workflow displaying the current elapsed percentage of the SLA. However, this does not work because using percentage in a notification only displays the most recently calculated value of the Task SLA. This results in inaccurate values sent out in email when using SLA calculated values in a Task SLA email notification.

One solution is to specify elapsed percentage in SLA notifications by using notifications for each percentage level. For example, an email notification for "75 percent SLA Warning" is created and a special event is used to trigger that notification. The event can be called "sla.warning.75". Another solution is hard-coding these email notifications to trigger at a specified duration percentage, and configure the workflow linked to that SLA definition to send an email notification after waiting an elapsed percentage.

-   **[Run the 2011 SLA engine asynchronously](../task/t_RunSLABusinessRule.md)**  
By default in the 2011 SLA engine, the SLA processing is performed by the **Run SLAs** business rule. This business rule runs synchronously and is the suggested configuration.
-   **[Recalculate SLA times automatically](../task/t_SLACalculationOnTaskDisplay.md)**  
By default when a user opens a task, the SLA timing information for that task is not automatically recalculated.
-   **[Use exact times in SLA calculations](../task/t_SLABreachCalculation.md)**  
When business percentages are used for SLA calculations, they are rounded up to two decimal places.

**Parent Topic:**[Using Service Level Management](../concept/using-service-level-management.md)


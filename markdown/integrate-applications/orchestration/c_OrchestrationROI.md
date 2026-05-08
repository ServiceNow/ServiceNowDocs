---
title: Orchestration ROI
description: The Orchestration ROI application allows you to estimate and compute cost savings for tasks in your system that could be automated with Orchestration.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Orchestration ROI

The Orchestration ROI application allows you to estimate and compute cost savings for tasks in your system that could be automated with Orchestration.

After you automate the tasks, you can track cost savings by associating Orchestration workflows with corresponding task areas. Configuration in the application allows you to select the hourly rate for performing the task manually, the rules the system uses to select tasks for evaluation, and the time period of the evaluation. Orchestration ROI estimates your savings by multiplying the cost of performing repetitive tasks manually by the estimated number of times the system performs those tasks automatically during a specific date/time range. The system also calculates the actual savings of your automations. Orchestration ROI is included with the base Orchestration subscription.

Orchestration ROI reports offer a number of views of the comparative data and allow you to access the associated records directly from the reports. The [standard reports](../reference/r_OrchestrationROIStandardDashboard.md#) included with the Orchestration - ROI plugin provide summaries, estimated costs, and calculated costs for automated processes. The [ROI premium dashboard](../reference/r_OrchestrationROIPremiumDashboard.md#) uses Performance Analytics to provide detailed reports on calculated savings over time. Performance Analytics requires a different plugin and subscription.

**Note:** When Orchestration ROI is activated as a dependent plugin of Orchestration, demo data is not installed. If you want to use demo data as a template for your own ROI evaluation, submit a request to ServiceNow® technical support for an Orchestration ROI plugin upgrade with demo data selected.

To set up Orchestration ROI, complete the configuration tasks in the order shown here.

-   **[Create Orchestration ROI labor rate cards](../task/t_CreateOrchROILaborRateCard.md)**  
Before calculating your Orchestration ROI, you must create labor rate cards for the manual work that would be required to complete the tasks correlated to the ROI calculations.
-   **[Create an Orchestration ROI automation entry record](../task/t_CreateOrchROIAutoEntryRecord.md)**  
The ROI automation entry record couples the cost of performing a task with the specific workflow that automates the task, for the purpose of calculating the resulting savings.
-   **[Create an Orchestration ROI correlated task rule](../task/t_CreateOrchROICorrTaskRule.md)**  
The correlated task rule applies configurable conditions to fields in a selected table that tell the instance which manual tasks correspond to an automation entry record.
-   **[Configure the time range for Orchestration ROI calculations](../task/t_ConfigTimeOrchROICalc.md)**  
Select a date range to calculate the average number of tasks and the duration per month for the correlated tasks.
-   **[Installed with Orchestration ROI](../reference/r_InstalledWithOrchestrationROI.md#)**  
Several types of components are installed with the Orchestration - ROI plugin \(com.snc.runbook\_automation.roi\).
-   **[Orchestration ROI reports](c_OrchestrationROIDashboards.md)**  
Orchestration ROI provides a collection of standard and premium reports to help you calculate savings from automating services in your organization.

**Parent Topic:**[Orchestration applications](c_OrchestrationApplications.md)


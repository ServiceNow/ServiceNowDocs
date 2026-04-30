---
title: Approvals hub integration with Workday
description: Enable easier access to all active approvals of external business applications such as Workday from Employee Center Pro. The Workday spoke is built by Bristlecone, Inc.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Approval hub integrations, Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Approvals hub integration with Workday

Enable easier access to all active approvals of external business applications such as Workday from Employee Center Pro. The Workday spoke is built by Bristlecone, Inc.

Using Approvals hub integration with Workday, you can perform the following actions from Employee Center Pro:

-   Pull employee information from Workday for time off requests, correct time off request, leave of absence, timesheet, job change, job requisition, termination, spend authorization, and compensation details to a ServiceNow application.
-   View the Workday information from your ServiceNow instance.
-   Enable approvers to view, reject, and approve the tasks right from Employee Center Pro.

## Application setup

Ensure you have the latest versions of the following plugins:

-   Employee Center Pro
-   HR Service Delivery Integration with Workday 3.0.0

    **Note:** Upgrade v2.0.6 to v 3.0.0

-   Workday HR Spoke
-   Human Resources Scoped App: Core \(com.sn\_hr\_core\)
-   Enterprise Service Management Integrations Framework. This framework is installed with Employee Center Pro.

## Prerequisites

Before you start working on the Workday integration, get familiar with the following steps.

-   Ensure you have the HRSD pro/Enterprise license that includes EC Pro. Workday integration is not available for Employee Center Pro standalone.​
-   Understand how Enterprise Service Management Integrations Framework works, see [Using Enterprise Service Management Integrations Framework](../../human-resources/task/use-integrations-framework.md) and [View tasks of a third-party system](../../human-resources/task/display-todos.md)
-   Integrate Workday with ServiceNow, as explained in [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) and [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).
-   Activate and run the schedule flow that pulls record details. For more information, see [Activating schedule flows](../../human-resources/task/activate-w-schedule-flow.md).
-   Understand the installed components as explained in [Components installed with HR Service Delivery Integration with Workday](../../human-resources/reference/installed-with-wd.md)
-   Understand the basics of [Workday integration](https://www.workday.com/en-us/products/platform-product-extensions/integrations.html) and business processes.

**Note:** The RCAs that are generated after the installation are in the **Requested** state and you must manually mark the RCAs as **Allowed**, which can be time-consuming. To automate the RCA approvals for any record, you can run the EC bulk RCAs approval script where the source scope is one of the Employee Experience applications.

## Workday approvals workflow

Improve productivity by managing third-party approval flows from Employee Center Pro. Here is a list of the supported Workday todos configurations.

|Todos configuration|Table name|
|-------------------|----------|
|Job Change Request Todos|sn\_hr\_workday\_job\_change\_request\_todos|
|Job Requisition Request Todos|sn\_hr\_workday\_job\_requisition\_request\_todos|
|Leave Of Absence Request Todos|sn\_hr\_workday\_leave\_of\_absence\_request\_todos|
|Spend Authorization Request Todos|sn\_hr\_workday\_spend\_authorization\_request\_todos|
|Termination Request Todos|sn\_hr\_workday\_termination\_request\_todos|
|Time Off Request Todos|sn\_hr\_workday\_time\_off\_request\_todos|
|Correct Time Off Request Todos|sn\_hr\_workday\_correct\_time\_off\_request\_todos|
|Timesheet Request Todos|sn\_hr\_workday\_todo|
|Compensation Change Request Todos|sn\_hr\_workday\_compensation\_change\_request\_todos|

By default, todos configurations are available for **Open** and **Completed**.

**Note:** For more information the field-level info about leaves, timesheets, timeoffs, compensation change, job change, job requisition, or leave of absence, see [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

For additional reference information, see [Approvals experience reference](../reference/approval-hub-ootb.md).

-   **[Fetch Workday reports](../task/wd-ec-approvals-scheduled-job.md)**  
As an administrator, fetch the reports metadata from other business applications such as Workday. View the Workday reports, leaves, compensation, and other information from your ServiceNow instance.
-   **[Configure Workday to-dos](../task/config-workday-raas-report.md)**  
Store one-time configuration parameters to pull tasks from Workday into the ServiceNow application.
-   **[Use task configuration for Workday approvals](../task/wd-approval-hub-to-dos-page.md)**  
Using the default To-dos configuration, you can provide the approvers with more in-context information about the approval requests for better approval workflows.

**Parent Topic:**[Approval hub integrations](approvals-int-concept.md)


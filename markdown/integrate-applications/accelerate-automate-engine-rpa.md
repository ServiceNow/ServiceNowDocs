---
title: Accelerating and automating your repetitive tasks by using Workflow Data Fabric
description: Reduce the time that you spend on repetitive tasks and deliver services faster through an automated workflow in Workflow Data Fabric. You can automate the data extraction from your documents with the Document Intelligence application, automate your data validation with third-party APIs with the Integration Hub application, and automate your legacy systems with the RPA Hub application all within a single workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Workflow Data Fabric]
---

# Accelerating and automating your repetitive tasks by using Workflow Data Fabric

Reduce the time that you spend on repetitive tasks and deliver services faster through an automated workflow in Workflow Data Fabric. You can automate the data extraction from your documents with the Document Intelligence application, automate your data validation with third-party APIs with the Integration Hub application, and automate your legacy systems with the RPA Hub application all within a single workspace.

## Using the combined benefits of the solution

Get these benefits by using different applications through the solution:

-   Automate document data extraction.
-   Create and extend processes by using low-code, no-code API integration.
-   Automate repetitive and legacy processes to deliver services faster.
-   Reduce the time that you spend on repetitive tasks and improve your productivity.
-   Realize the value of automation to the organization through Automation Center workspace.

## Workflow for the solution

Let's consider a scenario of how an employee and an agent use an automation engine and its various products to set up a direct deposit service. The employee, who had recently changed bank accounts, wants to update their direct deposit information. A direct deposit service is used to set up a new bank account for payroll, through an automated process. In this automated process, the following applications are used:

-   Document Intelligence
-   Integration Hub
-   RPA Hub
-   Automation Center

These applications together enable the employee and agent to get complete visibility into the direct deposit workflow.

The direct deposit request from the employee is divided into three stages. The stages are to extract the data, validate the data, and update the payroll system.

The following diagram shows the workflow for the solution.

![Workflow for accelerating and automating your repetitive tasks with Workflow Data Fabric. For the text description, refer to the workflow steps that follow.](../image/automation-engine-workflow.png "Workflow for the solution")

The workflow for this solution is

1.  An employee visits the Employee Center portal and searches for the Direct Deposit form through AI Search or Virtual Agent chat assistant.

    Employee Center is a central portal where employees can find out the latest updates from your organization. For more information, see [Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

2.  The employee uploads a void check and submits the request.
3.  The request comes into the Direct Deposit Workspace that uses a playbook to navigate the complex process in a guided process.
4.  In the back end, Document Intelligence analyzes the attached check data, extracts the data, and displays it so that the agent can review it.

    Document Intelligence knows which fields to extract. When the model is trained over time, the value has a higher confidence score that is determined by the AI in Document Intelligence. The agent or the automation team can set a score to meet their threshold requirements.

    For more information about Document Intelligence, see [Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

5.  An agent navigates to the Direct Deposit Workspace, opens the direct deposit request, and reviews the data that was extracted from the employee's check. As the agent completes the review, the information is automatically updated on the form.
6.  The extraction stage completes and the validation stage starts. An agent can view this process in the playbook.
7.  By using Integration Hub, a third-party integration validates the extracted data from the check. The extracted values are sent through an API for validation using Integration Hub spoke actions. This flow is completed by using Workflow Studio with the power of the Integration Hub spokes. The flow hits an external end point, fetches the data, and compares this data against the system data to validate the bank details. On a successful validation, the direct deposit form is updated with any relevant notes.

    For more information about Workflow Studio, see [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US). For more information about Integration Hub, see [Integration Hub](../../administer/integrationhub/concept/integrationhub.md).

8.  The data validation stage completes and the payroll system update stage begins.
9.  When the request arrives for a payroll update, the system initiates an unattended robot to process the employee's bank information into the legacy payroll system \(that doesn't have any API interface\) by using RPA Hub.

    In a typical situation, an agent copies the data from the bank record, opens the payroll application, and pastes the data manually to submit. This process is prone to error. With RPA Hub, this process is automated by using an unattended robot that impersonates the agent and runs on any remote Windows machine. It accesses the ServiceNow record securely and inserts the data into the payroll system within a few seconds.

    For more information about RPA Hub, see [Robotic Process Automation \(RPA\) Hub](../../product/rpa-core/concept/rpa-main-landing-page.md).

10. After the payroll updates, the direct deposit request changes to the **Closed** state.
11. The agent can open the Automation Center Workspace to view the cost, time saving, and the true value of the automation.

    For more information about Automation Center, see [Automation Center](../../product/automation-center/concept/automation-center-landing-page.md).


## Requirements for integrating the solution

Your administrators can integrate the solution by doing the following actions:

1.  Activate the Integration Hub plugins. For more information, see [Request an Integration Hub plugin](../../administer/integrationhub/tasks/request-integrationhub.md) and [Integration Hub plugins](../../administer/integrationhub/reference/ih-plugins.md).
2.  Install the Employee Center application and configure the Employee Center Portal. For more information, see [Install Employee Center](https://www.servicenow.com/docs/access?context=activate-ec&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) and [Employee Center admin configurations](https://www.servicenow.com/docs/access?context=configure-ec-portal&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).
3.  Install and set up the Document Intelligence application. For more information, see [Install Document Intelligence](https://www.servicenow.com/docs/access?context=install-document-intelligence&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) and [Set up Document Intelligence](https://www.servicenow.com/docs/access?context=get-started-with-doc-intel&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
4.  Install the RPA Hub application. For more information, see [Install Robotic Process Automation \(RPA\) Hub](../../product/rpa-core/task/install-rpa.md).
5.  Install the Automation Center application. For more information, see [Install Automation Center](../../product/automation-center/task/install-automation-center.md).
6.  Activate a spoke. For more information, see [Integration Hub spokes](../../administer/integrationhub/reference/spokes-list.md).
7.  Build spokes using Spoke Generator. For more information, see [Building spokes using Spoke Generator](https://www.servicenow.com/docs/access?context=spoke-builder&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).


---
title: Oracle HCM Cloud Spoke
description: Manage work structures and human capital in Oracle HCM Cloud instance from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-06"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle HCM Cloud Spoke

Manage work structures and human capital in Oracle HCM Cloud instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle HCM Cloud spoke v4.4.0 is the latest version.

## Supported versions

This spoke was built for Oracle HCM Cloud API version 11.13.18.05, but may be compatible with later versions.

## Spoke requirements

Oracle HCM Cloud subscription.

## Spoke dependencies

If you’re having trouble installing the app, verify that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   Large JSON and XML Payload Builder API \(com.glide.streaming\_builder\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke subflows

The Oracle HCM Cloud spoke provides sample subflows to demonstrate automating Oracle HCM Cloud tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Get Active Department|Retrieves the active department information by calling the **Look up Departments** action.|

## Spoke actions

The Oracle HCM Cloud spoke provides actions to automate tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|All Record Management|Look up Record Details|Retrieves all record details.|
|Look up Time Record Details|Retrieves the employee's time sheet for the specified time.|
|Absence Management|Look up Time Off Balance|Retrieves the time-off details of an employee.|
|Look up Absence Type|Retrieves the absence type for the specified employee.|
|Look up Absence Type Reason|Retrieves absence type reasons for all the available absence types.|
|Request Time Off|Request time off for the specified employee.|
|Employee Information Management|Update Personal Details|Updates the employee details, such as the email address, phone number, date of birth, or blood type.|
|Employee Document Management|Get Employee Documents by Employee ID|Retrieves the documents of an employee by the employee ID.|
|Get Employee Documents Attachments|Retrieves the attachments of an employee's document.|
|Benefits Management|Look up Benefit Enrollments|Retrieves the benefit enrollment details of an employee.|
|Compensation Management|Get Total Rewards|Retrieves the total rewards details of an employee.|
|Look up Individual Compensation|Retrieves the individual compensation details of an employee.|
|Employee Atom Feeds|Look up Atom Feeds Employees Assignments Stream|Retrieves the changes made in employee assignments.|
|Look up Atom Feeds Employees New hire Stream|Retrieves information about the employees who were recently hired.|
|Look up Atom Feeds Employees Termination Stream|Retrieves information about the terminated employees.|
|Look up Atom Feeds Employees Update Stream|Retrieves information about the employee updates.|
|Feedback Management|Look up Feedback|Retrieves the feedback received for the employees.|
|Goals Management|Look up Goals|Retrieves the goals of an employee.|
|Human Capital Management|Look up Departments Stream|Retrieves information about the departments.|
|Look up Employee Assignments|Retrieves information about the employees assignments.|
|Look up Employees Stream|Retrieves information about the employees.|
|Get User Holiday Calendar|Retrieves information about the holidays for the specified year in the specified country.|
|Look up Jobs Stream|Retrieves information about the jobs.|
|Look up Locations Stream|Retrieves information about the locations.|
|Look up Organizations Stream|Retrieves a list of organizations from Oracle HCM.|
|Look up Positions Stream|Retrieves information about the positions.|
|Look up Workers Stream|Retrieves information about the workers.|
|Look up Active and Inactive Workers Stream|Retrieves information about the active and inactive workers.|
|Job Management|Look up Job Application Attachment|Retrieves the job application attachments.|
|Look up Job Applications Stream|Retrieves a list of job applications fromOracle HCM.|
|Look up Recruiting Candidates|Retrieves the details of a recruiting candidate.|
|Look up Recruiting Job Requisitions Stream|Retrieves a list of recruiting job requisitions.|
|Metadata Retrieval|Get Oracle Cloud HCM Array.Object Schema|Retrieves information about the Oracle Cloud HCM array object schema.|
|Get Oracle Cloud HCM Object Metadata|Retrieves information about the Oracle Cloud HCM object metadata.|
|Get Oracle Cloud HCM Objects|Retrieves information from Oracle Cloud HCM Objects.|
|Payroll Management|Look up External Bank Accounts|Retrieves external bank account information for employees.|
|Look up Payroll|Retrieves payroll information of an employee.|
|Look up Legislative Data Group|Retrieves legislative data group details for an employee.|
|Look up Payslip|Retrieves payslip details for an employee.|
|Look up Payroll Elements|Retrieves payroll element information of employees.|
|Workstructures Atom Feeds|Look up Atom Feeds Jobs Stream|Retrieves the changes made in jobs.|
|Look up Atom Feeds Locations Stream|Retrieves the changes made in locations.|
|Look up Atom Feeds Organizations Stream|Retrieves the changes made in organizations.|
|Look up Atom Feeds Positions Stream|Retrieves the changes made in positions.|

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for information about AI agents.

Available AI agents include:

|AI agent|Description|
|--------|-----------|
|Oracle HCM Cloud feedback management AI agent|Retrieves and manages feedback that the employees received.|
|Oracle HCM Cloud goals management AI agent|Retrieves goals and provide relevant actionable information to enable users manage and track their objectives.|
|Oracle HCM Cloud human capital management AI agent|Retrieves employee data, organizational structures, and other HR-related tasks by leveraging predefined actions.|
|Oracle HCM Cloud jobs management AI agent|Retrieves and manages data related to recruiting, job applications, and candidate information.|
|Oracle HCM Cloud payroll management AI agent|Retrieves, processes, and manages payroll-related data.|
|Oracle HCM Cloud compensation management AI agent|Retrieves and manages compensation-related data. Also, provides access to critical information and insights.|

Looking for an AI agent?

-   There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available on your instance, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).
-   To find agents that might not be installed on your instance, visit the [AI Agent Marketplace](https://store.servicenow.com/store/ai-marketplace) on the ServiceNow Store.

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

<table id="id_fx3_vvk_53c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Fetch Individual Compensation and Payslip and Total Rewards

</td><td>

Retrieves and consolidates an employee’s compensation data from Oracle HCM, including payslips, salary details, and total rewards information. It orchestrates multiple Oracle HCM actions and presents the results as a clear, HR‑friendly summary that supports payroll review, employee inquiries, and compensation analysis.

</td><td>

-   Oracle HCM Cloud payroll management AI agent
-   Oracle HCM Cloud compensation management AI agent

</td><td>

Yes

</td></tr><tr><td>

Fetch Goals and Performance Feedback

</td><td>

Retrieves employee goals and performance feedback from Oracle HCM and presents the information as a consolidated goals and performance summary. It helps HR teams and managers quickly review progress, feedback, and performance context in a clear format.

</td><td>

-   Oracle HCM Cloud goals management AI agent
-   Oracle HCM Cloud feedback management AI agent

</td><td>

Yes

</td></tr></tbody>
</table>## Spoke module

The Oracle HCM Cloud spoke adds the Oracle HCM Cloud application to your instance and includes the modules in the following table.

|Module|Description|
|------|-----------|
|BI Report Paths|Lists the BI report paths for the actions.|
|Look up Holiday Calendars|Lists the holiday calendars.|
|New Positions|Lists the available new positions.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Configure the Oracle HCM Cloud spoke connection record](../../integrationhub-store-spokes/task/setup-oracle-hcm.md).


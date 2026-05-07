---
title: SuccessFactors Spoke
description: The SuccessFactors spoke is built by Bristlecone, Inc. Manage data and entities in SuccessFactors from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-04-06"
reading_time_minutes: 18
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SuccessFactors Spoke

The SuccessFactors spoke is built by Bristlecone, Inc. Manage data and entities in SuccessFactors from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html). Starting on March 1st 2022, all SAP spokes will be available only on the Store.

## IntegrationHub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SuccessFactors spoke v4.10.1 is the latest version.

## Supported versions

This spoke was built for SuccessFactors v2.0, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - XML Parser \(com.glide.hub.action\_step.xmlparser\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   Remote Tables \(com.glide.script.vtable\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke flows

The SuccessFactors spoke provides sample flows in the draft state to demonstrate automating the SuccessFactors tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

<table id="table_jrx_pjp_5lb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Todo

</td><td>

Creates a to-do record in SuccessFactors.

</td></tr><tr><td>

Update Todo

</td><td>

Updates details of the specified to-do record in SuccessFactors.

</td></tr><tr><td>

Run SuccessFactors Integration Flow

</td><td>

Retrieves entire data or only updates made after the last refresh, for the selected entities, from SuccessFactors to your ServiceNow instance. By default, you can retrieves data from these entities in SuccessFactors:-   Department
-   Location
-   Job Profile
-   Workers Profile
-   Effective Workers Profile
-   Job History Including Secondary Assignments
-   Todo

</td></tr></tbody>
</table>**Note:** The Create Todo and Update Todo flows demonstrate the to-do record management when events occur in ServiceNow. You can customize these flows according to your requirement to manage records of other entities from your ServiceNow instance.

## Spoke subflows

The SuccessFactors spoke provides sample subflows in the draft state to demonstrate automating the SuccessFactors tasks. To customize a sample subflow, copy the sample subflow to a new application scope. Available sample subflows include:

<table id="table_bd5_ckp_5lb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Look up Departments

</td><td>

Retrieves the department data from SuccessFactors and stores it in SuccessFactors Departments Staging Table.

</td></tr><tr><td>

Retrieve Effective Worker Profiles

</td><td>

Retrieves the Effective Worker Profiles data from SuccessFactors and stores it in SuccessFactors Worker Profiles Staging Table.

</td></tr><tr><td>

Retrieve Full Job History Including Secondary Assignments

</td><td>

Retrieves all primary and secondary job history data from SuccessFactors.

</td></tr><tr><td>

Retrieve Job Profiles

</td><td>

Retrieves the job profile data from SuccessFactors and stores it in SuccessFactors Job Profile Staging Table.

</td></tr><tr><td>

Retrieve Locations

</td><td>

Retrieves the location data from SuccessFactors and stores it in SuccessFactors Locations Staging Table.

</td></tr><tr><td>

Retrieve Todos

</td><td>

Retrieves the to-do data from SuccessFactors and stores it in SuccessFactors Inbound Todos Staging Table.

</td></tr><tr><td>

Retrieve Worker Profiles

</td><td>

Retrieves the Worker Profiles data from SuccessFactors and stores it in SuccessFactors Worker Profiles Staging Table.

</td></tr><tr><td>

Run SuccessFactors Service

</td><td>

Retrieves entire data or only updates made from the last successful runtime, for the selected entities.

</td></tr><tr><td>

Process SuccessFactors Webhooks

</td><td>

Processes the SAP SuccessFactors webhook event. For more information about setting up the webhooks, see [Set up webhook for the SuccessFactors spoke](../task/setup-sapsf-webhooks.md).

</td></tr><tr><td>

Retrieve Worker Profile by Company Territory Code

</td><td>

Retrieves the data of worker profile from SAP SuccessFactors based on company territory code, and stores it in the 'SuccessFactors Worker Profiles Staging Table'.**Note:** Worker profiles without employment or job information will not be retrieved, as the subflow fetches data based on the company territory code, which is assigned only after employment is assigned to the worker.

</td></tr></tbody>
</table>## Spoke actions

The SuccessFactors spoke provides sample actions in the draft state to demonstrate automating the SuccessFactors tasks when events occur in ServiceNow. To customize a sample action, copy it to a new application scope. Available sample actions include:

**Note:**

-   To help prevent unauthorized users from accessing the sensitive data, the hasRole functionality has been implemented for the sensitive actions of the SuccessFactors spoke. As a result, users without the System Administrator role won’t be able to run successfully the actions if they don't have the SuccessFactors Spoke Admin role. This rule is applicable from SuccessFactors spoke v3.1.5 and v4.0.3 of the spoke respectively. For more information, see the [SuccessFactors Spoke hasRole fix details](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1281664) knowledge base article on [NOW Support](https://support.servicenow.com/now).
-   To help prevent unauthorized users from generating reports for SuccessFactors spoke tables, report\_view ACLs are incorporated with the spoke admin role. Thus, you must have the SuccessFactors Spoke’s Admin role to generate a report.

<table id="table_ymm_ql1_zmb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="24">

Employee Management

</td><td>

Employee Address Information

</td><td>

Retrieves the address information of the specified employee.

</td></tr><tr><td>

Employee Annual Compensation

</td><td>

Retrieves the annual compensation details of the specified employee.

</td></tr><tr><td>

Employee Compensation Details

</td><td>

Retrieves compensation details of the specified employee.

</td></tr><tr><td>

Employee Documents

</td><td>

Retrieves all the viewable documents of the specified employee.

</td></tr><tr><td>

Employee Payment Method Details

</td><td>

Retrieves the details about payment method of the specified employee.

</td></tr><tr><td>

Employee Time Off

</td><td>

Retrieves the time offs taken by the specified employee.

</td></tr><tr><td>

Employee Time Off Balances

</td><td>

Retrieves the time off-balance details of the specified employee.

</td></tr><tr><td>

My TimeCard Details

</td><td>

Retrieves the time sheet details of the specified employee.

</td></tr><tr><td>

Change User Roles

</td><td>

Adds user to the given permission group.

</td></tr><tr><td>

Employee All Payment Methods Details

</td><td>

Retrieves details of all the payment methods of the specified employee.

</td></tr><tr><td>

Employee Recurring Compensations

</td><td>

Manages the recurring component of a specified employee's compensation.

</td></tr><tr><td>

Get Employee Benefit Enrollments

</td><td>

Retrieves details of the benefit enrollments of the specified employee during a specific time period.

</td></tr><tr><td>

Offboard an Employee

</td><td>

Triggers the termination process of the specified employee.

</td></tr><tr><td>

Org Change

</td><td>

Changes the organization related information of the specified employee.

</td></tr><tr><td>

Report No Shows

</td><td>

Reports no show for the specified employee.

</td></tr><tr><td>

Reporting Structure

</td><td>

Retrieves the reporting structure of the specified employee.

</td></tr><tr><td>

Request Time Off

</td><td>

Applies a time off request for the specified employee.

</td></tr><tr><td>

Update Employee Address

</td><td>

Updates the address of the specified employee.

</td></tr><tr><td>

Update Employee DOB

</td><td>

Updates the date of birth of the specified employee.

</td></tr><tr><td>

Update Employee Email

</td><td>

Updates the details of the email of the specified employee.

</td></tr><tr><td>

Update Employee Phone

</td><td>

Updates the phone details of the specified employee.

</td></tr><tr><td>

Update Employee Personal Information

</td><td>

Updates the personal information of the specified employee.

</td></tr><tr><td>

Update Employee Personal Information - Global

</td><td>

Updates the global information of the specified employee.

</td></tr><tr><td>

Update Employee Start Dates

</td><td>

Updates the start date of employment of the specified employee.

</td></tr><tr><td rowspan="20">

HR Foundational Data

</td><td>

Login into SuccessFactors

</td><td>

Logs in to SuccessFactors and retrieves the Session ID.

</td></tr><tr><td>

Retrieve Current Employment Information

</td><td>

Retrieves the current employment information from SuccessFactors.

</td></tr><tr><td>

Look up Departments

</td><td>

Retrieves the department data from SuccessFactors.

</td></tr><tr><td>

Look up Addresses Stream

</td><td>

Retrieves address information from SuccessFactors.

</td></tr><tr><td>

Look up Emails Stream

</td><td>

Retrieves emails information.

</td></tr><tr><td>

Look up Person Biographical Stream

</td><td>

Retrieves person biographical information.

</td></tr><tr><td>

Look up Personal Detailed Information Stream

</td><td>

Retrieves personal detailed information.

</td></tr><tr><td>

Look up Employment Information Stream

</td><td>

Retrieves the employment information from SuccessFactors.

</td></tr><tr><td>

Look up Phone Stream

</td><td>

Retrieves phone information from SuccessFactors.

</td></tr><tr><td>

Look up Employee Global Assignments Stream

</td><td>

Retrieves all global assignment details from SAP SuccessFactors.

</td></tr><tr><td>

Look up Secondary Assignments Stream

</td><td>

Retrieves all secondary assignments from SAP SuccessFactors.

</td></tr><tr><td>

Retrieve Full Job History Including Secondary Assignments

</td><td>

Retrieves the complete job history data including secondary assignments from SuccessFactors.

</td></tr><tr><td>

Retrieve Effective Worker IDs

</td><td>

Retrieves the effective Worker Profiles ID from SuccessFactors.

</td></tr><tr><td>

Retrieve Profiles by Person ID

</td><td>

Retrieves the Worker Profiles data by Person ID from SuccessFactors.

</td></tr><tr><td>

Retrieve Effective Worker Profiles

</td><td>

Retrieves the Effective Worker Profiles data from SuccessFactors.

</td></tr><tr><td>

Retrieve Job History Including Secondary Assignments \(Deprecated\)

</td><td>

Retrieves the job history data including secondary assignments from SuccessFactors.

</td></tr><tr><td>

Retrieve Job Profiles

</td><td>

Retrieves the job profile data from SuccessFactors.

</td></tr><tr><td>

Retrieve Locations

</td><td>

Retrieves the location data from SuccessFactors.

</td></tr><tr><td>

Retrieve Worker Profiles

</td><td>

Retrieves the Worker Profiles data from SuccessFactors.

</td></tr><tr><td>

Get Holiday Calendar

</td><td>

Retrieves holiday calendar for a country.

</td></tr><tr><td rowspan="28">

Metadata Retrieval**Note:** To execute the creatable, deletable, updatable, and list metadata actions, create a system property with **Name** as **com.glide.attachment.max\_get\_size** in the Global scope and set its **Value** to `20000000`.

</td><td>

Get Dynamic Output Fields

</td><td>

Creates a dynamic output structure for mapping of fields in response for the given entity.

</td></tr><tr><td>

Get Entities - Creatable

</td><td>

Retrieves the entities for which the create operation is supported.

</td></tr><tr><td>

Get Entities - Deletable

</td><td>

Retrieves the entities for which the delete operation is supported.

</td></tr><tr><td>

Get Entities - Updatable

</td><td>

Retrieves entities for which the update operation is supported.

</td></tr><tr><td>

Get Entities List

</td><td>

Retrieves the list of all entities.

</td></tr><tr><td>

Get Fields - Creatable

</td><td>

Retrieves all the creatable non-navigation properties in an entity.

</td></tr><tr><td>

Get Fields - Updatable

</td><td>

Retrieves all the updatable non-navigation fields in an entity.

</td></tr><tr><td>

Get Key Fields

</td><td>

Retrieves all the key fields in the specified entity.

</td></tr><tr><td>

Get Required Fields - Creatable

</td><td>

Retrieves all the required insertable fields in the specified entity.

</td></tr><tr><td>

Get Updatable Todo Fields

</td><td>

Retrieves the list of updatable fields in the Outbound Todos Staging Table.

</td></tr><tr><td>

Get Available Positions

</td><td>

Retrieves all the available positions for given company and location code.

</td></tr><tr><td>

Get Business Units

</td><td>

Retrieves all the available business units in SuccessFactors.

</td></tr><tr><td>

Get Companies

</td><td>

Retrieves all the available active companies in SuccessFactors.

</td></tr><tr><td>

Get Countries

</td><td>

Retrieves all the available countries in SuccessFactors.

</td></tr><tr><td>

Get Country Code

</td><td>

Retrieves country code of a country.

</td></tr><tr><td>

Get Dynamic Permission Groups

</td><td>

Retrieves all the available dynamic permission groups.

</td></tr><tr><td>

Get Event Reasons By Event ID

</td><td>

Retrieves all the event reasons for the specified Event ID.

</td></tr><tr><td>

Get Global Information By Entity

</td><td>

Retrieves metadata of the entity specified to fetch the global information.

</td></tr><tr><td>

Get Global Personal Information Supported Countries

</td><td>

Retrieves details of the countries that support the creation and modification of the personal global information.

</td></tr><tr><td>

Get Locations By Company Code

</td><td>

Retrieves all the active locations from SuccessFactors for the specified company code.

</td></tr><tr><td>

Get People Pools By Group ID

</td><td>

Retrieves all people pools with only user name category for the specified group.

</td></tr><tr><td>

Get Pick List Options

</td><td>

Retrieves all the available pick list options for the specified pick list ID.

</td></tr><tr><td>

Get Pick List Options By Country

</td><td>

Retrieves the pick list options of the specified country.

</td></tr><tr><td>

Get Recurring Pay Components Defined for Employee

</td><td>

Retrieves recurring pay components and relevant information for the specified employee.

</td></tr><tr><td>

Get Required Fields - Creatable

</td><td>

Retrieves all the required insertable fields in the specified entity.

</td></tr><tr><td>

Get Time Types By User ID

</td><td>

Retrieves all the available time types of the specified employee in SAP SuccessFactors.

</td></tr><tr><td>

Get Updatable Todo Fields

</td><td>

Retrieves the list of updatable fields in the SuccessFactors Outbound Todos Staging table.

</td></tr><tr><td>

Look up Company Territory Code

</td><td>

Retrieves all available company territory codes from SAP SuccessFactors.

</td></tr><tr><td rowspan="5">

Record Management

</td><td>

Create Record

</td><td>

Creates a record in SuccessFactors.**Note:** The Create Record action displays non-navigable fields only in the creatable fields list.

</td></tr><tr><td>

Delete Record

</td><td>

Deletes the specified record in SuccessFactors.

</td></tr><tr><td>

Execute Entity By URL

</td><td>

Takes navigation URL as input and provides the response for that navigation URL.

</td></tr><tr><td>

Get Record

</td><td>

Retrieves the record for the selected entity and for the given key fields.

</td></tr><tr><td>

Update Record

</td><td>

Updates details of the specified record.

</td></tr><tr><td rowspan="4">

Todos

</td><td>

Create Todo

</td><td>

Create a to-do record in SuccessFactors.

</td></tr><tr><td>

Get Todo By ID

</td><td>

Get details of a to-do from SuccessFactors.

</td></tr><tr><td>

Retrieve Todos

</td><td>

Retrieves the to-do data from SuccessFactors, except those with Category ID as 57.

</td></tr><tr><td>

Update Todo

</td><td>

Updates details of the specified to-do record.

</td></tr><tr><td rowspan="6">

User Management

</td><td>

Look up User Activity

</td><td>

Retrieves the last activity time of your SAP SuccessFactors users.

</td></tr><tr><td>

Look up User Activity SFTP

</td><td>

Retrieves the last activity time of your SAP SuccessFactors users by fetching the report published on an SSH File Transfer Protocol \(SFTP\) location.

</td></tr><tr><td>

Look up Users

</td><td>

Retrieves the list of SAP SuccessFactors users.

</td></tr><tr><td>

Look up User by User ID

</td><td>

Retrieves the worker details of the SuccessFactors user.

</td></tr><tr><td>

Look up User Personal Details

</td><td>

Retrieves user personal details of the specified employee.

</td></tr><tr><td>

Suspend User

</td><td>

Suspends a user account.

</td></tr><tr><td rowspan="5">

Utility Category

</td><td>

Call A SuccessFactors Subflow

</td><td>

Executes the specified SuccessFactors spoke subflow synchronously.

</td></tr><tr><td>

Call Run SuccessFactors Service Subflow

</td><td>

Executes the Run SuccessFactors Service subflow asynchronously.

</td></tr><tr><td>

Check Flow Status

</td><td>

Checks if the context of flow is running.

</td></tr><tr><td>

Get Last Run Date

</td><td>

Retrieves the last run date and time of the flow.

</td></tr><tr><td>

Update Record In Outbound Todos Staging Table

</td><td>

Updates details of the specified to-do record in SuccessFactors Outbound Todos Staging Table.**Note:** Only an admin user can run this action.

</td></tr><tr><td>

Goal Management

</td><td>

Look up Goals by User ID

</td><td>

Retrieves goals information from SuccessFactors for the specified user ID.**Note:** Only an admin user can run this action.

</td></tr><tr><td>

Payroll Management

</td><td>

Look up Employee Payrolls

</td><td>

Retrieves payroll details of the specified employee.

</td></tr><tr><td rowspan="3">

Skill Management

</td><td>

Create or Update Skill Profile

</td><td>

Creates or updates skill profile and profile skill mappings for a particular employee.

</td></tr><tr><td>

Look up Employee Skills Stream

</td><td>

Retrieves the skill information of required employee.

</td></tr><tr><td>

Look up Skills Stream

</td><td>

Retrieves the skill information.

</td></tr><tr><td rowspan="8">

Job Management

</td><td>

Look up Attachment by ID

</td><td>

Retrieves attachment content and stores it in the SuccessFactors Attachments data source for the specified attachment ID.To access the attachments, navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources** and open the record **SuccessFactors Attachments**. The required files are attached to this data source record.

**Note:** Only an admin user can run this action.

</td></tr><tr><td>

Look up Candidate by ID

</td><td>

Retrieves candidate information from SuccessFactors for the specified candidate ID.**Note:** Only an admin user can run this action.

</td></tr><tr><td>

Look up Job Applications Stream

</td><td>

Retrieves job application information from SuccessFactors.**Note:** Only an admin user can run this action.

</td></tr><tr><td>

Look up Job Codes Stream

</td><td>

Retrieves job level, employment type, and job type information from SuccessFactors.**Note:** Only an admin user can run this action.

</td></tr><tr><td>

Look up Job Requisition by ID

</td><td>

Retrieves job requisition details for the specified requisition ID.**Note:**

-   Create a copy of the Lookup Job Requisition by ID action, if the API attribute of Job Level ID and Employment Type ID is configured with other custom attributes except customString3 and customString4, and modify the post-processing script with the expected API attribute path.
-   Only an admin user can run this action.

</td></tr><tr><td>

Look up Job Requisition Postings Stream

</td><td>

Retrieves job posting information from SuccessFactors.**Note:** Only an admin user can run this action.

</td></tr><tr><td>

Look up Employee Jobs Stream

</td><td>

Retrieves All Employee Jobs information from SuccessFactors.

</td></tr><tr><td>

Look up Job Profiles Stream

</td><td>

Retrieves job profiles information from SuccessFactors.

</td></tr></tbody>
</table>**Note:** If a spoke action requires date or time as an input, ensure that you provide the value in GMT time zone only.

## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See [Create an agentic workflow](https://www.servicenow.com/docs/access?context=configure-use-case-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See [Duplicate an AI agent](https://www.servicenow.com/docs/access?context=clone-ai-agent&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for more information about creating a clone.
-   See [Now Assist AI agents](https://www.servicenow.com/docs/access?context=na-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US) for information about AI agents.

|AI agent|Description|
|--------|-----------|
|SuccessFactors payroll management AI agent|Retrieves and manages payroll related information.|
|SuccessFactors user management AI agent|Retrieve detailed personal information of users.|
|SuccessFactors todos AI agent|Synchronizes, retrieves, manages, and creates todos.|
|SuccessFactors hr foundational data AI agent|Retrieves the holiday calendar.|
|SuccessFactors jobs management AI agent|Retrieves candidate information based on the ID.|
|SuccessFactors employee management AI agent|Retrieves and manages employee-related information such as, benefit information and time off details.|

There might be AI agents installed with the Now Assist application that are not used in agentic workflows. To learn how to see all agents that are available to you, see [Find AI agents](https://www.servicenow.com/docs/access?context=find-ai-agents&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Note:** Ensure that the user running an AI agent has the required roles and permissions to access data or perform operations on data in the table that is associated with the AI agent.

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see [Modify an agentic workflow](https://www.servicenow.com/docs/access?context=modify-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

<table id="table_jm1_mlv_c3c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Fetch User Details and Time‑Off Balance and Time‑Off Details

</td><td>

Retrieves a worker’s profile information along with their time‑off balance and time‑off details for a specified date. It is designed to help downstream processes access accurate HR and time‑management data from SuccessFactors.

</td><td>

-   SuccessFactors Employee Management AI Agent
-   SuccessFactors User Management AI Agent

</td><td>

No**Note:** To activate the workflow, see [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr><tr><td>

Fetch Employee Payrolls and Benefit Enrollments

</td><td>

Retrieves an employee’s payroll information and benefit enrollment details from SuccessFactors. It is intended for use cases requiring payroll validation, compensation planning, and benefits‑related decision support.

</td><td>

-   SuccessFactors Payroll Management AI Agent
-   SuccessFactors Employee Management AI Agent

</td><td>

No**Note:** To activate the workflow, see [Activate an agentic workflow template](https://www.servicenow.com/docs/access?context=activate-aia-use-case&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

</td></tr></tbody>
</table>## Spoke modules

The SuccessFactors spoke provides sample modules in the draft state to demonstrate automating the SuccessFactors tasks when events occur in ServiceNow. To customize a module, copy it to a new application scope. Available sample modules include:

<table id="table_qbq_m4n_5lb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Department Staging Table

</td><td>

Displays the department data retrieved from SuccessFactors.

</td></tr><tr><td>

Locations Staging Table

</td><td>

Displays the location data retrieved from SuccessFactors.

</td></tr><tr><td>

Job Profile Staging Table

</td><td>

Displays the job profile data retrieved from SuccessFactors.

</td></tr><tr><td>

Worker Profiles Staging Table

</td><td>

Displays the worker profile data retrieved from SuccessFactors.

</td></tr><tr><td>

Inbound Todos Staging Table

</td><td>

Displays the to-do records retrieved from SuccessFactors.

</td></tr><tr><td>

Outbound Todos Staging Table

</td><td>

Displays the todo records created in ServiceNow. When a todo record is created or updated in ServiceNow, the Create Todo or Update Todo flow is triggered and the same record is created or updated in SuccessFactors. All the associated record details, are retrieved from SuccessFactors and saved in this staging table. If the flow fails to create or update record in SuccessFactors, the associated record or updates in ServiceNow is also deleted.

</td></tr><tr><td>

Employee Job Information And History

</td><td>

Displays the job information and job history of all users.

</td></tr><tr><td>

View My Time Off Balance

</td><td>

Displays the time off balance of the logged-in user.

</td></tr><tr><td>

View My Time Off Details

</td><td>

Displays details of the time off requests of the logged-in user.

</td></tr><tr><td>

Webhook Registry

</td><td>

Displays the list of webhook registries. Admin must create webhook registry here. For more information, see [Set up webhook for the SuccessFactors spoke](../task/setup-sapsf-webhooks.md).

</td></tr><tr><td>

View My Time Card Details For Past 1 Month

</td><td>

Displays time card details of the previous one month for the logged-in user.

</td></tr><tr><td>

View My Worker Profile

</td><td>

Displays the worker profile details of the logged-in user.

</td></tr><tr><td>

View My Holiday Calendar

</td><td>

Displays the holiday calendar applicable to the logged-in user.

</td></tr><tr><td>

View My Reporting Structure

</td><td>

Displays the reporting structure details of the logged-in user.

</td></tr><tr><td>

View My Direct Deposit Information

</td><td>

Displays the direct deposit details of the logged-in user.

</td></tr><tr><td>

View My Total Rewards

</td><td>

Displays the total rewards of the logged-in user.

</td></tr></tbody>
</table>To retrieve the data, run Run SuccessFactors Integration Flow. The data in the staging tables is available for seven days. During this time period, you must use transform maps to save this data in the required target ServiceNow tables according to your requirement.

## Spoke transform maps

The SuccessFactors spoke provides sample transform maps in inactive state and associated sample target tables to demonstrate using transform maps to save SuccessFactors data in your ServiceNow tables. You can use these sample transform maps and target tables as reference to create transform maps according to your requirement.

For more information, see [Transform maps](../../../script/server-scripting/concept/c_CreatingNewTransformMaps.md).

## Spoke user roles

These user roles are available along with the spoke:

-   SuccessFactors Admin \(sn\_successfactors.SuccessFactors Admin\): If you have this role, you can access all spoke modules and tables.
-   SuccessFactors Private Data \(sn\_successfactors.SuccessFactors Private Data\): If you have this role, you can access to data in these spoke modules:
    -   View My Direct Deposit Information
    -   View My Total Rewards
-   SuccessFactors Public Data \(sn\_successfactors.SuccessFactors Public Data\): If you have this role, you can access to data in these spoke modules:
    -   View My Time Off Balance
    -   View My Time Off Details
    -   View My Time Card Details For Past 1 Month
    -   View My Worker Profile
    -   View My Holiday Calendar
    -   View My Reporting Structure

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

Two connection and credential aliases are available with the SuccessFactors spoke. One for the SOAP API and the other for the OData API.

For information about setting up the spoke, see [Set up the SuccessFactors spoke v4.x.x](../task/setup-successfactors.md#).


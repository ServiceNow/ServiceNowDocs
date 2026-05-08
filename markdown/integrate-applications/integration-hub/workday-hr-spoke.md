---
title: Workday HR Spoke
description: The Workday HR spoke is built by Bristlecone, Inc. Manage staffing, resources, payroll, benefits, and so on in the system from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 26
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday HR Spoke

The Workday HR spoke is built by Bristlecone, Inc. Manage staffing, resources, payroll, benefits, and so on in the system from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store website](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Workday HR spoke v2.11.1 is the latest version.

## Supported versions

This spoke was built for Workday HR SOAP Application Programming Interface \(API\) version v33.2 and REST API version v1, and is compatible until Workday HR SOAP API version v39.0.

## Required configurations in Workday

To set up the integration, you must initially perform this procedure in Workday:

1.  Register an Integration System User.

    **Note:** While filling account information details, confirm that you select the **Do Not Allow UI Sessions** check box.

2.  Create a security group and assign it to the integration system user.
    1.  In **Action**, navigate to **Security Group** &gt; **Maintain Domain Permissions for Security Group** and provide these permissions:

<table id="table_udc_wbj_qmb"><thead><tr><th>

Operation

</th><th>

Domain Security Policy

</th><th>

Domain Security Policies Inheriting Permission

</th><th>

Functional Areas

</th></tr></thead><tbody><tr><td>

View and Modify

</td><td>

WQL for Workday Extend

</td><td>

 

</td><td>

System

</td></tr><tr><td>

View and Modify

</td><td>

Workday Query Language

</td><td>

 

</td><td>

System

</td></tr><tr><td>

View Only

</td><td>

Worker Data: Active and Terminated Workers

</td><td>

 

</td><td>

Staffing

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Workers

</td><td>

 

</td><td>

Staffing

</td></tr><tr><td>

View Only

</td><td>

Reports: Manager

</td><td>

 

</td><td>

Staffing

</td></tr><tr><td>

View Only

</td><td>

Reports: Matrix Manager

</td><td>

 

</td><td>

Staffing

</td></tr><tr><td>

View and Modify

</td><td>

Business Process Administration

</td><td>

Business Process Delegation

</td><td>

System

</td></tr><tr><td>

View Only

</td><td>

Worker Data: Benefits

</td><td>

-   Worker Data: Beneficiaries and Dependents
-   Worker Data: Benefit Annual Credit
-   Worker Data: Benefit Eligibility
-   Worker Data: Benefits Annual Rate
-   Worker Data: Court Order Details
-   Worker Data: Retirement Details
-   Worker Data: Wellness


</td><td>

-   Benefits
-   Personal Data


</td></tr><tr><td>

View Only

</td><td>

Reports: Learning Record

</td><td>

 

</td><td>

Learning Core

</td></tr><tr><td>

View Only

</td><td>

Worker Data: Funded Plan Assignments

</td><td>

 

</td><td>

Advanced Compensation

</td></tr><tr><td>

View Only

</td><td>

Business Process Reporting

</td><td>

 

</td><td>

System

</td></tr><tr><td>

View Only

</td><td>

Workday Accounts

</td><td>

 

</td><td>

System

</td></tr><tr><td>

View Only

</td><td>

Person Data: Gender

</td><td>

 

</td><td>

Personal Data

</td></tr><tr><td>

View Only

</td><td>

Manage: Organization Roles

</td><td>

 

</td><td>

Organizations and Roles

</td></tr><tr><td>

View Only

</td><td>

Person Data: Work Address

</td><td>

 

</td><td>

Contact Information

</td></tr><tr><td>

View Only

</td><td>

Person Data: Home Phone

</td><td>

 

</td><td>

Contact Information

</td></tr><tr><td>

View Only

</td><td>

Person Data: Work Phone

</td><td>

 

</td><td>

Contact Information

</td></tr><tr><td>

Get and Put

</td><td>

Manage: Payment Election

</td><td>

 

</td><td>

Expenses

</td></tr><tr><td>

Get and Put

</td><td>

Person Data: Personal Data

</td><td>

-   Person Data: Ethnicity Visual Survey
-   Person Data: Licenses
-   Person Data: Other IDs
-   Person Data: Passports and Visas
-   Worker Data: Tobacco Use


</td><td>

Personal Data

</td></tr><tr><td>

Get and Put

</td><td>

Worker Data: Payroll \(Payment Elections\)

</td><td>

 

</td><td>

Core Payroll

</td></tr><tr><td>

Get and Put

</td><td>

Worker Data: Payroll Interface \(Payment Elections\)

</td><td>

 

</td><td>

Payroll Interface

</td></tr><tr><td>

Get and Put

</td><td>

Worker Data: Beneficiaries

</td><td>

-   Worker Data: Beneficiary Additional Address
-   Worker Data: Beneficiary Additional email
-   Worker Data: Beneficiary Additional Instant Messenger
-   Worker Data: Beneficiary Additional Phone
-   Worker Data: Beneficiary Additional Web Address
-   Worker Data: Beneficiary Date of Birth
-   Worker Data: Beneficiary Gender
-   Worker Data: Beneficiary Government IDs
-   Worker Data: Beneficiary National IDs
-   Worker Data: Beneficiary Other IDs
-   Worker Data: Beneficiary primary Address
-   Worker Data: Beneficiary Primary email
-   Worker Data: Beneficiary Primary Instant Messenger
-   Worker Data: Beneficiary primary Phone
-   Worker Data: Beneficiary Primary Web Address


</td><td>

Benefits

</td></tr><tr><td>

Get and Put

</td><td>

Process: Import Time Blocks

</td><td>

 

</td><td>

-   Time Tracking
-   Time Tracking Hub


</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Current Staffing Information

</td><td>

 

</td><td>

Staffing

</td></tr><tr><td>

Get Only

</td><td>

Set Up: Calendar

</td><td>

 

</td><td>

System

</td></tr><tr><td>

Get Only

</td><td>

Job Information

</td><td>

 

</td><td>

Jobs &amp; Profile

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Payroll \(Income Withholding Orders\)

</td><td>

 

</td><td>

Core Payroll

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Payroll \(Income Withholding Orders\) - CAN

</td><td>

 

</td><td>

CAN Payroll

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Payroll \(Company Specific\) - USA

</td><td>

 

</td><td>

USA Payroll

</td></tr><tr><td>

Get Only

</td><td>

Manage: Location

</td><td>

Location: View

</td><td>

Organizations and Roles

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Benefits

</td><td>

-   Worker Data: Beneficiaries and Dependents
-   Worker Data: Benefit Annual Credit
-   Worker Data: Benefit Eligibility
-   Worker Data: Benefits Annual Rate
-   Worker Data: Court Order Details
-   Worker Data: Retirement Savings
-   Worker Data: Wellness


</td><td>

-   Benefits
-   Personal Data


</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Project time sheet and Worksheet

</td><td>

 

</td><td>

Project Tracking

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Public Worker Reports

</td><td>

 

</td><td>

Staffing

</td></tr><tr><td>

Get Only

</td><td>

Payroll Interface

</td><td>

 

</td><td>

Payroll Interface

</td></tr><tr><td>

Get Only

</td><td>

Reports: Pay Calculation Results for Worker

</td><td>

-   Reports: Pay Calculation Results for Worker \(Audits\)
-   Reports: Pay Calculation Results for Worker \(Payslips\)
-   Reports: Pay Calculation Results for Worker \(Results\)


</td><td>

Core Payroll

</td></tr><tr><td>

Get Only

</td><td>

Manage: Organization Integration

</td><td>

 

</td><td>

Organizations and Roles

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Benefit Elections

</td><td>

 

</td><td>

-   Benefits
-   Personal Data


</td></tr><tr><td>

Get Only

</td><td>

Person Data: Emergency Contacts

</td><td>

 

</td><td>

Contact Information

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Edit and Delete Worker Documents

</td><td>

 

</td><td>

Personal Data

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Compensation by Organization

</td><td>

 

</td><td>

Core Compensation

</td></tr><tr><td>

Get Only

</td><td>

Integration Build

</td><td>

 

</td><td>

Integration

</td></tr><tr><td>

Get Only

</td><td>

Worker Data: Time Off \(Time-Off Balances\)

</td><td>

 

</td><td>

Time Off and Leave

</td></tr><tr><td>

Get Only

</td><td>

Person Data: Personal Information

</td><td>

 

</td><td>

Personal Data

</td></tr><tr><td>

View Only

</td><td>

Worker Data: Public Worker Reports

</td><td>

 

</td><td>

Staffing

</td></tr><tr><td>

View Only

</td><td>

Integration Security

</td><td>

 

</td><td>

Integration

</td></tr><tr><td>

Get and Put

</td><td>

Integration Event

</td><td>

 

</td><td>

Integration

</td></tr></tbody>
</table>        **Note:** Ensure that the domain security policies are activated for the security group.

    2.  Configure the business process policies of your security group and provide these permissions:

<table id="table_stn_smk_qmb"><thead><tr><th>

Operation

</th><th>

Business Process Type

</th><th>

Functional Area

</th></tr></thead><tbody><tr><td>

Initiate \(Assign Roles \(web service\)\)

</td><td>

Assign Roles

</td><td>

Organizations and Roles

</td></tr><tr><td>

Initiate \(Change Organization Assignments \(web service\)\)

</td><td>

Change Organization Assignments for Worker

</td><td>

Organizations and Roles

</td></tr><tr><td>

Initiate \(Maintain Contact Information \(Web Service\)\)

</td><td>

Contact Change

</td><td>

Contact Information

</td></tr><tr><td>

Initiate \(Add Dependent \(web service\)\)

</td><td>

Dependent Event

</td><td>

-   Benefits
-   Personal Data


</td></tr><tr><td>

Initiate \(Edit Worker Additional Data \(Web Service\)\)

</td><td>

Edit Worker Additional Data Event

</td><td>

Staffing

</td></tr><tr><td>

Initiate \(Change Legal Name \(Web Service\)\)

</td><td>

Legal Name Change

</td><td>

Contact Information

</td></tr><tr><td>

Initiate \(No Show \(Web Service\)\)

</td><td>

No Show

</td><td>

Staffing

</td></tr><tr><td>

Initiate \(Change Personal Information \(Web Service\)\)

</td><td>

Personal Information Change

</td><td>

Personal Data

</td></tr><tr><td>

Initiate \(Request Leave of Absence \(Web Service\)\)

</td><td>

Request Leave of Absence

</td><td>

Time Off and Leave

</td></tr><tr><td>

Initiate \(Enter Time off \(Web Service\)\)

</td><td>

Request Time Off

</td><td>

Time Off and Leave

</td></tr><tr><td>

Initiate \(Terminate Employee \(Web Service\)\)

</td><td>

Termination

</td><td>

Staffing

</td></tr></tbody>
</table>        **Note:** Confirm that the business process security policies are activated for the security group.


**Note:** If you have installed spoke v1, uninstall it and install the spoke v1.1.

## Spoke dependencies

If you’re having trouble installing the app, confirm that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   Complex Object \(com.glide.cobject\)
-   System Import Data Source \(glide.system\_import\_data\_source\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Workday HR spoke provides a sample flow, Verify User Sample Flow that demonstrates automating the Workday tasks. This flow calls the subflow with the same name to verify if the user who raised the request is a valid user in the Workday system. To customize a sample flow, copy it to a new application scope.

## Spoke subflows

The Workday HR spoke provides sample subflows to demonstrate automating Workday HR tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Verify User Subflow|Verifies if the user who raised request is a valid user in Workday system.|
|Get WID For Worker|Retrieves WID details of the employee using the Look up Worker Profile action.|
|Create User|Creates a user in the ServiceNow when the user is onboarded in the Workday system. To use this subflow, you should [Set up webhooks for your Workday HR spoke](../task/setup-webhook-wd-hr-spoke.md#).|
|Leave of absence|Retrieves the leave of absence details of an employee from Workday using the LeaveofAbsence Webhook.|
|Deactivate User|Deactivates an user in Workday using the Workday Deactivate User webhook.|
|Look up job Requisition|Retrieves all the existing job requisition information from Workday application into Job Requisition table.|
|Update Job Requisition|Retrieves the changes made to the existing job requisition in Workday using the UpdateJobRequisition webhook and stores the changes in the Job Requisition table.|
|Look up Using WQL Stream|Retrieves Workday HR data using a WQL \(Workday Query Language\) stream query.|
|Sample Sequences to Make a WQL Call|Constructs a Workday Query Language \(WQL\) query based on the specified inputs.|

## Spoke actions that use Workday SOAP APIs

Workday itself organizes its APIs into two major categories: SOAP Public API and REST API. Thus, the Workday HR spoke also reflects the same. You can use the spoke by using one of these two APIs, but not necessarily both, depending on the spoke actions you must use.

The Workday HR spoke provides actions to automate Workday tasks when events occur in your ServiceNow instance. Available actions include:

**Note:** The SOAP-based actions use the Workday SOAP web services and require you to perform the configurations mentioned in [Configurations to use Workday SOAP Basic Auth with WS-Security](../task/soap-wd-hr-spoke.md#).

|Actions that use the Workday SOAP APIs|
|Category|Action|Description|
|--------------------------------------|
|--------|------|-----------|
|Default|Look up Skills|Retrieves the details of the skills from Workday.|
|Absence Management|Get Time off Balances By Employee ID|Retrieves details of the time off plan balance for the specified employee.|
|Look up Time Off Balance|Retrieves details of the time off balance, based on the provided filter criteria.|
|Request Leave Of Absence|Creates a long leave absence request or updates an existing request.|
|Request Time Off|Creates a short-term leave request.|
|Approval Management|Approve Business Process|Approves the specified business process in Workday.|
|Reject Business Process|Rejects the specified business process in Workday.|
|Benefits Administration|Add Dependent|Adds a dependent to the specified worker.|
|Change Beneficiaries|Updates beneficiary details of the specified worker.|
|Cash Management|Update Direct Deposit Information|Updates details of the current payment elections.|
|Metadata Retrieval|Get Additional Workday Fields|Retrieves all additional fields for each action.|
|Get Custom Dynamic Input Fields|Retrieves all custom dynamic input fields.|
|Get Custom Dynamic Output Fields|Retrieves all custom dynamic output fields.|
|Get Object For Custom Dynamic Fields|Retrieves object for the specified custom dynamic field.|
|Get Parent Object For Custom Dynamic Fields|Retrieves parent object for the specified custom dynamic field.|
|Get Reference ID List|Retrieves values of the Reference ID, based on its reference type.|
|Get References WID|Retrieves reference IDs for the specified reference type.|
|Get Access Token|Retrieves the access tokens for authenticating SOAP-based actions using OAuth 2.0.|
|Get Dynamic Response Schema|Retrieves the output schema for the specified query from Workday.|
|Payroll Management|Get My Tax Withholding Information Canada By Employee ID|Retrieves all types of income withholding orders from Canada for the specified employee.|
|Get My Tax Withholding Information US By Employee ID|Retrieves all types of income withholding orders from US for the specified employee.|
|Get Payroll Federal W4 Tax Elections By Employee ID|Retrieves federal W-4 tax election data for the specified employee.|
|Get Payroll Payee FUTAs By Employee ID|Retrieves FUTA tax election data for the specified employee.|
|Get Payroll USA And Local Tax Elections By Employee ID|Retrieves information about the tax elections for state and local tax authorities, for the specified employee.|
|Look up Direct Deposit Information Details|Retrieves information about the specified payee, who belongs to an external pay group.|
|Look up Payroll Federal W4 Tax Elections|Retrieves the federal W-4 tax election details for the required employees, based on the provided filter criteria.|
|Look up Payroll Payee FUTAs Details|Retrieves the payroll payee FUTA details for the required employees, based on the provided filter criteria.|
|Look up Payroll Results|Retrieves payroll results for the required employees, based on the provided filter criteria.|
|Look up Payroll USA And Local Tax Elections|Retrieves details of worker tax elections for state and local tax authorities for the required employees, based on the provided filter criteria.|
|Look up Tax Elections Ongoing Work Jurisdiction Details|Retrieves details of the ongoing work jurisdiction tax election for the required employees, based on the provided filter criteria.|
|Look up Tax Withholding Information Details Canada|Retrieves all types of income withholding orders from Canada for the required employees, based on the provided filter criteria.|
|Look up Tax Withholding Information Details US|Retrieves all types of income withholding orders from US for the required employees, based on the provided filter criteria.|
|Resource Management|Change Legal Name|Changes or sets the legal name for the specified employee.|
|Change Personal Information|Changes the personal information of the specified employee.|
|Get Employee Documents By Employee ID|Retrieves documents of the specified employee.|
|Get My Compensation Details By Employee ID|Retrieves the compensation details of the specified employee.|
|Get My Contact Details By Employee ID|Retrieves contact information of the specified employee, such as address, phone number, email address, and beneficiaries.|
|Get My Org Structure By Employee ID|Retrieves details of the org structure for the specified employee.|
|Get Total Benefit Enrollments By Employee ID|Retrieves details of the benefit enrollments for the specified employee.|
|Get Total Rewards By Employee ID|Retrieves details of the total rewards for the specified employee.|
|Look up Compensation Details|Retrieves compensation details for the required employees, based on filter criteria.|
|Look up Contact Details|Retrieves contact details for the required employees, such as address, phone number, email address, and beneficiaries, based on filter criteria.|
|Look up Employee Documents|Retrieves documents of the required employees, based on the filter criteria.|
|Look up Holiday Calendars|Retrieves the details of the holiday calendars.|
|Look up Job Profiles|Retrieves details of the job profile, based on the specified criteria.|
|Look up Location Details|Retrieves location details, based on the specified criteria.|
|Look up Organizations|Retrieves details of the organizations, based on the provided filter criteria.|
|Look up Timesheet Details|Retrieves details of the timesheets, based on the provided filter criteria.|
|Look up Total Benefit Enrollments|Retrieves details of the benefit enrollments, based on the provided filter criteria.|
|Look up Total Rewards|Retrieves details of the employee rewards, based on the provided filter criteria.|
|Look up Work Schedule Calendars|Retrieves details of the work schedule calendars.|
|Look up Worker Job History Report|Retrieves the job history of a worker.|
|Look up Worker Profile|Retrieves details of the employee profiles, based on worker type.|
|Look up Workers|Retrieves details such as, first name, last name, address, phone number, email address, instant messenger, worker position, and management chain, based on the provided filter criteria.|
|Look up Workers Employment Data|Retrieves details such as, position, position organizations, position management chains, and worker status, based on the provided filter criteria.|
|Update My Address|Updates employees details, such as address, phone number, email address, instant messenger, and web address.|
|Look up Workers And Employment Info|Retrieves worker profile information from Workday.|
|Look up Professional Profiles Stream|Retrieves professional workers profile information from Workday.|
|Staffing|Change Organization|Assigns values for company, cost center, region, and so on that are configured for staffing usage to a filled position.|
|Change Roles|Changes roles of the specified employee.|
|No Show|Rescinds the hiring process if a hired employee doesn't show on joining date.|
|Offboard Employee|Offboards the specified employee.|
|Hire Employee|Hires a user as an employee to the specified job.|
|Set Hiring Restrictions|Creates hiring restrictions for a job management supervisory organization.|
|Create Position|Creates or opens a position for a supervisory organization using the position management staffing model.|
|Look up Positions|Retrieves position-related details based on the position ID from Workday.|
|Edit Position|Edits a position that is already filled.|
|Edit Hiring Restrictions|Edits the hiring restrictions for a job management supervisory organization.|
|Change Job|Changes the job of an employee or a contingent worked. The types of changes include transfer, promotion, demotion, lateral moves, and any other change in the information on the job.|
|Close Position|Closes a position.|
|Contract Contingent Worker|Hires a user to a contingent position or job.|
|Talent Management|Create External Skill|Creates a new external skill in Workday and associates it with the specified skill vendor.|
|Look up External Skills Mapping Stream|Retrieves the external skill mapping records from Workday for the specified skill vendor or mapping criteria.|
|Look up User Skills Stream|Retrieves skill details for a specified employee from Workday, including associated skills and proficiency attributes.|
|Manage External Skill Mapping|Manages external skill mapping records in Workday, including creating, updating, or removing skill associations.|
|Update User Skill Proficiency|Updates the proficiency level of a specified user skill in Workday.|
|Time Tracking|Update Reported Time Blocks|Updates details of reported time blocks.|
|Skill Management|Manage Employee Skills|Adds or removes skills associated with an employee.|
|Look up Employee Skills|Retrieves employees skills from Workday for the specified date range.|
|Jobs Management|Create Job Requisition|Creates a job requisition in Workday.|
|Look up Candidates Stream|Retrieves the candidates information like candidate data, social media account data and others from Workday.|
|Look up Compensation Grades Stream|Retrieves compensation details like the default minimum and maximum of the compensation pay range and others from Workday.|
|Look up Job Postings Stream|Retrieves job post details like job posting title, job posting description, education data, certification data, and others from Workday.|
|Look up Job Requisitions Stream|Retrieves job requisition details like recruiting start date, target hire date and others from Workday.|
|Update Job Requisition|Updates the specified job requisition.|

## Spoke actions that use Workday REST APIs

Workday itself organizes its APIs into two major categories: SOAP Public API and REST API. Thus, the Workday HR spoke also reflects the same. You can use the spoke by using one of these two APIs, but not necessarily both, depending on the spoke actions you must use.

The Workday HR spoke provides actions to automate Workday tasks when events occur in your ServiceNow instance. Available actions include:

**Note:** The REST-based actions use the Workday REST API and requires you to perform the configurations mentioned in [Configurations to use Workday REST API](../task/rest-wd-hr-spoke.md#).

<table id="table_hxw_3rc_gxb"><thead><tr><th colspan="3">

Actions that use the Workday REST APIs

</th></tr><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Absence Management

</td><td>

Look up Worker Time Off and Leave Of Absence Request

</td><td>

Retrieves the time off and leave of absence details of the worker using RaaS report.**Important:** Before executing this action, you must set up a report. When you execute the action, it calls the report and the data is sent from Workday HR to your ServiceNow instance. To set up the report, see .

</td></tr><tr><td>

Approval Management

</td><td>

Look up In-Progress Approval Requests

</td><td>

Retrieves the approval requests that are in progress from Workday for the specified date range.

</td></tr><tr><td rowspan="3">

Custom Actions**Note:** To use these action, you must create a record in the Workday Custom Objects \[x\_snc\_sn\_workday\_s\_workday\_custom\_objects\] table and provide these details:

-   Parent Object WS Alias
-   Extension Object WS Alias
-   Extension Object Fields
-   Extension Object Field Data Type
-   Field Type

</td><td>

Look up Object Custom Fields

</td><td>

Retrieves data relevant to the specified custom object.

</td></tr><tr><td>

Look up Custom Reports

</td><td>

Retrieves the custom reports.

</td></tr><tr><td>

Update Object Custom Fields

</td><td>

Updates fields in the specified custom object.

</td></tr><tr><td>

Payroll Management

</td><td>

Look up Payslip

</td><td>

Retrieves payslip details of the specified employee.

</td></tr><tr><td>

Goals Management

</td><td>

Look up Employee Goals

</td><td>

Retrieves the employee goals from Workday.

</td></tr><tr><td>

Feedback Management

</td><td>

Look up Feedback Received

</td><td>

Retrieves the feedback requests from Workday.

</td></tr><tr><td rowspan="4">

Performance Management

</td><td>

Look up Employee Latest Performance Review

</td><td>

Pulls the latest performance review of the employee from Workday.**Important:** Before executing this action, you must set up a report. When you execute the action, it calls the report and the data is sent from Workday HR to your ServiceNow instance. To set up the report, see [Configure the Employee Latest Performance Review report](../task/configure-employee-latest-performance-review-report.md).

</td></tr><tr><td>

Look up Employee Performance Review Historical Data

</td><td>

Pulls the historical data on the employee performance review Workday.**Important:** Before executing this action, you must set up a report. When you execute the action, it calls the report and the data is sent from Workday HR to your ServiceNow instance. To set up the report, see [Configure the Worker's Historical Performance Review report](../task/configure-the-workers-historical-performance-review-report.md).

</td></tr><tr><td>

Look up Succession Planning

</td><td>

Pulls the succession planning from Workday.**Important:** Before executing this action, you must set up a report. When you execute the action, it calls the report and the data is sent from Workday HR to your ServiceNow instance. To set up the report, see [Configure Succession Planning Report](../task/configure-succession-planning-report.md).

</td></tr><tr><td>

Look up Succession Pool

</td><td>

Pulls the succession pool from Workday.**Important:** Before executing this action, you must set up a report. When you execute the action, it calls the report and the data is sent from Workday HR to your ServiceNow instance. To set up the report, see [Configure Succession Pool report](../task/configure-succession-pool-report.md).

</td></tr><tr><td rowspan="2">

Skill Management

</td><td>

Look up Employee Skills

</td><td>

Retrieves employee skills from Workday for specified date range.**Important:** You must create report in Workday instance to use this action.

-   For more information about extracting workers skill with skill cloud, see [Extract workers skill \(with the skill cloud\)](../task/wd-worker-skill-with-cloud.md).
-   For more information about extracting workers skill without skill cloud, see [Extract workers skill \(without the skill cloud\)](../task/wd-worker-skill-without-cloud.md).

</td></tr><tr><td>

Look up Skills

</td><td>

Retrieves skills from Workday.**Important:** You must create report in Workday instance to use this action. For more information, see [Create report to extract skills](../task/wd-hr-lookup-skills.md).

</td></tr><tr><td rowspan="8">

Resource Management

</td><td>

Get My Reporting Structure

</td><td>

Retrieves details of the reporting structure for the specified employee.

</td></tr><tr><td>

Look up Holiday Calendars Of An Employee

</td><td>

Retrieves details of the holiday calendar for the specified employee.

</td></tr><tr><td>

Look up Holiday Calendars Reference WID Of An Employee

</td><td>

Retrieves details of the holiday calendar WID for the specified employee.

</td></tr><tr><td>

Look up Inbox Items

</td><td>

Retrieves inbox items from Workday for the specified date range.

</td></tr><tr><td>

Look up Merit And Benefit Plan Details Of An Employee

</td><td>

Retrieves details of merit and benefit plan for the required employees, based on the provided filter criteria.

</td></tr><tr><td>

Look up Schedule Calendars Reference WID Of An Employee

</td><td>

Retrieves work schedule calendars for the required employees.

</td></tr><tr><td>

Look up Total Rewards using Report

</td><td>

Retrieves the total rewards for the specified report owner and report.

</td></tr><tr><td>

Look up Using WQL Stream

</td><td>

Retrieves Workday HR data using a WQL \(Workday Query Language\) stream query.

</td></tr><tr><td rowspan="6">

Metadata Retrieval

</td><td>

Look up Data Source

</td><td>

Retrieves details for the specified Workday data source.

</td></tr><tr><td>

Look up Data Source Field

</td><td>

Retrieves a specific field for the selected data source and includes the related business object information.

</td></tr><tr><td>

Look up Data Source Fields Stream

</td><td>

Retrieves all fields for the specified data source, including their related business objects.

</td></tr><tr><td>

Look up Data Source Filter

</td><td>

Retrieves details for a specific data source filter, including required and optional parameters.

</td></tr><tr><td>

Look up Data Source Filters Stream

</td><td>

Retrieves all available filters for the specified Workday data source.

</td></tr><tr><td>

Look up Data Sources Stream

</td><td>

Retrieves all available data sources from Workday.

</td></tr><tr><td>

Attachment Management

</td><td>

Download Workday RAAS CSV

</td><td>

Downloads a specified Workday RAAS report in CSV format and attaches it to the selected data source.

</td></tr></tbody>
</table>## Available AI agents

Install Now Assist for Integration Hub and start using the available AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

This spoke provides standalone AI agents that mimic human-like intelligence to perform tasks in your ServiceNow instance.

-   In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. See Create an agentic workflow for information about adding AI agents to create agentic workflows as per your requirement and provide the required trigger.

    You can also search for other available AI agents and add them to your agentic workflow. See Find AI agents for more information.

-   You can create a clone of the required spoke AI agent and customize it as per your requirement. See Duplicate an AI agent for more information about creating a clone.
-   See Now Assist AI agents for information about AI agents.

|AI Agent|Description|
|--------|-----------|
|Workday HR Feedback Management AI Agent|Manages feedback retrieval and review workflows within Workday. This AI agent enables users to access employee feedback, support performance discussions, and streamline HR decision-making through seamless integration with Workday.|
|Workday HR Approval Management AI Agent|Manages approval workflows and business process decisions within Workday. This AI agent enables users to approve or reject requests, track approval statuses, and optimise HR operations through direct Workday integration.|
|Workday HR Goals Management AI Agent|Manages employee goal tracking and review processes within Workday. This AI agent enables users to look up goals, monitor progress, and support HR conversations through efficient Workday integration.|
|Workday HR Performance Management AI Agent|Manages performance review and succession planning workflows within Workday. This AI agent enables users to retrieve reviews, analyse historical data, and access succession pools for informed HR decision-making.|
|Workday HR Absence Management AI Agent|Manages absence and leave workflows within Workday. This AI agent enables users to look up time off balances, process leave requests, and manage absence data for streamlined HR operations.|
|Workday HR Payroll Management AI Agent|Manages payroll and tax information workflows within Workday. This AI agent enables users to retrieve payslips, access tax details, and manage payroll data for efficient HR and payroll operations.|
|Workday HR Resource Management AI Agent|Manages employee data and organisational resource workflows within Workday. This AI agent enables users to retrieve employee information and manage organisational details for effective HR resource management.|

## Available sample agentic workflows

Install Now Assist for Integration Hub and start using the available sample agentic workflows and AI agents. For more information, see [Now Assist for Integration Hub](../../integrationhub/concept/now-assist-spokes.md).

In the ServiceNow agentic system, you can create an agentic workflow that comprises of a set of large language model \(LLM\) instructions along with one or more standalone AI agents to execute an objective. Use the available sample agentic workflow in AI Agent Studio so that AI agents can coordinate to solve complex problems. To modify the available sample agentic workflow as per your requirement, see Modify an agentic workflow.

<table id="table_emr_pyw_c3c"><thead><tr><th>

Sample agentic workflow

</th><th>

Description

</th><th>

AI agents used

</th><th>

Always ON by default?

</th></tr></thead><tbody><tr><td>

Fetch Employee Profile, Rewards Details, and Latest Performance Review

</td><td>

Retrieves an employee’s profile information, rewards details, and latest performance review data from Workday. This workflow consolidates multiple reports and endpoints to provide a unified view of a worker’s employment, rewards history, and performance feedback.

</td><td>

-   Workday HR performance management AI agent
-   Workday HR resource management AI agent

</td><td>

No**Note:** To activate the workflow, see Activate an agentic workflow template.

</td></tr><tr><td>

Fetch Employee Time Off and Holiday Calendar

</td><td>

Retrieves employee‑specific time‑off information along with the applicable holiday calendar. This workflow returns a summary of approved leave, pending time‑off entries, and holidays relevant to the employee’s assigned region or work schedule.

</td><td>

-   Workday HR absence management AI agent
-   Workday HR resource management AI agent

</td><td>

No**Note:** To activate the workflow, see Activate an agentic workflow template.

</td></tr></tbody>
</table>## Spoke modules

The Workday HR spoke adds the Workday application to your instance and includes these modules:

**Important:** The remote tables, View my Total rewards \[sn\_workday\_hr\_spke\_st\_get\_payroll\_results\] and Get Payroll Results \[sn\_workday\_hr\_spke\_st\_view\_my\_total\_rewards\], store sensitive data. Hence, discretion is advised before you give users the permission to view data stored in these tables.

<table id="table_j3m_pnh_pmb"><thead><tr><th>

Module

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Details

</td><td>

Contains information about the base URL of the Workday instance or tenant, and API version.

</td></tr><tr><td>

Custom Objects

</td><td>

To use the custom actions, create a record in the Custom Objects module and provide these details:-   Parent Object WS Alias
-   Extension Object WS Alias
-   Extension Object Fields
-   Extension Object Field Data Type
-   Field Type

</td></tr><tr><td>

Get My Holiday Calendar

</td><td>

Sample remote table that you should customise to retrieve details of the holiday calendar for the logged in employee. From the Get My Holiday Calendar remote table definition, the Get My Holiday Calendar action is called to retrieve the data.

</td></tr><tr><td>

Get Payroll Results

</td><td>

Sample remote table that you should customise to retrieve the payroll information. From the Get Payroll Results remote table definition, the Look up Payroll Results action is called to retrieve the data.**Important:** This remote table stores sensitive data. Hence, discretion is advised before you give users the permission to view data stored in these tables.

</td></tr><tr><td>

RAAS Report Access Details

</td><td>

To use actions based on Workday Report as a Service API, create a record in the RAAS Report Access Details module and provide details of the ServiceNow user along with the Workday report owner name and Workday report name. Confirm that the user is entitled to access these reports.Create a record and fill in these values:

-   **User ID**: User ID of the ServiceNow user, who is entitled to access the required reports.
-   **Report Name**: Name of the RAAS API while configuring it in Workday system.
-   **Report Owner Username**: Username of the RAAS owner.

</td></tr><tr><td>

Remote Table Configurations

</td><td>

An entry of column and table name that consists of Workday employee ID of the logged-in user should be made into this table. For example, Employee Number column of the User Table. That is, **Table Name** is `sys_user` and **Field Name** is `employee_number`.

**Note:** Confirm that you provide the internal name of the table and field.

</td></tr><tr><td>

View My Direct Deposit Information

</td><td>

Sample remote table that you should customize to retrieve the direct deposit information. From the View My Direct Deposit Information remote table definition, the Look up Direct Deposit Information Details action is called to retrieve the data.

</td></tr><tr><td>

View My Total Rewards

</td><td>

Sample remote table that you should customise to retrieve the total rewards for a logged in employee. From the View My Total Rewards remote table definition, the Look up Total Rewards action is called to retrieve the data.**Important:** This remote table stores sensitive data. Hence, discretion is advised before you give users the permission to view data stored in these tables.

</td></tr><tr><td>

View Time Off Balance

</td><td>

Sample remote table that you should customize to retrieve the time off balance for a logged in employee. From the View Time Off Balance remote table definition, the Look up Time Off Balance action is called to retrieve the data.

</td></tr><tr><td>

Webhook Registry

</td><td>

Contains records of webhooks registries. Admin should create record here to [Set up webhooks for your Workday HR spoke](../task/setup-webhook-wd-hr-spoke.md#) for the required Workday HR event.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see Connections and Credentials.


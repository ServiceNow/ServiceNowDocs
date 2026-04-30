---
title: Quick start tests for Customer Service Management
description: Quick start tests are part of the Automated Test Framework \(ATF\). Use these tests to validate that the Customer Service Management application still works after you make any configuration change, such as applying an upgrade or developing an application.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 14
breadcrumb: [Administer, Customer Service Management]
---

# Quick start tests for Customer Service Management

Quick start tests are part of the Automated Test Framework \(ATF\). Use these tests to validate that the Customer Service Management application still works after you make any configuration change, such as applying an upgrade or developing an application.

A quick start test is a test or test suite installed with the demo data of an application. You can use quick start tests as templates to build your own tests and test suites that ensure successful execution with your instance-specific data.

For more information about using quick start tests, see the following topics:

-   [Test your apps with the ATF](https://www.servicenow.com/docs/access?context=automated-test-framework&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Getting started with quick start tests](https://www.youtube.com/watch?v=wV0SjY5gq8M)

## CSM test suites and tests

The CSM test suites and tests are listed in the tables below.

-   CSM: Case management test suite
-   CSM Configurable Workspace test suite
-   CSM: Case Types - Complaint
-   CSM: Case Types - Onboarding
-   CSM: Operations Dashboard test suite
-   CSM Portal test suite
-   Guided Decision - Next Best Action ATF test suite
-   TC: Targeted Communications test suite
-   CSM Walkup Experience tests

## Plugins

All Customer Service Management quick start tests require activating the Customer Service Management Demo Data plugin \(com.snc.customerservice.demo\). Some quick start tests also require activating the following plugins:

-   Business Location \(com.snc.business\_location\)
-   Case Playbook for Complaints \(sn\_complaint\)
-   Case Playbook for Onboarding \(sn\_onboarding\)
-   Consumer Service Portal \(com.glide.service-portal.consumer-portal\)
-   CSM Contributor User \(com.snc\_csm\_contributor\_user\)
-   CSM Extension for Proxy Contacts \(com.snc.csm\_proxy\_contacts\)
-   Customer Service Household \(com.snc.household\)
-   Customer Service Management for Orders \(com.snc.csm.order\)
-   Customer Service Portal \(com.glide.service-portal.customer-portal\)
-   Customer Service with Request Management \(com.sn\_cs\_sm\_request\)
-   Customer Service with Service Management \(com.sn\_cs\_sm\)
-   Guided Decisions Experience \(com.snc.guided\_decisions\_playbook\_experience\)
-   Guided Decision - Next Best Action \(com.snc.next\_best\_action\)
-   Major Issue Management \(com.sn\_majorissue\_mgt\)
-   Proactive Customer Service Operations with Event Management \(com.snc.proactive\_cs\_itom\)
-   Skill Determination \(com.snc.skill\_determination\)
-   UX ATF Action \(com.glide.ux.atf\_action\)
-   Walk-Up for CSM \(com.snc.walkup\_for\_csm\)

<table id="table_udf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

CSM: Create Product Case

</td><td>

Create a case for a product.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Assign Case to an Agent

</td><td>

Create a case and assign it to a customer service agent.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Assign Asset on Case

</td><td>

Assign an asset to a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Assign Entitlement

</td><td>

Assign an entitlement to a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Escalate an Account

</td><td>

Escalate an account.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Escalate a Case

</td><td>

Escalate a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Create Special Handling Notes

</td><td>

Create special handling notes for a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Close a Case

</td><td>

Close a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Time Recording

</td><td>

Record the time worked on a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Create CHG from Case

</td><td>

Create a change record from a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Create Incident from Case

</td><td>

Create an incident record from a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Create Order Case

</td><td>

Create a case for an order. **Note:** Requires Customer Service Management for Orders.

</td><td>

Madrid

</td></tr><tr><td>

CSM - Create Order Case as Customer from CSM Portal

</td><td>

Create an order case as a customer from the Customer Service Portal. **Note:** Requires the Customer Service Portal. Also requires that the test be run as admin.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Create Problem from Case

</td><td>

Create a problem record from a case.

</td><td>

Madrid

</td></tr><tr><td>

CSM: Create Major Case and its Child Cases

</td><td>

Create a major case and the associated child cases for the customer accounts in the recipient list. **Note:** Requires Major Issue Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM: Agent Creating Request for Customer

</td><td>

As a customer service agent, create a request for a customer. **Note:** Requires Customer Service Request Integration.

</td><td>

Orlando

</td></tr><tr><td>

CSM: Register New Case Type

</td><td>

Register a case type and verify the record is created.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Create Project for an Account

</td><td>

Project Manager creates project for an account.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Identify Project Contact

</td><td>

Project manager identifies customers to a project.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Create Case from Project

</td><td>

Create a case from a project.

</td><td>

Orlando

</td></tr><tr><td>

CSM: Advanced Type Skill Determination Rule Test

</td><td>

Create an advanced type skill determination rule.

 **Note:** Requires Skill Determination.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Create Case from Project Task

</td><td>

Create a case from a project task.

</td><td>

Orlando

</td></tr><tr><td>

CSM: Create Task from Case

</td><td>

Create a case task from a case.

</td><td>

Orlando

</td></tr><tr><td>

CSM: Assign Case Task to Case Task Agent

</td><td>

The customer service agent creates and assigns a case task to a case task agent.

</td><td>

Rome

</td></tr><tr><td>

CSM: Case Task Agent views assigned Case Task

</td><td>

Verifies that the case task agent can view an assigned case task.

</td><td>

Rome

</td></tr><tr><td>

CSM: Case Task Agent Completes Assigned Task

</td><td>

The case task agent completes an assigned case task.

</td><td>

Rome

</td></tr><tr><td>

CSM-Create a case using 'Create a case \(POST\)' API

</td><td>

Create a case using 'Create a case \(POST\)' API.**Note:** Requires a user authentication record assigned to the **Basic authentication** field in step 1 of the ATF.

</td><td>

Rome

</td></tr><tr><td>

CSM-Query a case using 'Query a case \(GET\)' API

</td><td>

Query a case using 'Query a case \(GET\)' API.**Note:** Requires a user authentication record assigned to the **Basic authentication** field in step 1 of the ATF.

</td><td>

Rome

</td></tr><tr><td>

CSM: Address sharing across Accounts

</td><td>

Implement reusable addresses for accounts to support complex customer operations and business models.

</td><td>

Washington DC

</td></tr><tr><td>

CSM: Manage Consumer Profile Locations

</td><td>

Create and manage consumer locations, and map them to consumer profiles.

</td><td>

Washington DC

</td></tr><tr><td>

CSM: OCS Manager creating New OSP

</td><td>

Verify that a new Outsourced Service Provider \(OSP\) is created by the OCS internal manager. **Note:** Requires Outsourced Customer Service.

</td><td>

Rome

</td></tr><tr><td>

CSM: Case Creation by OCS Agent

</td><td>

Verify that an Outsourced Customer Service agent is able to create a case. **Note:** Requires Outsourced Customer Service.

</td><td>

Rome

</td></tr><tr><td>

CSM - Create Proactive Case by NOC Operator

</td><td>

Verify whether a proactive case is created.**Note:** Requires Proactive Customer Service Operations with Event Management.

</td><td>

New York

</td></tr><tr><td>

CSM - Employee creating case OBO customer

</td><td>

As an employee with the proxy contact role \(sn\_customerservice\_proxy\_contact\), create a case from the self-service portal on behalf of a customer. **Note:** Requires the CSM Extension for Proxy Contacts.

</td><td>

New York

</td></tr><tr><td>

CSM - Lookup Type Skill Determination Rule Test

</td><td>

Create a lookup type skill determination rule.**Note:** Requires Skill Determination.

</td><td>

New York

</td></tr><tr><td>

CSM - Manager creating request OBO customer from CSM portal

</td><td>

As a user with the case manager role, create a case on behalf of a customer from the Customer Service Portal.**Note:** Requires Customer Service Request Integration.

</td><td>

New York

</td></tr><tr><td>

CSM - Simple Type Skill Determination Rule Test

</td><td>

Create a simple type skill determination rule.**Note:** Requires Skill Determination.

</td><td>

New York

</td></tr><tr><td>

CSM - Project Manager create project task and assign to a customer

</td><td>

Project manager creates project task and assigns to a customer.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Agent Create Cases from a Project

</td><td>

As a customer service agent, create a case from a project.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Agent Create Cases from a Project task

</td><td>

As a customer service agent, create a case from a project task.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Agent Create Change Requests for a project

</td><td>

As a customer service agent, create a change request for a project.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Service Contracts covered under Sold Product

</td><td>

Create sold products and service contracts and associate service contracts to a sold product. Verify the association between the active contracts and the sold product.**Note:** Requires Customer Service Install Base Management.

</td><td>

Orlando

</td></tr><tr><td>

AWA - Create New Service Channel

</td><td>

Create a new service channel in the Advanced Work Assignment application.

 **Note:** Requires Advanced Work Assignment for CSM.

</td><td>

Orlando

</td></tr><tr><td>

CSM-ITOM - Create Child Cases for Proactive Major Case

</td><td>

Create a child case for a proactive major case using recipient list.**Note:** Requires Proactive Customer Service Operations with Event Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Create Outage from Case

</td><td>

Validate if newly created outage is linked to a case.

</td><td>

Paris

</td></tr><tr><td>

CSM: Create Sold Product on Household

</td><td>

Create a sold product on a household and its member. **Note:** Requires Customer Service Install Base Management and Customer Service Household with **Load demo data** enabled.

</td><td>

Quebec

</td></tr><tr><td>

CSM: View Health Status of Install Base Item from Account and Case pages

</td><td>

Validates the functionality of the **Refresh Install Base Health** button on the Account and Case record pages.

</td><td>

Quebec

</td></tr><tr><td>

CSM: Report a knowledge gap from a case in Agent Workspace

</td><td>

Verify that a knowledge gap related to a case was reported in Agent Workspace

</td><td>

Rome

</td></tr><tr><td>

CSM-Create a case using 'Create a case \(POST\)' API

</td><td>

Create a case using 'Create a case \(POST\)' API.**Note:** Requires a user authentication record assigned to the **Basic authentication** field in step 1 of the ATF.

</td><td>

Rome

</td></tr><tr><td>

CSM-Query a case using 'Query a case \(GET\)' API

</td><td>

Query a case using 'Query a case \(GET\)' API.**Note:** Requires a user authentication record assigned to the **Basic authentication** field in step 1 of the ATF.

</td><td>

Rome

</td></tr><tr><td>

CSM: OCS Manager creating New OSP

</td><td>

Verify that a new Outsourced Service Provider \(OSP\) is created by the OCS internal manager. **Note:** Requires Outsourced Customer Service.

</td><td>

Rome

</td></tr><tr><td>

CSM: Case Creation by OCS Agent

</td><td>

Verify that an Outsourced Customer Service agent is able to create a case. **Note:** Requires Outsourced Customer Service.

</td><td>

Rome

</td></tr><tr><td>

CSM: Manage Consumer Profile Locations

</td><td>

Create and manage consumer locations, and map them to consumer profiles.

</td><td>

Washington DC

</td></tr><tr><td>

CSM: Address sharing across Accounts

</td><td>

Implement reusable addresses for accounts to support complex customer operations and business models.

</td><td>

Washington DC

</td></tr><tr><td>

CSM: Create Case as Location Contributor from BLSP Portal

</td><td>

As a location contributor,create a case from the BLSP portal.

</td><td>

Yokohama

</td></tr><tr><td>

CSM: Create a Business Location And Onboard a Member To It

</td><td>

Verifies the creation of a business location and onboarding a member to it.

</td><td>

Yokohama

</td></tr><tr><td>

CSM: Escalate or de-escalate account workflow

</td><td>

Escalate or de-escalate account workflow

</td><td>

Zurich

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|CSM Workspace: Case creation Workflow|Tests the creation of a case record by a customer service manager in CSM/FSM Configurable Workspace.|Xanadu|
|CSM Workspace: Case follow up workflow|Tests the requesting of information from a customer by a customer service manager in CSM/FSM Configurable Workspace.|Xanadu|
|CSM Workspace: Report knowledge gap workflow|Tests the creation of a knowledge feedback task for a case record by a customer service manager in CSM/FSM Configurable Workspace.|Xanadu|
|CSM Workspace: Case resolution workflow|Tests the resolution of a case record by a customer service manager in CSM/FSM Configurable Workspace.|Xanadu|
|CSM Workspace: Create Incident from Case|Tests the creation of an incident record from a case record by a customer service agent in CSM/FSM Configurable Workspace.|Xanadu|
|CSM Workspace: Create Problem from Case|Tests the creation of a problem record from a case record by a customer service agent in CSM/FSM Configurable Workspace.|Xanadu|
|CSM Workspace: Create Normal Change from Case|Tests the creation of a change record from a case record by a customer service agent in CSM/FSM Configurable Workspace.|Xanadu|
|CSM Workspace: Case creation from All Cases list|Tests the creation of a case from the All cases list by a customer service manager \(sn\_customerservice\_manager\) in CSM/FSM Configurable Workspace.|Yokohama|
|CSM Workspace: Case Creation from My Cases list|Tests the creation of a case from the My Cases list by a customer service manager \(sn\_customerservice\_manager\) in CSM/FSM Configurable Workspace.|Yokohama|
|CSM Workspace: Case Creation from My Open cases list|Tests the creation of a case from the My Open list by a customer service manager \(sn\_customerservice\_manager\) in CSM/FSM Configurable Workspace.|Yokohama|
|CSM Workspace: Interaction creation from My Interaction list|Tests the creation of an interaction record from the My Interactions list by a customer service manager \(sn\_customerservice\_manager\) in CSM/FSM Configurable Workspace.|Yokohama|

|Test|Description|Release version|
|----|-----------|---------------|
|Create a Complaint Case|Tests that a user can create a case that is of type complaint in the sn\_complaint\_case table.|Paris|
|Escalate a Complaint Case|Tests that a user can escalate a case that is of type complaint in the sn\_complaint\_case table.|Paris|

|Test|Description|Release version|
|----|-----------|---------------|
|Create an Onboarding Case|Tests that a user can create a case that is of type onboarding in the sn\_onboarding\_case table.|Paris|
|Escalate an Onboarding Case|Tests that a user can escalate a case that is of type onboarding in the sn\_onboarding\_case table.|Paris|

|Test|Description|Release version|
|----|-----------|---------------|
|awa\_admin\_operations\_dashboard|Verify whether user with role awa\_admin is able to view the Advanced Work Assignment menu under Operations Dashboard and unassigned interactions and unassigned task work items modules.|Orlando|
|awa\_manager\_operations\_dashboard|Verify whether user with role awa\_manager is able to view the Advanced Work Assignment menu under Operations Dashboard and unassigned interactions and unassigned task work items modules.|Orlando|

<table id="table_pq2_bkb_4jb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

CSM - Create Product Case as Customer from CSM Portal

</td><td>

Create a product case as a customer from the Customer Service Portal.**Note:** Requires Customer Service Portal. Also requires that the test be run as admin.

</td><td>

Madrid

</td></tr><tr><td>

CSM - Create Product Case as Partner from CSM Portal

</td><td>

Create a product case as a partner from the Customer Service Portal.**Note:** Requires Customer Service Portal. Also requires that the test be run as admin.

</td><td>

Madrid

</td></tr><tr><td>

CSM - Search on Homepage

</td><td>

Search for information from the Customer Service Portal. The search includes cases, Knowledge articles, and Community threads.

</td><td>

New York

</td></tr><tr><td>

CSM - Update Support Profile

</td><td>

Update a contact's profile from the Customer Service Portal.

</td><td>

New York

</td></tr><tr><td>

CSM - Provide requested info on case

</td><td>

From the Customer Service Portal, the contact can provide information for a case that was requested by the agent.

</td><td>

New York

</td></tr><tr><td>

CSM - Accept Proposed Solution On Case

</td><td>

Accept a proposed solution for a case from the Customer Service Portal.

</td><td>

New York

</td></tr><tr><td>

CSM - Provide Feedback on Survey

</td><td>

Provide feedback on a survey after a case is closed from the Customer Service Portal.

</td><td>

New York

</td></tr><tr><td>

CSM - View All Desktop Notifications

</td><td>

View all Customer Service Management specific desktop notifications.

</td><td>

Orlando

</td></tr><tr><td>

CSM - View Publications on CSM Portal

</td><td>

View publications on the Customer Service Management portal.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Create Contact on CSM Portal

</td><td>

Create contacts on the Customer Service Management portal.

</td><td>

Orlando

</td></tr><tr><td>

CSM: Validate Outage widgets in CSM Portal

</td><td>

Validates various types of outages and the corresponding widgets shown on the Customer Service Portal home page and the Install Base page.

</td><td>

Quebec

</td></tr><tr><td>

CSM - Create case from Portal as Consumer Contributor

</td><td>

Creates a customer case from the portal by a user with the consumer contributor user role \(sn\_customerservice.consumer\_contributor\).**Note:** Requires Business Location, Customer Service Household, and CSM Contributor User.

</td><td>

Rome

</td></tr><tr><td>

CSM - Create case from Portal as Account Contributor

</td><td>

Creates a customer case from the portal by a user with the account contributor user role \(sn\_customerservice.account\_contributor\).**Note:** Requires Business Location, Customer Service Household, and CSM Contributor User.

</td><td>

Rome

</td></tr><tr><td>

CSM - Add Related parties on Case and perform action on case as Related party

</td><td>

Verify the ability to add related parties to the case and perform actions on the case as related parties through the CSM Portal.

</td><td>

Rome

</td></tr></tbody>
</table><table id="table_lss_wlb_4jb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

CSP - Create Product Case as Consumer from CSP Portal

</td><td>

Create a product case as a consumer from the Consumer Service Portal. **Note:** Requires the Consumer Service Portal. Also requires that the test be run as admin.

</td><td>

Madrid

</td></tr><tr><td>

CSP - Search on Homepage

</td><td>

Search for information from the Consumer Service Portal. The search includes cases, knowledge articles, and Community threads.

</td><td>

New York

</td></tr><tr><td>

CSP - Update Support Profile

</td><td>

Update a consumer's profile from the Consumer Service Portal.

</td><td>

New York

</td></tr><tr><td>

CSP - Register Your Product

</td><td>

Register a product from the Consumer Service Portal.

</td><td>

New York

</td></tr><tr><td>

CSP - Provide requested info on case

</td><td>

From the Consumer Service Portal, the consumer can provide information for a case that was requested by the agent.

</td><td>

New York

</td></tr><tr><td>

CSP - Accept Proposed Solution On Case

</td><td>

Accept a proposed solution for a case from the Consumer Service Portal.

</td><td>

New York

</td></tr><tr><td>

CSP - Provide Feedback on Survey

</td><td>

Provide feedback on a survey after a case is closed from the Consumer Service Portal.

</td><td>

New York

</td></tr><tr><td>

CSP - View Publications on CSP Portal

</td><td>

View publications on Customer Service portal.

</td><td>

Orlando

</td></tr><tr><td>

CSP - Create Product Case as an internal unified consumer from CSP Portal

</td><td>

This test verifies the functionality of creating a product case as an internal unified consumer from the CSP portal in conjunction with the Customer Service and Consumer Service Portal plugins, using the Customer Service Management \(CSM\) demo data plugin.

</td><td>

Yokohama

</td></tr><tr><td>

CSP - Create Product Case as an external unified consumer from CSP Portal

</td><td>

This test verifies the functionality of creating a product case as an external unified consumer from the CSP portal in conjunction with the Customer Service and Consumer Service Portal plugins, using the Customer Service Management \(CSM\) demo data plugin.

</td><td>

Yokohama

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|Validate Next Best Action List- Guided Decisions|Validates the list of next best actions recommended based on the configured rules.|San Diego|
|Validate Next Best Action Ranking- Guided Decisions|Validates the list of next best actions recommended based on the configured rules.|San Diego|

|Test|Description|Release version|
|----|-----------|---------------|
|TC - Create Recipient List|Create a recipient list with the required parameters. Verify the new recipient list in the related list "Recipients".|Orlando|
|TC - Create Publication|Create a publication. The publication is published based on the publication date and verify if an user in the recipient list gets the publication.|Orlando|

<table id="table_myh_4hq_wtb"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

CSM Walkup: Check-in as a walkup user, look at the queue, and submit a survey

</td><td>

As a walk-up user, perform check-in, look at the queue, and submit feedback through a survey.**Note:** This test works when the Seattle location, available with demo data, is available.

</td><td>

Rome

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|CSM PPM: Case creation from project workflow|As a customer service agent, create a case from a CSM project record in CSM Configurable Workspace.|Yokohama|
|CSM PPM: Case creation from project task workflow|As a customer service agent, create a case from a CSM project task record in CSM Configurable Workspace.|Yokohama|


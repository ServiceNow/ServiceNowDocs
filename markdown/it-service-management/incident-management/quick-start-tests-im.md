---
title: Quick start tests for Incident Management
description: Validate that Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Incident Management, Incident Management, IT Service Management]
---

# Quick start tests for Incident Management

Validate that Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

Incident Management quick start tests require activating the Incident Management - ATF Tests plugin \(com.snc.incident.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|INCIDENT MGMT: Incident Resolution SLA|Test to verify the Incident Resolution SLA baseline functionality.|Madrid|
|INCIDENT MGMT: Incident Response SLA|Test to verify the Incident Response SLA baseline functionality.|Madrid|
|INCIDENT MGMT: Copy Incident|Test to verify whether the fields from the original Incident are copied correctly to the new Incident.|Madrid|
|INCIDENT MGMT: Copy Incident from a Closed Incident|Test to verify that the **Copy Incident** UI action is visible for closed Incidents.|Madrid|
|INCIDENT MGMT: Create Standard Change from Incident|Test to verify the creation of a Standard Change from an Incident.|Madrid|
|INCIDENT MGMT: Create of Emergency Change from an Incident|Test to verify the creation of an Emergency Change from an Incident.|Madrid|
|INCIDENT MGMT: Create Normal Change from an Incident|Test to verify the creation of a Normal Change from an Incident.|Madrid|
|INCIDENT MGMT: Create Problem from an Incident|Test to verify the creation of a Problem from an Incident.|Madrid|
|INCIDENT MGMT: Create Knowledge from an Incident|Test to verify the creation of a Knowledge from an Incident.|Madrid|
|INCIDENT MGMT: Incident State flow|Test to verify the state flow of an incident.|Madrid|
|INCIDENT MGMT: Reopening an Incident|Test to verify the reopen incident functionality.|Madrid|
|INCIDENT MGMT: Incident Assignment|Test to verify the incident assignment functionality.|Madrid|
|INCIDENT MGMT: Create child Incident using UI action and verify its fields|Test to verify the creation of a child Incident from an Incident through the **Create Child Incident** UI action. The test also verifies that the fields of the child Incident get copied correctly from the parent incident to the child incident.|Madrid|
|INCIDENT MGMT: Incident creation — Self Service|Test to verify the creation of an Incident using the **Create Incident** catalog item.|Madrid|
|INCIDENT MGMT: Parent and Child Incident state sync up|Test to verify that the state of a child Incident synchronizes with the parent Incident when the child Incident is created.|Madrid|
|INCIDENT MGMT: Parent and child Incident state sync up after reopening an Incident|Test to verify that the state of a child Incident synchronizes with the parent Incident when the parent Incident is reopened.|Madrid|
|INCIDENT MGMT: Verify creation of knowledge article from an Incident|Test to verify the creation of a knowledge article from an Incident using the **Create Knowledge** UI action on the Incident form. The UI action is visible when you activate the KCS Integration for Incident Management plugin \(com.snc.incident.knowledge\).|Orlando|

**Parent Topic:**[Configuring Incident Management](../../../product/incident-management/concept/incident-configuration.md)

**Related topics**  


[Quick start tests](https://www.servicenow.com/docs/access?context=quick-start-tests&version=australia&pubname=australia-application-development&ft:locale=en-US)


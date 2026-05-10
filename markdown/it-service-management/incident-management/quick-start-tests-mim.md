---
title: Quick start tests for Major Incident Management
description: Validate that Major Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing major incidents, Incident Management, IT Service Management]
---

# Quick start tests for Major Incident Management

Validate that Major Incident Management still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize these quick start tests to pass when using your instance-specific data.

## Major Incident Major Incident Management

Major Incident Management quick start tests require activating the Incident Management - Major Incident Management plugin \(com.snc.incident.mim\).

|Test|Description|Release version|
|----|-----------|---------------|
|MIM: Create a Major Incident|Test to verify the creation of major incident from the application navigation module.|Orlando|
|MIM: Create a Major Incident Candidate|Test to verify the **Create a Major Incident Candidate** module from navigation menu.|Orlando|
|MIM: Create a Major Incident from a Major Incident Candidate|Test to verify the creation of a major incident from a major incident candidate.|Orlando|
|MIM: Major Incident Candidate creation when it matches Major Incident Management trigger rule|Test to verify the creation of a major incident candidate when conditions to create a major incident match the major incident management trigger rule.|Orlando|
|MIM: Propose a major Incident \(Assignment group empty\)|Test to verify auto assignment of major incident candidate when an incident is proposed as a major incident and the **Assignment group** and the **Assigned to** fields are empty.|Orlando|
|MIM: Propose a major Incident \(Assignment group is not empty\)|Test to verify the auto assignment of a major incident when an incident is proposed as major incident and the **Assignment Group** and the **Assigned to** fields are not empty.|Orlando|
|MIM: Promote a candidate to major Incident \(Assignment group is empty\)|Test to verify auto assignment of major incident when a candidate is promoted to a major incident and the **Assignment Group** is empty.|Orlando|
|MIM: Promote a candidate to major Incident \(Assignment group is not empty\)|Test to verify auto assignment of major incident when a candidate is promoted to a major incident and the **Assignment group** is not empty.|Orlando|
|MIM: Reject a Major Incident Candidate|Test to verify the rejection of a major incident candidate.|Orlando|
|MIM: Demote a Major Incident|Test to verify whether a major incident gets demoted to an incident.|Orlando|
|MIM: Major Incident closure|Test to validate the major incident closure functionality.|Orlando|
|MIM: State sync up with ICP and ICT|Test is to verify the state sync up with Incident Communication Plan and Incident Communication Task.|Orlando|
|MIM: ICP attached to an Incident based on conditions and its state sync up with ICT|Test is to verify Incident Communication Plan attached to an Incident based on defined conditions.|Orlando|
|MIM: Resolving MI and PIR|Test is to verify resolving a Major Incident and Post Incident Report.|Orlando|
|MIM: Major Incident workbench layout verification|Test is to verify Major Incident workbench layout verification.|Orlando|
|MIM: Verify communication task from MI workbench|Test is to verify communication task from MI workbench.|Orlando|

To learn more about Major Incident Management, see [Major Incident Management](../../../product/incident-management/concept/major-incident-management.md).

**Parent Topic:**[Managing major incidents](../../../product/incident-management/concept/major-incident-management.md)

**Related topics**  


[Quick start tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/quick-start-tests.md)


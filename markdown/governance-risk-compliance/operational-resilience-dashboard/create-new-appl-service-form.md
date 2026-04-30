---
title: Create New Service Instance form
description: Use the Create New Service Instance form in Operational Resilience Workspace to set up an application service and configure its related lists.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Add an application service to Operational Resilience reporting, Gathering data aligned with the CSDM setup, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create New Service Instance form

Use the Create New Service Instance form in Operational Resilience Workspace to set up an application service and configure its related lists.

## Create New Service Instance form

For a description of the field values, see the following table.

<table id="table_krg_hgd_qtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Details tab

</td></tr><tr><td>

Name

</td><td>

Name of the application service.

</td></tr><tr><td>

Approval group

</td><td>

Approval group that is responsible for the approval of the application service, for example, Analytics setting managers or Application Security group.

</td></tr><tr><td>

Model ID

</td><td>

Model ID for the application service, for example, AT&amp;T SoundPoint IP 560.

</td></tr><tr><td>

Support group

</td><td>

Support group for the application service, for example, App Engine Admins.

</td></tr><tr><td>

Owned by

</td><td>

Owner of the application service.

</td></tr><tr><td>

Change group

</td><td>

Change group that is responsible for updating the application service, for example, Application Development.

</td></tr><tr><td>

Business criticality

</td><td>

Criticality of the application service. The available options are as follows:-   1—most critical
-   2—somewhat critical
-   3—less critical
-   4—not critical

</td></tr><tr><td>

Managed by

</td><td>

User that manages the application service.

</td></tr><tr><td>

Version

</td><td>

Version of the application service.

</td></tr><tr><td>

SLA

</td><td>

Service level agreements \(SLAs\) associated with the application service, for example, Finance 99.99.

</td></tr><tr><td>

Used for

</td><td>

Usage category that the application service is used for. For example, Staging. The available options for the usage category are as follows:-   Production
-   Staging
-   QA
-   Test
-   Development
-   Demonstration
-   Training
-   Disaster recovery

</td></tr><tr><td>

Location

</td><td>

Location and the physical address for the application service.

</td></tr><tr><td>

Operational status

</td><td>

Operational status of the application service. The available options are as follows:-   Operational
-   Non-Operational
-   Repair in Progress
-   DR Standby
-   Ready
-   Retired
-   Pipeline
-   Catalog

</td></tr><tr><td>

Vendor

</td><td>

Vendor that is responsible for operating the application service, for example, Acer or Adobe Systems.

</td></tr><tr><td>

Service classification

</td><td>

Classification of the service. The available options are as follows:-   Application Service
-   Business Service
-   Technology Management Service

</td></tr><tr><td>

Comments

</td><td>

Comments section for the application service. Typically, the Operational Resilience administrators add comments about the application service.

</td></tr></tbody>
</table><table id="table_vjd_mmd_qtb"><thead><tr><th>

Related tab

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

General

</td></tr><tr><td>

Overview tab

</td><td>

Displays the following red flags data:1.  Total red flags
2.  Red flags by type
    -   Issues
    -   Failed controls
    -   Risks
    -   Outages
    -   Incidents
    -   Change requests
    -   Operational vulnerabilities
    -   Vulnerabilities
    -   Third party risk assessments
3.  Assets impacted by red flags

</td></tr><tr><td>

Details tab

</td><td>

Details of the selected application service record.

</td></tr><tr><td class="sub-head" colspan="2">

Services and dependencies

</td></tr><tr><td>

Child services

</td><td>

Child services that are associated with the application service.

 The tab displays the following sample information about the child services:

-   Dependency
-   Pillar
-   Impacted objects
-   Red flags count

</td></tr><tr><td>

Business processes

</td><td>

Processes that are associated with the application service.

 The tab displays the following sample information about the business processes:

-   Dependency
-   Pillar
-   Impacted objects
-   Red flags count

</td></tr><tr><td>

Dependencies

</td><td>

Dependencies that are associated with the application service. The tab displays the following sample information about the dependencies:

-   Dependency
-   Pillar
-   Impacted objects
-   Red flags count

</td></tr><tr><td class="sub-head" colspan="2">

Ongoing events

</td></tr><tr><td>

Incidents

</td><td>

Incidents that are associated with the application service.

 The tab displays the following sample information about the incidents:

-   Incident
-   Short description
-   Owner
-   Opened
-   Caller
-   Priority
-   State
-   Category
-   Assignment group
-   Assigned to
-   Updated
-   Updated by
-   Dependency
-   Pillar

</td></tr><tr><td>

Outages

</td><td>

Outages that are associated with the current application service. You can create an outage for the service.

 The tab displays the following sample information about the outages:

-   Number
-   Outage
-   Type
-   Begin
-   End
-   Dependency
-   Pillar

</td></tr><tr><td colspan="2">

Red flags

</td></tr><tr><td>

Issues

</td><td>

Issues that are associated with the application service.

 The tab displays the following sample information about the issues:

-   Issue
-   Priority
-   Status
-   Planned end date
-   Dependency
-   Pillar

</td></tr><tr><td>

High risks

</td><td>

High risks that are associated with the application service.

 The tab displays the following sample information about the high risks:

-   Risk
-   Risk assessment
-   Risk statement
-   Risk response
-   Inherent rating
-   Computed inherent rating
-   Residual rating
-   Computed residual rating
-   Dependency
-   Pillar

</td></tr><tr><td>

Failed controls

</td><td>

Failed controls that are associated with the application service.

 The tab displays the following sample information about the failed controls:

-   Control
-   Control objective
-   Status
-   Dependency
-   Pillar

</td></tr><tr><td>

Change requests

</td><td>

Change requests that are associated with a business service.

 The tab displays the following sample information about the change requests:

-   Change request
-   Short description
-   Type
-   State
-   Planned start date
-   Planned end date
-   Assigned to
-   Dependency
-   Pillar

</td></tr><tr><td>

Tasks

</td><td>

Tasks that are associated with the application service.

 The tab displays the following sample information about the tasks:

-   Task
-   Short description
-   State
-   Task type
-   Priority
-   Assigned to
-   Dependency
-   Pillar

</td></tr><tr><td>

Vulnerabilities

</td><td>

Vulnerabilities associated with the application service. The tab displays the following sample information about the vulnerabilities:

-   Vulnerability
-   Dependency
-   Pillar

</td></tr><tr><td>

Operational vulnerabilities

</td><td>

Operational vulnerabilities associated with the application service. The tab displays the following sample information about the operational vulnerabilities:

-   Number
-   Case
-   Related area
-   Related area table
-   Title
-   Related area type
-   Domain

</td></tr><tr><td>

Third party risk assessments

</td><td>

Third party risk assessments associated with the application service. The tab displays the following sample information about the Third party risk assessments:

-   Third party risk assessment
-   Dependency
-   Pillar

</td></tr><tr><td class="sub-head" colspan="2">

Program activities

</td></tr><tr><td>

Business continuity plans

</td><td>

List of the Business continuity plans that are associated with the application service. The tab displays the following sample information about the plans:

-   Plan
-   Plan asset
-   Activated plan
-   Event
-   Event asset
-   Dependency
-   Pillar
-   Status
-   RTO
-   RPO
-   BIA date
-   RTO gap

</td></tr><tr><td>

Importance and impact assessment

</td><td>

Importance and impact assessment that is done for the application service.

 The tab displays the following sample information about the assessment:

-   Impact tolerance \(Duration\)
-   Impact tolerance assessment
-   Justification for overriding impact tolerance \(Duration\)
-   Justification for overriding impact tolerance \(Customer impact\)
-   Justification for overriding impact tolerance \(Financial impact\)
-   Justification for overriding impact tolerance \(Transaction Volume\)
-   Overridden importance
-   Impact tolerance \(Customer impact\)
-   Impact tolerance \(Financial impact\)
-   Impact tolerance \(Transaction Volume\)
-   Importance

</td></tr><tr><td>

Scenario analysis

</td><td>

Scenario analysis that is associated with the application service.

 The tab displays the following sample information about the scenario analysis:

-   Breach status
-   Disruption duration
-   Impact tolerance
-   Deviation \(%\)
-   Importance
-   Scenario analysis
-   Service
-   Created by
-   Created
-   Domain

</td></tr></tbody>
</table>
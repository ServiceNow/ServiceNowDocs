---
title: Create New Service form
description: Use the Create New Service form in Operational Resilience Workspace to set up a business service and configure its related lists.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Add a service to Operational Resilience reporting, Gathering data aligned with the CSDM setup, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Create New Service form

Use the Create New Service form in Operational Resilience Workspace to set up a business service and configure its related lists.

## Create New Service form

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

Name of the service.

</td></tr><tr><td>

Approval group

</td><td>

Approval group that is responsible for the approval of the service. For example, Application Development or Application Security group.

</td></tr><tr><td>

Model ID

</td><td>

Model ID for the service.

</td></tr><tr><td>

Support group

</td><td>

Support group for the service.

</td></tr><tr><td>

Owned by

</td><td>

Owner of the service. This field is auto-filled.

</td></tr><tr><td>

Change group

</td><td>

Change group that is responsible for updating the service.

</td></tr><tr><td>

Business criticality

</td><td>

Criticality of the service. The available options are as follows:-   1—most critical
-   2—somewhat critical
-   3—less critical
-   4—not critical

</td></tr><tr><td>

Managed by

</td><td>

User that manages the service.

</td></tr><tr><td>

Version

</td><td>

Version of the service.

</td></tr><tr><td>

SLA

</td><td>

Service level agreements \(SLAs\) for the service.

</td></tr><tr><td>

Used for

</td><td>

Usage category that the service is used for. For example, Staging. The available options are as follows:-   Production
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

Physical location of the service.

</td></tr><tr><td>

Operational status

</td><td>

Operational status of the service. The available options are as follows:-   Operational
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

Vendor that is responsible for operating the service.

</td></tr><tr><td>

Service classification

</td><td>

Classification of the service. The available options are as follows:-   Business Service
-   Technical Service
-   Application Service

</td></tr><tr><td>

Comments

</td><td>

Comments section for the service. Typically, the Operational Resilience administrators add the comments about the service.

</td></tr></tbody>
</table>## Related tabs

In the Create New Service form, you can add a parent service, child service, and process for the business service. You can also configure the related tabs, such as the tabs for change requests, incidents, and tasks for the service. You can then view the service attributes and resilience metrics on the dashboard. The following table describes the related tabs that are associated with a service.

<table id="table_vjd_mmd_qtb"><thead><tr><th>

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

Details of the selected service record. For more information on the fields and their description, see the "Create New Service form" table on this page.

</td></tr><tr><td class="sub-head" colspan="2">

Services and dependencies

</td></tr><tr><td>

Child services

</td><td>

Child services that are associated with the service.

 The tab displays the following sample information about the child services:

-   Dependency
-   Pillar
-   Impacted objects
-   Red flags count

</td></tr><tr><td>

Business processes

</td><td>

Processes that are associated with the service.

 The tab displays the following sample information about the business processes:

-   Dependency
-   Pillar
-   Impacted objects
-   Red flags count

</td></tr><tr><td>

Dependencies

</td><td>

Dependencies that are associated with the service. The tab displays the following sample information about the dependencies:

-   Dependency
-   Pillar
-   Impacted objects
-   Red flags count

</td></tr><tr><td class="sub-head" colspan="2">

Ongoing events

</td></tr><tr><td>

Incidents

</td><td>

Incidents that are associated with the service.

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

Outages that are associated with the current service. You can create an outage for the service.

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

Issues that are associated with the service.

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

High risks that are associated with the service.

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

Failed controls that are associated with the service.

 The tab displays the following sample information about the failed controls:

-   Control
-   Control objective
-   Status
-   Dependency
-   Pillar

</td></tr><tr><td>

Change requests

</td><td>

Change requests that are associated with the service.

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

Tasks that are associated with the service.

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

Vulnerabilities associated with the service. The tab displays the following sample information about the vulnerabilities:

-   Vulnerability
-   Dependency
-   Pillar

</td></tr><tr><td>

Operational vulnerabilities

</td><td>

Operational vulnerabilities associated with the service. The tab displays the following sample information about the operational vulnerabilities:

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

Third party risk assessments associated with the service. The tab displays the following sample information about the Third party risk assessments:

-   Third party risk assessment
-   Dependency
-   Pillar

</td></tr><tr><td class="sub-head" colspan="2">

Program activities

</td></tr><tr><td>

Business continuity plans

</td><td>

List of the Business continuity plans that are associated with the service. The tab displays the following sample information about the plans:

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

Importance and impact assessment that is done for the service.

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

Scenario analysis that is associated with the service.

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
</table>To view Related lists and Red flags data in the Operational Resilience Workspace, you must have appropriate user roles. See the "Roles to view elated lists and Red flags data" table for more information.

<table id="table_z32_2f4_bgc"><thead><tr><th>

Related lists and Red flags data

</th><th>

Roles required

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Business continuity information related list

</td><td>

BCM manager role

</td><td>

 

</td></tr><tr><td>

Failed controls red flags

</td><td>

BCM manager role

</td><td>

 

</td></tr><tr><td>

Risks and Third party risk assessments red flags

</td><td>

IRM manager role

</td><td>

-   **TPRM is not installed**

If TPRM is not installed, Operational Resilience users cannot access risk red flags without the IRM roles.

-   **TPRM is installed**

However, if TPRM is installed, Operational Resilience users can access both risk red flags and Third-party Risk Management red flags because they are assigned the TPRM viewer role. The TPRM viewer role includes risk viewer capabilities, thus eliminating the need for IRM roles.


</td></tr><tr><td>

Rest of the related lists and red flags in the dashboard

</td><td>

Accessible with Operational Resilience roles

</td><td>

 

</td></tr></tbody>
</table>
---
title: Available quick start tests by application or feature
description: Validate that your instance still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize the ServiceNow -provided quick start tests to pass when using your instance-specific data.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 108
breadcrumb: [Quick start tests, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Available quick start tests by application or feature

Validate that your instance still works after you make any configuration change such as apply an upgrade or develop an application. Copy and customize the ServiceNow -provided quick start tests to pass when using your instance-specific data.

**Danger**

By default, the system property that is used to run automated tests is disabled to prevent you from accidentally running these tests on a production system. To avoid data corruption or an outage, run tests only on development, test, and other non-production instances. See [Enable or disable executing Automated Test Framework tests](../task/atf-enable-tests.md).

## Agile Development 2.0

Agile Development 2.0 quick start tests require activating the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) and the Agile Development 2.0 - ATF Tests plugin \(com.snc.sdlc.agile.2.0.atf \).

<table id="atf-tests-Agile2.0"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

Verify that global rank is populated when a story is created

</td><td>

Verify the global rank of a story after creation.

</td><td>

Madrid

</td></tr><tr><td>

Verify that closing a sprint with active stories is prevented

</td><td>

Verify that a sprint with active stories cannot be closed.

</td><td>

Madrid

</td></tr><tr><td>

Verify that sprints cannot overlap in the same group

</td><td>

Verify that sprints in the same group do not overlap.

</td><td>

Madrid

</td></tr><tr><td>

Verify that sprint points are updated

</td><td>

Verify that changes to stories produce accurate sprint point totals.

</td><td>

Madrid

</td></tr><tr><td>

Verify that only one sprint in a group can have the current state

</td><td>

Verify sprint statuses.

</td><td>

Madrid

</td></tr><tr><td>

Verify sprint end date is after the sprint start date

</td><td>

Verify sprint start and end dates.

</td><td>

Madrid

</td></tr><tr><td>

Verify that any update on story rolls up to Epic

</td><td>

Verify that adding, estimating, removing, deleting, updating, or cancelling a story updates the epic-level roll-ups correctly.

</td><td>

Orlando

</td></tr><tr><td>

Verify changes to the scope of a current sprint do not alter the value of the Total Committed Points

</td><td>

Verify that the value of Total Committed Points does not change with change in the scope of a sprint after its state is changed to Current.

</td><td>

Orlando

</td></tr><tr><td>

Verify active flag is set false when Agile Story state is changed to Completed/Cancelled

</td><td>

Verify that active flag of an Agile story is set to the following: -   False, if the state is changed to Completed or Cancelled
-   True, for all other states

</td><td>

Orlando

</td></tr><tr><td>

Verify that updating the team/group capacity overrides the capacity on all the future sprints

</td><td>

Verify that any update to the **Group capacity** field of the assignment group results in the following changes to the **Group capacity** field of the various sprints associated with this assignment group:

-   For the sprints that are in the Draft and Planning state:
    -   The group capacity is updated to the new value.
    -   The **Group capacity** field is editable.
-   For the sprints in the Current, Complete, or Cancelled state:
    -   The group capacity remains the old value.
    -   The **Group capacity** field is read-only.

 For the sprints in the Draft or Planning state, you can individually edit the group capacity of the sprint anytime later. This would not change the group capacity of the assignment group associated with this sprint.

</td><td>

Paris

</td></tr><tr><td>

Verify create and edit functionality of an epic backlog on the scrum program board

</td><td>

-   Verify that you can create an epic backlog for scrum programs from the Backlog tab of Agile Board.
-   Verify that you can update an existing epic backlog for scrum programs from the Backlog tab of Agile Board.
-   The epics listed in the backlog must belong to the selected epic backlog.

</td><td>

Quebec

</td></tr><tr><td>

Verify a Demand is converted to a scrum story

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to an Agile 2.0 story using the **Create Story** related link on the Demand form. For more information on how to create an Agile 2.0 story from a demand, see [Create an artifact from a demand](https://www.servicenow.com/docs/access?context=t_CrtArtftDmdMnu&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

</td><td>

Quebec

</td></tr><tr><td>

Verify a Demand is converted to a scrum epic

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to an Agile 2.0 epic using the **Create Epic** related link on the Demand form.For more information on how to create an Agile 2.0 epic from a demand, see [Create an artifact from a demand](https://www.servicenow.com/docs/access?context=t_CrtArtftDmdMnu&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

</td><td>

Quebec

</td></tr></tbody>
</table>To learn more about Agile Development 2.0, see [Agile Development 2.0](https://www.servicenow.com/docs/access?context=agile-landing-page&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Enterprise Architecture \(formerly Application Portfolio Management\)

Enterprise Architecture quick start tests require enabling the Enterprise Architecture – ATF Tests plugin \(com.snc.apm.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|Enterprise Architecture: Create Business Application|Verify the creation of an application category and then the creation of a business application with users having apm\_user role.|Madrid|
|Enterprise Architecture: Create Business Capability|Verify the creation of a parent and child business capability and verify its field values.|Madrid|
|Enterprise Architecture: Test relating Business Service, Business Application, and Software Models|Verify the creation of a business application, business service, using the existing software model, and a relationship between them.|Orlando|
|Enterprise Architecture: Test for Indicator Score and Application Score generation|Verify the creation of indicator, scoring profile, and generation of indicator scores and application scores.|Paris|
|Enterprise Architecture: Business Application with Information Object and Data Domain|Verify the creation of business application, information object, and addition of the CRUD operations in relation attributes.|Quebec|

To learn more about Enterprise Architecture \(formerly Application Portfolio Management\), see [Application Portfolio Management](https://www.servicenow.com/docs/access?context=application-portfolio-management&version=xanadu&pubname=xanadu-application-portfolio-management&ft:locale=en-US).

## Assessments and Surveys

Assessments and Surveys quick start tests require activating the Automated Test Framework for Survey plugin \(com.glide.automated\_testing\_impl. Survey\).

|Name|Description|Release version|
|----|-----------|---------------|
|Survey: Basic Platform Based Test|Create a survey using Platform UI actions.|Madrid|
|Survey: Platform test for Dynamic Validation|Validate a survey dynamically.|Madrid|
|Survey: Clone Action|Clone a survey and validate the records of the original survey and the cloned survey.|New York|
|Survey: Question Bank Flow|Verify the addition of a question bank to a survey.|New York|
|Survey: Survey Creator Work Flow|Survey creator can create a survey and assign to the user who can take the survey and submit it.|New York|
|Assessment: Assign assessment to assessor|Assign an assessment to an assessor and verify that the instance is created for the assessor.|Orlando|
|Assessment: Create assessment as survey creator|Create an assignment as a survey creator.|Orlando|
|Assessment: Scale and Template support|Create, publish, and assign the assessment. Then take the assessment.|Rome|
|Assessment: Basic test flow|Verify the basic flow of an assessment.|Orlando|

To learn more about Assessments and Surveys, see [Service administration](https://www.servicenow.com/docs/access?context=c_ServiceAdministration&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Change Management

Change Management quick start tests require activating the Change Management - ATF Tests plugin \(com.snc.change\_management.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|Emergency Type Change Request workflow|Process an emergency change request from new to closed.|Madrid|
|On Hold for Emergency type Change Request|Validate the approval state of an on-hold emergency change request.|Madrid|
|Copy Change For Emergency type Change Request|Validate the state of a copied emergency change request.|Madrid|
|Reject By Approver for Emergency type|Validate the state of a rejected emergency change request.|Madrid|
|Revert to new for emergency type|Validate the state of an emergency change request after using the Revert to new UI action.|Madrid|
|Convert Emergency to Normal type|Validate the conversion of an emergency change request to a normal change request.|Madrid|
|Cancel Change Request For Emergency Type|Validate the state of a canceled emergency change request.|Madrid|

|Test|Description|Release version|
|----|-----------|---------------|
|Normal Type Change Request Workflow|Process a normal change request from new to closed.|Madrid|
|Convert Normal to Emergency type|Validate the conversion of a normal change request to an emergency change request.|Madrid|
|Copy change on Normal Change Request|Validate the state of a copied normal change request.|Madrid|
|On hold for Normal type Change Request|Validate the approval state of an on-hold normal change request.|Madrid|
|State validation when Reject Normal type Change request by Approver.|Validate the state of a rejected normal change request.|Madrid|
|Revert to New Functionality for Normal Type Change Request|Validate the state of a normal change request after using the Revert to new UI action.|Madrid|
|Cancel Change Request For Normal type|Validate the state of a canceled normal change request.|Madrid|

|Test|Description|Release version|
|----|-----------|---------------|
|Standard Change Proposal|Determine whether a user can successfully perform standard change proposal creation, approval, and template publishing processes.|Madrid|

|Test|Description|Release version|
|----|-----------|---------------|
|Standard Change Request Workflow|Process a standard change request from new to closed.|Madrid|
|Convert Standard to Emergency Change Request|Validate the conversion of a standard change request to an emergency change request.|Madrid|
|Convert Standard to Normal Change Request|Validate the conversion of a standard change request to a normal change request.|Madrid|

|Test|Description|Release version|
|----|-----------|---------------|
|Unauthorized change request Workflow|Process a unauthorized change request from new to closed.|Orlando|
|Create Outage of type planned outage from change request|Validate the creation of an outage of type planned outage from a change request.|Orlando|
|Create Outage of type outage from change request|Validate the creation of an outage of type outage from a change request.|Orlando|

|Test|Description|Release version|
|----|-----------|---------------|
|Moderate Risk with UI Action Property|Process a moderate risk with UI action property.|Orlando|
|Low Risk with UI Action Property|Process a low risk with UI action property.|Orlando|
|Leave Alone Risk with UI Action Property|Process a leave alone risk with UI action property.|Orlando|
|High Risk with UI Action Property|Process a high risk with UI action property.|Orlando|
|High Risk with Business Rule Property|Process a high risk with Business rule property.|Orlando|
|Moderate Risk with Business Rule property|Process a moderate risk with Business rule property.|Orlando|

|Test|Description|Release version|
|----|-----------|---------------|
|Change against Blackout window|Process a change request against a blackout window.|Orlando|
|Check conflicts for CI Already Scheduled|Validate the conflicts for CI already scheduled.|Orlando|
|Change against Conflict Sources|Validate the change request against conflict sources.|Orlando|

|Test|Description|Release version|
|----|-----------|---------------|
|Change Schedules Definitions on New|Process the creation of change schedules definitions from New button on Change Schedules landing page.|Orlando|
|Share Panel On Change Schedules Definition|Validate the share panel on change schedules definition.|Orlando|
|Share Change Schedule Definition|Validate the sharing of change schedules definitions.|Orlando|
|Create Standard Change via Service Portal|Create Standard Change from Service Portal|Xanadu|

To learn more about Change Management, see [Change Management](https://www.servicenow.com/docs/access?context=c_ITILChangeManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Cloud Provisioning and Governance

Cloud Provisioning and Governance quick start tests require activating the following Cloud Provisioning and Governance plugins:

-   Cloud Provisioning and Governance \(com.snc.cloud.mgmt\)
-   Domain Support- Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\)
-   Service Catalog- Domain Separation plugin \(glideapp.servicecatalog.domain\_separation\)

|Test|Description|Release version|
|----|-----------|---------------|
|CMP: Add Azure Credentials|Add Azure credentials by inserting the fields into the Credentials table.|Orlando|
|CMP: Azure Service Account|Add Azure service account by inserting the fields into the service account table.|Orlando|
|CMP: Update datacenter type|Update the Cloud Service account with the datacenter type.|Orlando|
|CMP: Creating Resource Group|Creating Resource Group to provision Azure stack via ARM Template.|Orlando|
|CMP: Create Azure Logical datacenter.|Create Azure Logical datacenter for provisioning resources.|Orlando|
|CMP: Create "Contains: Contained by" relationship.|Create "Contains: Contained by" relationship between Resource Group and Azure datacenter.|Orlando|
|CMP: Create 'Hosted on' relationship.|Create hosted on relationship between logical datacenter and Cloud Service account.|Orlando|
|CMP: Create Cloud Account|Create cloud account by inserting the fields into the cloud account table.|Orlando|
|CMP: Cloud account and Logical datacenter association|Create an association between CMP cloud account and Logical datacenter.|Orlando|
|CMP: Create Catalog Item|Create Cloud Catalog Item with ARM Template.|Orlando|
|CMP: Create template version.|Create Cloud Template Version for Cloud Catalog Item.|Orlando|
|CMP: ARM template body|Update Cloud Template Version with ARM template body.|Orlando|
|CMP: Open the 'ServiceNow Cloud Template Versions'|Open the 'ServiceNow Cloud Template Versions' GUI page.|Orlando|
|CMP: Activate Cloud Template Version|Activate Cloud Template Version to create resource block, blueprint, and catalog.|Orlando|
|CMP: Verify the Cloud Template Version.|Validate whether status is Success and state is active in the Cloud Template Version after Activation operation.|Orlando|
|CMP: Activate Cloud Catalog Item|Activate Cloud Catalog Item to display catalog order form to the cloud user.|Orlando|
|CMP: Add stack and resource group name in Catalog item|Set the default value for stack name and resource group in the catalog item.|Orlando|
|CMP: Verify whether stack is present|Validate whether stack is available with name "ATFARMStack".|Orlando|
|CMP: Open Cloud Catalog Item page|Open Cloud Catalog Item page in the Service Portal.|Orlando|
|CMP: Submit Catalog form|Submit the Catalog Form to start provisioning ARM stack.|Orlando|
|CMP: Verify whether stack status is active|Validate the status of a stack after provisioning the stack.|Orlando|
|CMP: Verify stack status after Day2 - Stop operation|Validate the status of the stack status changed from 'On' to 'Off' after the Stop operation.|Orlando|
|CMP: Verify stack status after Day2 - Start operation|Validate the status of the stack status changed from 'Off' to 'On' after the Start operation.|Orlando|
|CMP: Verify stack status after Day2 - Deprovision operation|Validate the status of the stack status changed from 'On' to 'Terminate' after the de-provisioning operation.|Orlando|

|Test|Description|Release version|
|----|-----------|---------------|
|CMP: Add AWS Credentials|Add AWS credentials by inserting the fields into the credential table.|Orlando|
|CMP: AWS Service Account|Add AWS service account by inserting the fields into the service account table.|Orlando|
|CMP: Update datacenter type|Update the cloud service account with the datacenter type.|Orlando|
|CMP: Create logical datacenter|Create Logical datacenter for provisioning the resources.|Orlando|
|CMP: Create hosted on relationship|Create hosted on relationship between logical datacenter and Cloud Service account.|Orlando|
|CMP: Create Cloud Account|Create cloud account by inserting the fields into the cloud account table.|Orlando|
|CMP: Cloud account and Logical datacenter association|Create an association between CMP cloud account and logical datacenter.|Orlando|
|CMP: Create Catalog Item|Create Cloud Catalog Item with the CFT Template.|Orlando|
|CMP: Create template version|Created Cloud Template Version for a Cloud Catalog Item.|Orlando|
|CMP: CFT template body|Update Cloud Template Version with the CFT template body.|Orlando|
|CMP: Open the ' ServiceNow Cloud Template Versions'|Open the ' ServiceNow Cloud Template Versions' GUI page.|Orlando|
|CMP: Activate Cloud Template Version|Activate Cloud Template Version to crate resource block, blueprint, and catalog.|Orlando|
|CMP: Verify the Cloud Template Version|Validate the Cloud Template Version whether status is Success and state is active after Activation operation.|Orlando|
|CMP: Activate Cloud Catalog Item|Activate Cloud Catalog Item to display the catalog order form to the cloud user.|Orlando|
|CMP: Add stack name in Catalog item|Set the default value for stack name in the catalog item.|Orlando|
|CMP: Verify whether stack is present|Validate whether stack is available with name "ATFCFTStack".|Orlando|
|CMP: Open Cloud Catalog Item page|Open the Cloud Catalog Item page in the Service Portal.|Orlando|
|CMP: Submit Catalog form|Submit the Catalog Form to start provisioning CFT Stack.|Orlando|
|CMP: Verify whether stack status is active|Validate the status of the stack after provisioning the stack.|Orlando|
|CMP: Verify stack status after Day2 - Stop operation|Validate the status of the stack status changed from 'On' to 'Off' after the Stop operation.|Orlando|
|CMP: Verify stack status after Day2 - Start operation|Validate the status of the stack status changed from 'Off' to 'On' after the Start operation.|Orlando|
|CMP: Verify stack status after Day2 - De-provision operation|Validate the status of the stack status changed from 'On' to 'terminate' after the de-provisioning operation.|Orlando|

To learn more about Cloud Provisioning and Governance, see [Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

## Coaching

Coaching quick start tests requires activation of the Coaching plugin \(com.sn\_coaching\).

|Test|Description|Release version|
|----|-----------|---------------|
|Coaching: Create an assessment manually when logged in as a coach.|As a coach, verify that you can create an assessment and assign it to trainees.|Orlando|
|Coaching: Add skills to an opportunity and verify those skills awarded to trainee.|Add skills to a coaching opportunity and verify that those skills have been awarded to trainees after they complete an assessment.|Orlando|
|Coaching: Complete an assessment as a virtual coach.|Verify that the virtual coach completes an assessment and provides feedback to the trainee when a virtual coach is attached to an opportunity.|Orlando|
|Coaching: Add skills to an assessment and verify those skills awarded to trainee.|Add skills to a coaching assessment and verify that those skills have been awarded to trainees after they complete an assessment.|Orlando|
|Coaching: Add skills to a recommendation and verify those skills awarded to trainee.|Add skills to a coaching recommendation and verify that those skills have been awarded to trainees after they complete an assessment.|Orlando|
|Coaching: Move assessments from one state to another when logged in as a coach.|As a coach, verify that you can move an assessment from one state to another.|Orlando|
|Coaching: Attach a recommendation learning to an assessment.|Verify that a recommendation learning on an opportunity gets attached to an assessment when an assessment is generated.|Orlando|
|Coaching: When a coaching opportunity is inactive, assessments are not generated.|Verify that when a coaching opportunity is in inactive state, it does not generate assessments.|Orlando|
|Coaching: Submit Coaching survey as a Coach user.|Verify that coach can submit survey for a trainee.|Quebec|
|Coaching: Submit Coaching survey as a Traineer user.|Verify that trainee can submit survey for a coach.|Quebec|

To learn more about coaching, see [Coaching](https://www.servicenow.com/docs/access?context=coaching-landing&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Communities

Communities quick start tests require activating the Customer Communities plugin \(com.sn\_customer\_communities\) and the Communities Demo Data plugin \(com.sn\_communities\_demo\).

|Test|Description|Release version|
|----|-----------|---------------|
|Post question and validate feed|Verify that a question is posted in the community and validate whether it appears in the content feed.|Madrid|
|Post video|Verify that a video is posted in the community.|Madrid|
|Forum membership approval|Verify that a membership request to a forum is approved.|Madrid|
|Forum membership reject|Verify that a membership request to a forum is rejected.|Madrid|
|Approve a moderation task|Verify that a moderation task is approved.|Madrid|
|Reject a moderation task|Verify that a moderation task is rejected.|Madrid|
|Topic subscription and activity feed validation|Verify that a topic is subscribed to and the topic activities appear in the activity feed.|New York|
|Approve content approval workflow task on question|Verify the content approval workflow of a question.|New York|
|Question auto-subscription and activity feed validation|Verify that the author is automatically subscribed to the question and the question activities appear in the activity feed.|New York|
|Follow a user|Verify that a community user is able to follow another community user.|New York|
|Reject content approval workflow task on question|Verify the content approval workflow of a question when content is rejected.|New York|
|Gamification on video posting|Verify the gamification points gained when posting a video.|New York|
|Forum subscription and activity feed validation|Verify that a forum is subscribed to and the forum activities appear in the activity feed.|New York|
|Question subscription and activity feed validation|Verify that a question is subscribed to and the question activities appear in the activity feed.|New York|
|Post a video with 'Disable comment' option|Verify a video is posted with `Disable comments` option as selected.|Orlando|
|Pin a video as Featured|Verify that a video is marked as featured by community administrator in the forum and community home page.|Orlando|

To learn more about Communities, see [Communities](https://www.servicenow.com/docs/access?context=servicenow-communities&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

## Configuration Compliance

Configuration Compliance quick start tests require activating the Configuration Compliance application \(sn\_vulc\) and loading the demo data.

|Test|Description|Release version|
|----|-----------|---------------|
|Configuration Compliance Assignment Rules|Create an assignment rule.|Xanadu|
|Configuration Compliance - Reapply Group Rule|Reapply a test result group rule.|Xanadu|
|Configuration Compliance - Delete Group Rule|Delete a test result group rule.|Xanadu|

To learn more about Configuration Compliance, see [Configuration Compliance](https://www.servicenow.com/docs/access?context=vr-config-compliance-landing&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).

## Configuration Management Database \(CMDB\)

Configuration Management Database \(CMDB\) quick start tests require activating the Configuration Management \(CMDB\) plugin \(com.snc.cmdb\) and the CMDB - ATF Tests plugin \(com.snc.cmdb.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB BSM: Dependency Views|Test functionality of Dependency Views APIs. These APIs retrieve Dependency Views map and associated map items such as context menu items, for a given CI sys\_id and using itil user role.|New York|

<table id="table_ipl_qdw_nhb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

CMDB HEALTH: Health Job Status

</td><td>

Checks whether any CMDB Health dashboard jobs, which were started 30 or more days ago, are still in progress.

</td><td>

New York

</td></tr><tr><td>

CMDB HEALTH: CMDB Health Completeness/ Recommended

</td><td>

Checks whether the recommended metric \(included in the CMDB Health completeness KPI\) is fully functional.This test validates:

-   Creation of a health inclusion rule for the recommend metric.
-   Creation of a recommended field that satisfies the health inclusion rule.
-   Validate that the health inclusion rule is correctly applied to a test record with missing data in the recommended field.

</td><td>

New York

</td></tr></tbody>
</table><table id="table_zxd_11g_klb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

CMDB IRE: IRE Validation

</td><td>

Validate CI identifiers and reconciliation definitions and check indexes for CI identifiers.

</td><td>

Madrid

</td></tr><tr><td>

CMDB IRE: Reconciliation Rule

</td><td>

Check operations on a reconciliation rule, in CI Class Manager, using itil and itil\_admin roles. Operations include create, edit, and delete a reconciliation rule.

 Also, check for active and not active setting, and derived rules.

</td><td>

Paris

</td></tr><tr><td>

CMDB IRE: Identification Rule

</td><td>

Check operations on an identification rule, in CI Class Manager, using itil and itil\_admin roles. Operations include create, edit, and delete an identification rule.

 Also, check for active and not active setting, and derived rules.

</td><td>

Paris

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|CMDB QB: Query Builder - cmdb\_query\_builder Role|Verify that cmdb\_query\_builder user role can save queries, and access and run all saved queries, in CMDB Query Builder.|New York|
|CMDB QB: Query Builder - cmdb\_query\_builder\_read Role|Verify that cmdb\_query\_builder\_read user role can access and run all saved queries, and cannot save any query, in CMDB Query Builder.|New York|

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB REL EDITOR:Relationship Editor|Check addition of relations to a CI and deletion of relations from a CI using itil user role.|New York|
|CMDB REL FORMATTER:Relationship Formatter|Check accuracy of CI information, relationship types, relationships, associated records such as change tickets, and settings such as CMDB views \(relationship filters\), displayed for a specific CI in relationship formatter using itil user role.|New York|

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB SDK: Query CMDB Metadata|Test querying CMDB metadata.|New York|
|CMDB SDK: Create a relation for a CI using REST APIs|Test creation of a relationship for a CI in the CMDB using the CMDB REST APIs.|New York|
|CMDB SDK: Delete a relation for a CI using REST APIs|Test deletion of a relationship for a CI using CMDB REST APIs.|New York|
|CMDB SDK: Create a CI using REST API|Test creation of a CI using CMDB REST APIs.|New York|
|CMDB SDK: Query CMDB using REST APIs|Test querying the CMDB using CMDB REST APIs.|New York|
|CMDB SDK: Update a CI using REST APIs|Test updating of a CI using CMDB REST APIs.|New York|
|CMDB SDK: Query for a CI using REST APIs|Test querying a CI using CMDB REST APIs.|New York|

To learn more about Configuration Management Database, see [Configuration Management Database](https://www.servicenow.com/docs/access?context=c_ITILConfigurationManagement&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Continual Improvement Management

Continual Improvement Management quick start tests require activating the Continual Improvement Management Automated Tests plugin \(com.sn\_cim.atf\)

|Test|Description|Release version|
|----|-----------|---------------|
|CIM: Inbound integration from Assessments|Create an improvement initiative from an assessment.|Paris|
|CIM: Inbound integration from Incident Management|Create an improvement initiative from an incident.|Paris|
|CIM: Inbound integration from Problem Management|Create an improvement initiative from a problem.|Paris|
|CIM: Inbound integration from Survey Management|Create an improvement initiative from a survey.|Paris|

To learn more about Continual Improvement Management, see [Continual Improvement Management](https://www.servicenow.com/docs/access?context=cim-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Customer Service Management

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
-   Walk-Up for CSM \(com.snc.walkup\_for\_csm\)

<table id="table_udf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th>

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

CSM: Register New Case Type

</td><td>

Register a case type and verify the record is created.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Project Manager create Project for an Account

</td><td>

Project Manager creates project for an account.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Project Manager identify Project Contact

</td><td>

Project manager identifies customers to a project.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Project Manager create project task and assign to a customer

</td><td>

Project manager creates project task and assigns to a customer.**Note:** Requires Customer Project Management.

</td><td>

Orlando

</td></tr><tr><td>

CSM - Create Case from Project

</td><td>

Create a case from a project.

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

CSM: Agent Creating Request for Customer

</td><td>

As a customer service agent, create a request for a customer. **Note:** Requires Customer Service Request Integration.

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

CSM: Create Major Case and its Child Cases

</td><td>

Create a major case and the associated child cases for the customer accounts in the recipient list. **Note:** Requires Major Issue Management.

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

</th><th>

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

</th><th>

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

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

CSM Walkup: Check-in as a walkup user, look at the queue, and submit a survey

</td><td>

As a walk-up user, perform check-in, look at the queue, and submit feedback through a survey.**Note:** This test works when the Seattle location, available with demo data, is available.

</td><td>

Rome

</td></tr></tbody>
</table>To learn more about Customer Service Management, see [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US).

## Dashboards

Dashboards quick start tests require activating the Automated Test Framework - Responsive Dashboards plugin \(com.glide.automated\_testing\_impl.dashboards\). This plugin is active on zBoot of the instance.

|Test|Description|Release version|
|----|-----------|---------------|
|Responsive Dashboard Sharing|Confirm dashboard sharing by impersonating users.|Madrid|
|Responsive Dashboard Visibility|Confirm dashboard visibility by impersonating users.|Madrid|

To learn more about Dashboards, see [Dashboards](https://www.servicenow.com/docs/access?context=dashboards-landing-page&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

## DevOps

DevOps quick start tests are available when you install the DevOps application from ServiceNow Store.

|Test|Description|Release version|
|----|-----------|---------------|
|DevOps Code Tool Flow|Verify the Workflow Studio flow for a DevOps coding tool.|Madrid|
|DevOps Orchestration Flow with CR|Verify the Workflow Studio flow for a DevOps orchestration tool that includes a change request.|Madrid|
|DevOps Orchestration Tool Flow|Verify the Workflow Studio flow for a DevOps orchestration tool.|Madrid|
|DevOps Plan Tool Flow|Verify the Workflow Studio flow for a DevOps planning tool.|Madrid|

To learn more about DevOps, see [DevOps Change Velocity](https://www.servicenow.com/docs/access?context=devops-landing-page-new&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Employee Center and Employee Center Pro

<table id="atf-tests-hr-esc"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Create Adhoc Delegation for Approval Task

</td><td>

Ensures an adhoc delegation for an approval task can be created from the My Tasks form in the Employee Center.

</td><td>

San Diego

</td></tr><tr><td>

Create Adhoc Delegation for HR Task

</td><td>

Ensures an adhoc delegation for an HR task can be created from the My Tasks form in the Employee Center.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - My Favorites

</td><td>

Verifies the favorite functionality in the Employee Center. Also verifies when a KB article or catalog item is added to the Favorite widget.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - Approval Hub Approve Request

</td><td>

Verifies the approval functionality in the Employee Center. Also verifies that when a request is approved, it appears in the user's **Completed** column.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - Approval Hub Reject Request

</td><td>

Verifies the rejection functionality. Also verifies that when a request is rejected, it appears in the user's **Completed** column.

</td><td>

San Diego

</td></tr><tr><td>

Employee center - Employee Profile Generation

</td><td>

Verifies that employee profiles are generated as per the employee definition.

</td><td>

Xanadu

</td></tr><tr><td>

Employee Center - Topic Page

</td><td>

Associates a KB article or catalog item to a topic and verifies they display on the topic page.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center - Validate home page widgets

</td><td>

Validates the following widgets are present on the Employee Center home page:-   Relevant for you
-   Popular topics
-   My Active Items
-   Quick tasks
-   Homepage Search

</td><td>

San Diego

</td></tr><tr><td>

Employee Center Pro - App launcher

</td><td>

Verifies the following on the My Application page:-   Creates an application and verifies it is visible on the application page.
-   Creates a topic/category and associates the application and verifies it is visible under the topic and category.

</td><td>

San Diego

</td></tr><tr><td>

Employee Center Pro - Validate home page widgets

</td><td>

Validates the following widgets are present on the Employee Center Pro home page:-   Content Experience
-   Recommended for you
-   Popular topics
-   Upcoming Events
-   My Active Items
-   Videos
-   App launcher
-   Homepage Search

</td><td>

San Diego

</td></tr><tr><td>

ESC: Employee can see ticket updates

</td><td>

Employees can view updates to their tickets.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Post General HR Inquiry questions on ESC portal

</td><td>

Verifies an HR employee can create a General Inquiry case and post general HR inquiry questions on the ESC.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Submit a Record Producer which crates Universal Request and HR Case

</td><td>

Verifies a user can submit an HR catalog item that creates a Universal Request. Also verifies the Universal Request and HR case are created and linked.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Verify Standard Ticket page on ESC for HR Case

</td><td>

Creates a general inquiry case from the service portal and verifies it appears on the standard Ticket page.

</td><td>

Quebec

</td></tr><tr><td>

ESC: Verify widget contents in Catalog items

</td><td>

Verifies the widget content in a Catalog page.

</td><td>

Orlando

</td></tr><tr><td>

ESC: Verify widget contents in knowledge pages

</td><td>

Verifies the widget content in a Knowledge page.

</td><td>

Orlando

</td></tr><tr><td>

HR: Search catalog items &amp; KBs in ESC

</td><td>

Verifies the search functionality in the ESC.

</td><td>

Quebec

</td></tr><tr><td>

Taxonomy and Topic Creation

</td><td>

Creates taxonomy and topics and then adds content to the topic.

</td><td>

San Diego

</td></tr></tbody>
</table>**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Publishing \[app-content-publishing\]
-   Content Experiences \[app-content-experiences\]

|Test|Description|Release version|
|----|-----------|---------------|
|Content Experiences: Create and Publish a Campaign|Creates and publishes a campaign with portal content and verifies against the Content Experiences portal.|Orlando|
|Content Experiences: Portal preview|Verifies that a campaign manager is able to preview portal content using the portal preview.|Rome|
|Content Experiences: Preview individual content before Publishing a Campaign|Verifies a campaign manager can preview any individual content for a campaign.|San Diego|

**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Experiences \[app-content-experiences\]

|Test|Description|Release version|
|----|-----------|---------------|
|Content Governance - New Content Request E2E Workflow|Provides end-to-end testing from creating a content request through publishing the content.|San Diego|

**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Publishing \[app-content-publishing\]
-   Content Experiences \[app-content-experiences\]
-   Content Governance \[app-content-governance\]

|Test|Description|Release version|
|----|-----------|---------------|
|Content Publishing: Audience|Tests the audience configurations for Content Publishing.|Orlando|
|Content Publishing: Create Banner type content in SCA|Ensures the Create Banner type can be created when using Streamlined Content Authoring \(SCA\) under the Content Publishing module.|Rome|
|Content Publishing: Create Styled content \(Video\) type content in SCA|Verifies an admin can create styled content that is a video type using Content Publishing.|Rome|
|Content Publishing: Schedule Portal Content|Creates and schedules test content for the Content Publishing demo portal.|Orlando|
|Create news content via Content Library|Creates and publishes a news article to the portal.|Xanadu|

**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Center Core \[app-ex-employee-center-core\]
-   Employee Center \[app-ex-employee-center\]
-   Employee Center Pro \[app-ex-employee-center-pro-content\]
-   Content Publishing \[app-content-publishing\]
-   Content Experiences \[app-content-experiences\]

## Essential SAFe

Essential SAFe quick start tests require activating the Agile - Scaled Agile Framework - Essential SAFe plugin \(com.snc.sdlc.safe\) and the Agile - Scaled Agile Framework - Essential SAFe - ATF Tests plugin \(com.snc.sdlc.safe.atf\).

<table id="table_vqt_4nd_vfb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Essential SAFe: Feature tests

</td><td>

Verify feature global rank updates.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Feature tests

</td><td>

For a SAFe feature, verify that:

-   Actual start date is populated after the state is changed to Implementation, Validation on Staging, or Deployment.
-   Actual end date is populated after the state is changed to **Released** or **Cancelled**.
-   Active flag is set to the appropriate value:
    -   **False**, if the state is changed to **Released** or **Cancelled**.
    -   **True**, for all other states.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Feature tests

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to a SAFe feature using the **Create SAFe Feature** related link on the Demand form. For more information on how to create an SAFe feature from a demand, see [Create an artifact from a demand](https://www.servicenow.com/docs/access?context=t_CrtArtftDmdMnu&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

</td><td>

Quebec

</td></tr><tr><td>

Essential SAFe: Program increment tests

</td><td>

Verify program increment date overlapping.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Sprint tests

</td><td>

Verify the generation of ART sprints and team sprints as well as updates to sprint points and dates.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Sprint tests

</td><td>

Verify that any update to the **Group capacity** field of the assignment group results in the following changes to the **Group capacity** field of the various sprints associated with this assignment group:

-   For the sprints that are in the **Draft** or **Planning** states:
    -   The group capacity is updated to the new value.
    -   The **Group capacity** field is editable.
-   For the sprints in the **Current**, **Complete**, or **Cancelled** states:
    -   The group capacity remains the old value.
    -   The **Group capacity** field is read-only.

 For the sprints in the **Draft** or **Planning** state, you can individually edit the group capacity of the sprint anytime later. This would not change the group capacity of the assignment group associated with this sprint.

</td><td>

Paris

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify story global rank updates.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify that active flag of the SAFe story is set to the appropriate value:

-   **False**, if the state of the state is changed to Completed or Cancelled.
-   True, for all other states.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify that adding, estimating, removing, deleting, updating, or cancelling a SAFe story updates the SAFe feature-level and then the epic-level roll-ups correctly.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

Verify that adding, updating, or deleting the feature on a SAFe story updates the Epic field on the SAFe story form.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Story tests

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to a SAFe story using the **Create SAFe Story** related link on the Demand form. For more information on how to create a SAFe story from a demand, see [Create an artifact from a demand](https://www.servicenow.com/docs/access?context=t_CrtArtftDmdMnu&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

</td><td>

Quebec

</td></tr><tr><td>

Essential SAFe: Team tests

</td><td>

Verify team association with an ART.

</td><td>

Madrid

</td></tr><tr><td>

Essential SAFe: Epic tests

</td><td>

For a SAFe epic, verify that:-   Actual start date is populated after the state is changed to **Implementation**.
-   Actual end date is populated after the state is changed to **Complete**.
-   Active flag is set to the appropriate value:
    -   **False**, if the state is changed to **Released** or **Cancelled** states.
    -   **True**, for all other states.

</td><td>

Orlando

</td></tr><tr><td>

Essential SAFe: Epic tests

</td><td>

If the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is active, verify that a Demand can be converted to a SAFe epic using the **Create SAFe Epic** related link on the Demand form.For more information on how to create a SAFe epic agile from a demand, see [Create an artifact from a demand](https://www.servicenow.com/docs/access?context=t_CrtArtftDmdMnu&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

</td><td>

Quebec

</td></tr><tr><td>

Essential SAFe: Program PI Objective tests

</td><td>

Verify the functionality of creating and updating PI objectives-   Verify that you can create a program increment-level objective
-   Verify that you can update the created PI objective with the planned business value \(PBV\) and actual business value \(ABV\)
-   Verify that the percentage of business value achieved is computed as the percentage of ABV complete, for only the committed PI objectives, as compared to the PBV of the program in the PI

</td><td>

Rome

</td></tr><tr><td>

Essential SAFe: Team PI Objective tests

</td><td>

Verify the functionality of creating and updating team PI Objectives-   Verify that you can create a team-level PI objective
-   Verify that you can update the created PI objective with the planned business value \(PBV\) and actual business value \(ABV\)
-   Verify that the percentage of business value achieved is computed as the percentage of ABV complete, for only the committed PI objectives, as compared to the PBV of the team in the PI

</td><td>

Rome

</td></tr></tbody>
</table>To learn more about Essential SAFe, see [Essential SAFe](https://www.servicenow.com/docs/access?context=essential-overview&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Event Management

Event Management quick start tests require activating the Event Management plugin \(com.glideapp.itom.snac\).

|Test|Description|Release version|
|----|-----------|---------------|
|EMSelfMonitoring|Track problems with the Event Management plugin after upgrade. To understand the details of issues found, open the All Alerts list and search for alerts that failed, whose source is `EMSelfMonitoring`, and that were opened or reopened since the upgrade. The exact time for filtering can be found in the error message.|Madrid|

To learn more about Event Management, see [Event Management](https://www.servicenow.com/docs/access?context=c_EM&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

## Field Service Management

Field Service Management quick start tests are available when you enable the Field Service Management plugin \(com.snc.work\_management\). Enable the demo data plugin \(com.snc.work\_management.demo\) in a non-production instance to start using the quick start tests available with your application. Activate Field Service Contractor Management plugin \(com.snc.fsm\_contractor\_management\) to execute the External contractor related tests. You can also modify existing data and customize it to run the quick tests.

<table id="table_agf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

FSM: Create Initiate Qualify Dispatch and assign Work Order Task

</td><td>

-   Create a work order.
-   Initiate and qualify a work order.
-   Dispatch a work order.
-   Assign a work order task to an agent.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Part Sourcing

</td><td>

-   Source any part to an agent's stock room from the work order task.
-   Create a transfer order line for the part sourcing.
-   Use this part for any work order to consume it using the **Part Usage** action.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Part Usage

</td><td>

-   Source any part to an agent's stock room from the work order task.
-   Use this part for any work order to consume it using the Part Usage action.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Questionnaire

</td><td>

Create a questionnaire and associate it with a work order task.

</td><td>

Madrid

</td></tr><tr><td>

FSM: Field Service Configuration

</td><td>

Verify that the default configuration such as task assignment method, qualification requirement, PDF summary and agent's ability to accept or reject tasks is preserved.

</td><td>

New York

</td></tr><tr><td>

FSM: Planned Maintenance

</td><td>

Create a planned maintenance work order with weekly interval time for printer maintenance.

</td><td>

New York

</td></tr><tr><td>

FSM: Appointment Booking Configuration

</td><td>

Verify that the default configuration for appointment booking is preserved and that the point of sale service and catalog item exists in the system.

</td><td>

New York

</td></tr><tr><td>

FSM: Create Work or Personal Schedules

</td><td>

Create personal or work schedule for agents.

</td><td>

Orlando

</td></tr><tr><td>

FSM: Field Service Property Settings

</td><td>

Verify that the field service system properties preserve expected values.

</td><td>

Orlando

</td></tr><tr><td>

FSM: Work Groups

</td><td>

Verify that field service agents can be added to work groups.

</td><td>

Orlando

</td></tr><tr><td>

FSM: Dynamic Scheduling - Preferred Technician assignment with mandatory parts reservation

</td><td>

With Dynamic scheduling:-   Preferred technician should be picked for task assignment.
-   Mandatory parts should be reserved in the agent stock room.

 **Note:** Activate Customer service management demo data plugin.

</td><td>

Paris

</td></tr><tr><td>

FSM: Create Time Card

</td><td>

Verify that a time card is created for an agent in the work order task.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Create incidental

</td><td>

Verify that an incidental is created for an agent in the work order task.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Onboarding contractor company

</td><td>

Verify that a contractor company is onboarded with assignment group, external manager, and external agent.**Note:** Activate Field Service Contractor Management plugin.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Onboarding contractor agent by external manager

</td><td>

Verify that an external contractor manager can onboard external agents from the Field Service Contractor Management portal.

</td><td>

Quebec

</td></tr><tr><td>

FSM: External contractor manager fulfil the work order task

</td><td>

Verify that a contractor manager or an agent is able to fulfil the assigned work order task.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Assign work order task to Vendor group

</td><td>

Verify that a work order task is assigned to the external assignment group based on the defined criteria, such as task location and configuration parameters.

</td><td>

Quebec

</td></tr><tr><td>

FSM: Pause and Resume work order task

</td><td>

Verify that an agent can pause and resume work for a work order tasks.

</td><td>

Rome

</td></tr><tr><td>

FSM: Dynamic Scheduling - Assign technician with matching skills

</td><td>

With Dynamic Scheduling: Verify that a work order task is assigned to a technician who possesses all mandatory skills mentioned in the task.

</td><td>

Rome

</td></tr><tr><td>

FSM: Off boarding contractor agent by external manager

</td><td>

Verify that an external contractor manager can off board external agents from the Field Service Contractor Management portal.

</td><td>

Rome

</td></tr><tr><td>

FSM: External contractor manager asset sourcing and usage

</td><td>

Verify that an external contractor manager is able to perform the following actions: -   Request parts from stockroom.
-   Pick the part.
-   Close the transfer order.
-   Perform work using the part.

</td><td>

San Diego

</td></tr><tr><td>

FSM: External contractor agent fulfil the work order task

</td><td>

Verify that a contractor agent is able to fulfil the work order task that is assigned by the external contractor manager.

</td><td>

San Diego

</td></tr><tr><td>

FSM: Capacity Scheduling - Assign work to field service agents based on capacity

</td><td>

Verify that the rules and values mentioned in the capacity definition and capacity assignment module are evaluated to assign work to the agent based on capacity.

</td><td>

Tokyo

</td></tr><tr><td>

FSM: Onboarding external contractor agent as additional manager for the external assignment group

</td><td>

Verify that when onboarding an external agent for the contractor company, you can assign the additional manager role to the agent.

</td><td>

Tokyo

</td></tr><tr><td>

FSM: Dispatcher Workspace - Assign crews to work order tasks that require a group of agents to work on them

</td><td>

-   Verify that a dispatcher with the crew moderator role can create a crew in the Dispatcher Workspace.
-   Verify that a dispatcher with the crew moderator role can assign a work order task to the planned crew in the Dispatcher Workspace

</td><td>

Tokyo

</td></tr><tr><td>

FSM: Work order task supports Multi-day task scheduling

</td><td>

Verify the Multiday task scheduling functionality:-   Create Work order, work order task, and agent schedule records.
-   Select the Assign across schedule entries option in the work order task.
-   Assign an agent to the work order task for which the task duration is more than a day.
-   Verify that work order task is assigned successfully to the agent and the estimated end time is populated correctly.

</td><td>

Tokyo

</td></tr><tr><td>

Verify creating a work order from a case and assigning a work order task to an agent from CSM/ FSM Configurable Workspace

</td><td>

-   Verify you can create a work order from a case.
-   Qualify the work order and verify a work order task is created.
-   Assign the work order task to an agent and verify the agent it is assigned to is updated correctly.

</td><td>

Xanadu

</td></tr></tbody>
</table>## Finance Close Automation

Finance Close Automation quick start tests are available when you install the Finance Close Automation application from ServiceNow Store.

|Test|Description|Release version|
|----|-----------|---------------|
|FCA: Applicable Months sub-set tests|Verify that the Applicable months can only be sub-set of functional workbook.|New York|
|FCA: dates validations|Verify that the date related calculations are correct.|New York|
|FCA: task relationships|Verify that dates and states are updated correctly for the tasks having relationships.|New York|
|FCA: relationship with parent tasks|Verify that dates and states are updated correctly for tasks that have relationship with parent tasks.|New York|
|FCA: Reset Task|Verify the FCA workflow when the task is reset.|New York|
|FCA: Reject Task|Verify the FCA workflow when the task is rejected.|New York|
|FCA: Create JE Task|Verify that ERP source is available for a Journal Entry task type.|New York|
|FCA: Negative values as close day|Verify that both the positive and negative values are acceptable for close day and the planned dates are calculated correctly.|New York|
|FCA: Close day checks for Daily close Checklist|Close day verifications in daily close workbook.|New York|
|FCA: Daily close planned end date checks|Verify planned end dates in a daily close workbook.|New York|
|FCA: Kickstart errors|Verify that all the kickstart validations run.|New York|
|FCA: One final task verification|Verify that there is only one final task in each functional workbook.|New York|
|FCA: Confidential task|Verify that only the owner, reviewer, and approver of a confidential task can view the task.|New York|
|FCA: Unique checklist Verification|Verify that only one workbook is created for a specific day or period.|New York|
|FCA: Milestone and JE Validations|Verify that milestone and journal entry tasks don't have any child tasks.|New York|

## Financial Management

Financial Management quick start tests require activating the Financial Management Core - ATF Tests plugin \(com.snc.financial\_management.atf\)

|Test|Description|Release version|
|----|-----------|---------------|
|Verify FM Cost Allocation Flow|Verify the cost allocation flow in financial modeling.|Madrid|

To learn more about Financial Management, see [Financial Management](https://www.servicenow.com/docs/access?context=c_ITFinance&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Granular Delegation

Granular Delegation quick start tests require activating the Granular Delegation \(com.glide.granular\_service\_delegation\) plugin.

|Test|Description|Release version|
|----|-----------|---------------|
|\[Delegation\] Admin - Adding a delegation rule with delegator and delegate user criteria|Ensures a delegate or delegator honors the user criteria assigned to an HR task.|Xanadu|

## GRC Audit Management

GRC: Audit Management quick start tests require activating the GRC: Audit Management plugin \(com.sn\_audit\) and loading the demo data.

<table id="atf-tests-audit-management"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

GRC: Create Audit Engagement and Generate Audit Task

</td><td>

Validates audit engagement creation and associates entities to generate controls and test plans. Generates audit task which is associated to a test plan.

</td><td>

Paris

</td></tr><tr><td>

GRC: Create and process a milestone

</td><td>

Create a milestone in an engagement, notice that the due date cannot be in past and the completion date cannot be in future and for a milestone in open state the percent complete is 0 which changes in accordance with the milestone state change.

</td><td>

Paris

</td></tr><tr><td>

GRC: Cost and Resource plan rollup

</td><td>

Create an audit plan and associate an engagement to it, on adding cost plan and resource plan to this engagement, notice that these costs are rolled up to the plan. Any edits to these costs in engagement reflects in the plan.

</td><td>

Paris

</td></tr><tr><td>

GRC: Create Engagement Project Manual and automatic

</td><td>

On an engagement in the validate state, once the Enable advanced planning ui-action is performed notice an engagement project gets created and when the state of an engagement associated to an audit plan having "Advanced planning capabilities" is changed to validate notice that an engagement project gets created automatically.

</td><td>

Paris

</td></tr><tr><td>

GRC: Auditable Unit with Detailed Risk Assessment

</td><td>

Create an Auditable unit with method as "Detailed Risk Assessment" and request for Assessing the Risk Assessment by adding the Assessor once the assessor responds and Marks Assessment as Complete after performing the control assessment and residual assessment, the risk assessment fields should be auto updated.

</td><td>

Paris

</td></tr></tbody>
</table>To learn more about Audit Management, see [Audit Management](https://www.servicenow.com/docs/access?context=c_GRCAudits&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

## GRC Continuous Authorization and Monitoring

GRC: Continuous Authorization and Monitoring quick start tests require activating the Continuous Authorization and Monitoring plugin \(com.sn\_compliance\) and loading the demo data.

<table id="atf-tests-cam"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

GRC: System Owner create and validate responsibilities and roles for an AB and AP

</td><td>

System Owner creates and validates responsibilities and roles for an Authorization Boundary and Authorization Package.Information Owners and System User are pre-populated when selecting the Authorization Boundary.

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr><tr><td>

GRC: System Owner validate App Modules visibility

</td><td>

Verifies that the system owner persona is able to view the Continuous Authorization &amp; Monitoring application menu and the following modules under that menu:-   All Authorization Boundaries
-   All Authorization Packages
-   Information Type Library
-   Control Overlays
-   Control Objectives
-   Controls
-   All Engagements

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr><tr><td>

GRC: System Owner Request First approval &amp; My approvals module

</td><td>

System Owner requests an approval.

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr><tr><td>

SO: Create and validate responsibilities and roles for an AB and AP

</td><td>

Verifies if a system owner can create an Authorization Boundary by completing the fields on the Authorization Boundary form. Also verify if the same SO can create an Authorization Package from the form view.

</td><td>

Quebec \(compatible with Paris and Orlando\)

</td></tr></tbody>
</table>To learn more about Continuous Authorization and Monitoring, see [Continuous Authorization and Monitoring](https://www.servicenow.com/docs/access?context=grc-cam-landing-page&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

## GRC Policy and Compliance Management

GRC: Policy and Compliance Management quick start tests require activating the Policy and Compliance Management plugin \(com.sn\_compliance\) and loading the demo data.

|Test|Description|Release version|
|----|-----------|---------------|
|GRC: Create Controls|Validates control creation.|Madrid|
|GRC: Create Policy Exception and Flow|Create a policy exception and navigate through its states.|Paris|
|GRC: Policy Lifecycle|Create a policy and navigate through its states.|Paris|

To learn more about Policy and Compliance Management, see [Policy and Compliance Management](https://www.servicenow.com/docs/access?context=r_PolicyComplianceMgmt&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

## GRC Risk Management

GRC: Risk Management quick start tests require activating the Risk Management plugin \(com.sn\_risk\) and loading demo data.

|Test|Description|Release Version|
|----|-----------|---------------|
|GRC: Create Profile|Validate profile creation.|Madrid|
|GRC: Create Risk|Validates risk creation.|Madrid|
|GRC: Create Control|Validates control creation.|New York|
|GRC: Create Control Objective and Generate Controls|Validates control objective creation and associates profiles to generate controls.|New York|
|GRC: Create Issue|Validates issue creation|New York|
|GRC: Accept an Issue|Validates all the states of an issue till it is closed by accepting the issue.|New York|
|GRC: Remediate an Issue|Validates issue cannot be closed be with an open remediation task.|New York|
|GRC: ATF Flow for Indicator \(Manual\):|Create an indicator template with type manual and associate a control objective to it. Execute one of the indicators thus formed. Mark the state of the indicator task created as closed and result as failed. The associated control will become non- compliant and an issue will be generated.|New York|
|GRC: ATF flow for Indicator \(Basic\)|Create an indicator template with type basic and result as failed. Associate a control objective to it and give the supporting data. Execute one of the indicators thus formed. The associated control will become non- compliant and an issue will be generated.|New York|
|GRC: ATF flow for indicator \(Script\)|Create an indicator template with type script and enter a script and set the value of result.passed and result.value. Associate a control objective to it. Execute one of the indicators. The associated control will become non-compliant and an issue will be generated.|New York|

To learn more about Risk Management, see [Risk Management](https://www.servicenow.com/docs/access?context=grc-risk-overview&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).

## Hardware Asset Management

Hardware Asset Management quick start tests are available when you install the Hardware Asset Management \(HAM\) application from the ServiceNow Store.

<table id="table_mhx_1d3_nlb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

HAM - Hardware Normalization

</td><td>

Validates the various normalization status values based on the normalized Manufacturer, Product, and Model.

</td><td>

Orlando

</td></tr><tr><td>

HAM - Hardware Asset Disposal work flow

</td><td>

Validates asset disposal work flow.

</td><td>

Paris

</td></tr><tr><td>

HAM - Automating Asset deploy workflow

</td><td>

Validates asset deployment work flow.

</td><td>

Paris

</td></tr><tr><td>

HAM - Automating Asset Swap workflow

</td><td>

Validates Asset Exchange/Swap work flow.**Note:** Requires demo data.

</td><td>

Paris

</td></tr><tr><td>

HAM - Standard Hardware Asset Request Flow

</td><td>

Validates the Standard Hardware Asset Request flow, which is a part of the Hardware Asset Management application.

</td><td>

Paris

</td></tr><tr><td>

HAM - Hardware Asset Refresh flow

</td><td>

Validates asset refresh workflow.

</td><td>

Quebec

</td></tr><tr><td>

HAM - Loaner Asset Allocation Flow

</td><td>

Validates loaner asset workflow.

</td><td>

Quebec

</td></tr><tr><td>

HAM - Lease Contract Asset Expiration

</td><td>

Validates leased contract asset expiration end to end workflow, performing return or extend of the assets covered in the lease contract.

</td><td>

Quebec

</td></tr><tr><td>

HAM - Asset RMA Flow

</td><td>

Validates the asset Return Merchandise Authorisation \(RMA\) workflow with Inventory User.

</td><td>

Rome

</td></tr><tr><td>

HAM - Asset RMA Flow \(SP\)

</td><td>

Validates the asset Return Merchandise Authorisation \(RMA\) workflow from Service Portal.

</td><td>

Rome

</td></tr><tr><td>

HAM - Loaner Asset Request Flow

</td><td>

Validates the Loaner asset allocation workflow with Inventory Admin user.

</td><td>

Rome

</td></tr><tr><td>

HAM - Contract Renewal Flow

</td><td>

Validates the Contract Renewal flow with Contract Manager user.

</td><td>

Tokyo

</td></tr></tbody>
</table>To learn more about Hardware Asset Management, see [Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

## HR Service Delivery

<table id="atf-tests-hr-case"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Case Creation Configuration

</td><td>

Validates an HR service has a case creation configuration and is populated into the HR case form when creating an HR case for that HR service.

</td><td>

Xanadu

</td></tr><tr><td>

Create Document template block and block content

</td><td>

Verifies a document template block and document template content are created for block content.

</td><td>

Xanadu

</td></tr><tr><td>

Create HR Employee Document

</td><td>

Creates an employee document and ensures the Attachment \[sys\_attachment\] table points back to the record in the Employee Document \[sn\_hr\_ef\_employee\_document\] table.Verifies that the employee document is accessible from the Employee Center or Employee Center Pro via the employee HR profile.

</td><td>

 

</td></tr><tr><td>

Create Employee Document with Active Document Type

</td><td>

Validates the creation of:-   One active document type
-   One inactive document type
-   Employee file with active document type

 **Note:** Human Resources Scoped App: Core \(com.sn\_hr\_core\) and Employee Document Management \(com.sn\_employee\_document\_management\) must be activated.

</td><td>

Xanadu

</td></tr><tr><td>

\[Delegation\] Admin - Adding a delegation rule with delegator and delegate user criteria

</td><td>

Verifies that user criteria for a delegation rule works correctly,

</td><td>

San Diego

</td></tr><tr><td>

E2E test for Bulk Case Creation

</td><td>

Verifies that bulk cases can be created for selected users in a specific user segment.

</td><td>

San Diego

</td></tr><tr><td>

ER: Case Restriction

</td><td>

Verifies that restricted cases are only viewable by users with the sn\_hr\_er.confidential role.

</td><td>

San Diego

</td></tr><tr><td>

HR: Case updates visible to employees

</td><td>

Cases created and updated by an HR agent are visible to the Opened for or Subject person

</td><td>

Quebec

</td></tr><tr><td>

HR: Creation of 401k enrollment case from portal

</td><td>

Creates a 401\(k\) enrollment case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

Madrid

</td></tr><tr><td>

HR: Creation of Employee Relations case from ESC portal

</td><td>

Creates a Disciplinary Issue case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

New York

</td></tr><tr><td>

HR: Creation of Employment Verification Letter case from ESC portal

</td><td>

Creates an Employment Verification Letter case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

Madrid

</td></tr><tr><td>

HR: Creation of Payroll case from ESC portal

</td><td>

Creates a direct deposit payroll setup case from the Employee Center or Employee Center Pro.Verifies that the case creates successfully.

</td><td>

New York

</td></tr><tr><td>

HR: Creation of Tuition Reimbursement request from portal

</td><td>

Creates a Tuition Reimbursement Request case from the Employee Center or Employee Center Pro. Verifies that the case creates successfully.

</td><td>

Madrid

</td></tr><tr><td>

HR: Fulfillment Instructions

</td><td>

Verifies that fulfillment instructions are created for a specific condition for an opened for user. Also verifies the fulfillment instructions change when the details of the case changes.

</td><td>

Orlando

</td></tr><tr><td>

HR: Fulfillment Instructions conditions for COE specific fields

</td><td>

Verifies the conditions for COE specific fulfillment instruction.Fulfillment instructions update on an HR case based on the conditions defined in the fulfillment instructions.

</td><td>

Quebec

</td></tr><tr><td>

HR: General Benefits Inquiry Case Creation

</td><td>

Creates a General Benefits case using the native UI.It also verifies that the case opens and can be updated after case creation.

</td><td>

Madrid

</td></tr><tr><td>

HR: Payroll Discrepancy Case Creation

</td><td>

Creates a Payroll Discrepancy case using the native UI.It also verifies that the case opens and can be updated after case creation.

</td><td>

Madrid

</td></tr><tr><td>

HR: Reclassify Case Transfer

</td><td>

Tests when an HR case transfers from one COE \(HR service\) to a different COE using the reclassify \(HR case number remains the same\) method.

</td><td>

Orlando

</td></tr><tr><td>

HR: Response Template Configuration

</td><td>

Creates a response template for a payroll case and pastes the response in the worknotes.

</td><td>

Quebec

</td></tr><tr><td>

HR: Search catalog items &amp; KBs in ESC

</td><td>

Verifies the search functionality in the Employee Center or Employee Center Pro.

</td><td>

Orlando

</td></tr><tr><td>

HR: Standard Case Transfer

</td><td>

Tests an HR case transfers from one COE \(HR service\) to a different COE using the standard \(creates HR case number and deletes old number\) case transfer.

</td><td>

Orlando

</td></tr><tr><td>

HR: Suspend Case Flow

</td><td>

Tests the ability to suspend an HR case and later resume the case.

</td><td>

Rome

</td></tr><tr><td>

HR: Tuition Reimbursement Case Creation

</td><td>

Creates a Tuition Reimbursement HR case.

</td><td>

Orlando

</td></tr><tr><td>

HR: Workforce Administration Case Creation

</td><td>

Creates a Workforce Administration case, signs an employee verification letter, and generates the letter.

</td><td>

Orlando

</td></tr><tr><td>

JA: Publish &amp; edit plan details

</td><td>

Verifies the ability to delete an existing to-do in an action plan.

</td><td>

San Diego

</td></tr><tr><td>

Journey Designer: Create stage and edit stage

</td><td>

Verifies that the user can create a new stage, add a task template to the stage, edit the stage name, and delete the stage.

</td><td>

Vancouver

</td></tr><tr><td>

Journey Designer: Add task templates from scratch and edit

</td><td>

Verifies that the user can add a task template using the Build from scratch option, then edit the task template.

</td><td>

Vancouver

</td></tr><tr><td>

Journey Designer: Add existing task templates and remove task template

</td><td>

Verifies that a task template can be added to a Journey template with the Use template option, and then removed.

</td><td>

Vancouver

</td></tr><tr><td>

Learning Core Task Assignment

</td><td>

Verifies a learning task from a learning catalog can be assigned to a user.

</td><td>

San Diego

</td></tr></tbody>
</table>**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Employee Service Center \[com.sn\_hr\_service\_portal\]

|Test|Description|Release version|
|----|-----------|---------------|
|Configure HR Service for Auto Case Closure|Verifies that Lifecycle event cases are automatically closed.|Orlando|
|Create Employee request and associate it to LE case|Creates and validates that an employee request appears in the Lifecycle Event case action list.|Rome|
|Create Employee request for old ticket page|Validates if employee requests can be created from the legacy ticket page.|Xanadu|
|\[Delegation\] Admin - Adding a delegation rule with delegator and delegate user criteria|Verifies user criteria is working for delegation rules for a delegator and delegate user.|Xanadu|
|HR Lifecycle: Access Ticket page for a NewHire Onboarding Case in Employee Service Center|Verifies creation of a new hire and can access the Ticket page of the Employee Service Center.|Orlando|
|HR Lifecycle: Access ESC ticket page and todos page and complete assigned todos|Creates a Tuition Reimbursement Request case from Employee Service Center and the Complete NDA to-do from the subject person.|Orlando|
|HR LifeCycle: Request Onboarding Case Creation|Creates a Request Onboarding case using the native UI and updates the case after creation.|Madrid|
|HR Lifecycle: Trigger Rescind Workflow|Triggers the Rescind workflow for a New Hire Onboarding Lifecycle Event case.|Quebec|
|HR Lifecycle: Verify Requests page for Open and Closed cases|Verifies open and closed cases on the Requests page.|Orlando|
|HR Lifecycle: Verify search in Requests Page|Verifies the search functionality on the Requests page for open and closed cases.|Orlando|
|\[LE\]: Add Ad hoc task|Verifies an ad hoc task can be added for a Lifecycle Event case.|Xanadu|

**Note:** Requires plugin activation of:

-   Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)
-   Human Resources Scoped App: Lifecycle Events \[com.sn\_hr\_lifecycle\_events\]
-   Human Resources Scoped App: Lifecycle Events for Enterprise plugin \[com.sn\_hr\_lifecycle\_ent\]
-   Employee Service Center \[com.sn\_hr\_service\_portal\]

|Test|Description|Release version|
|----|-----------|---------------|
|Create knowledge block and attach block to article|Creates a knowledge block, publishes the block, and attaches the block to a knowledge article.|New York|
|Preview Knowledge Articles with Knowledge Blocks|Tests for preview of knowledge article that contains knowledge blocks.|New York|

**Note:** Requires plugin activation of Human Resources Scoped App: Core plugin \(com.sn\_hr\_core\)

To learn more about HR Service Delivery, see [HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-service-delivery&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

## Incident Management

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

To learn more about Incident Management, see [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Incident Management in Service Operations Workspace

Incident Management in Service Operations Workspace quick start tests are available in the base system when you install or update to Service Operations Workspace ITSM Applications \(sn-sow-itsm-cont\) 6.0 version.

|Test|Description|Release version|
|----|-----------|---------------|
|SOW Incident: Create problem from incident|Test to verify the creation of a problem record from an Incident using the **Create Problem** UI action on the Incident form.|Xanadu \(August store release, 6.0 version\)|
|SOW Incident: Verify Assign to me button functionality|Test to verify the assignment of the incident record to the logged-in user using the **Assign to me** UI option on the Record information side panel of the Incident form.|Xanadu \(August store release, 6.0 version\)|

To learn more about Incident Management in Service Operations Workspace, see [Incident Management in Service Operations Workspace](https://www.servicenow.com/docs/access?context=incident-sow&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Integration Commons for CMDB

|Test|Description|Release version|
|----|-----------|---------------|
|CMDB INT: Set Test Session Application|Modify the run server-side script to set an application name so that you can test only one integration. Otherwise, all integrations installed will be tested.|Paris|
|CMDB INT: Test Against Source Analysis|Test an integration against the values in the CMDB Integration Source Analysis \[sn\_cmdb\_int\_util\_cmdb\_integration\_source\_analysis\] table.|Paris|
|CMDB INT: Validate Application Feed|Validate all application feeds in an integration.|Paris|
|CMDB INT: Validate Discovery Source|Validate that the discovery source exists.|Paris|
|CMDB INT: Validate Entity Mappings|Validate all entity mappings of an integration.|Paris|
|CMDB INT: Validate Fields|Validate fields for CMDB Integrations.|Paris|
|CMDB INT: Validate Lookups|Validate CMDB integration lookups.|Paris|
|CMDB INT: Validate Mandatory Operations|Validate that all integrations for mandatory operations exist for mapped fields.|Paris|
|CMDB INT: Validate Operations|Validate all operations for an integration.|Paris|
|CMDB INT: Validate References|Validate CMDB integration references.|Paris|
|CMDB INT: Validate Related Entries|Validate all related classes against the data dictionary for related entries.|Paris|
|CMDB INT: Validate Relationships|Validate CMDB integration relationships.|Paris|

To learn more about Integration Commons for CMDB, see [Integration Commons for CMDB](https://www.servicenow.com/docs/access?context=integration-commons-for-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Investment Funding

The Investment Funding quick start tests require activating the Investment Funding - ATF Tests plugin \(com.snc.investment\_planning.atf\).

<table id="atf-tests-investment-funding-table"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Validation of top-down funding and unfunding

</td><td>

-   Validate that the correct amount is allocated from top investment to child investments while funding.
-   Validate that the correct amount is returned back to the top investment from the child investment while unfunding.

</td><td>

Orlando

</td></tr><tr><td>

Validation of bottom-up funding

</td><td>

-   Validate that the correct amount is requested by the child investment from the parent investment.
-   Validate that the correct amount is allocated back to the child investment from the parent investment.

</td><td>

Paris

</td></tr></tbody>
</table>To learn more about Investment Funding, see [Investment Funding](https://www.servicenow.com/docs/access?context=investment-funding-overview&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Knowledge Management

Knowledge Management quick start tests require activating the Knowledge Management Core plugin \(com.glideapp.knowledge\), the Knowledge Management Advanced Installer plugin \(com.snc.knowledge\_advanced.installer\), the Knowledge Blocks plugin \(com.snc.knowledge\_blocks\), and the Customer Service Management Demo Data plugin \(com.snc.customerservice.demo\).

<table id="table_whf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

KM : Create KCS Template Article with Approval Publish workflow

</td><td>

Verify the creation of a KCS template article with approval publish workflow.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Madrid

</td></tr><tr><td>

KM: Create MultiVersioned standard Article with approval publish workflow

</td><td>

Verify the creation of a multi-versioned standard article with approval publish workflow.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Madrid

</td></tr><tr><td>

KM: Article level subscription

</td><td>

Verify that users can subscribe to a knowledge article.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: User criteria covering canRead and canContribute for KnowledgeBase and canRead at Article level

</td><td>

Verify the creation of canRead and canContribute user criteria for knowledge base and canRead user criteria for article.**Note:** Requires the Knowledge Management Core plugin.

</td><td>

Madrid

</td></tr><tr><td>

KM: Create a KCS article from a case

</td><td>

Verify the creation of a KCS article from a case.**Note:** Requires the Knowledge Management Advanced Installer and Customer Service Management Demo Data plugins.

</td><td>

Madrid

</td></tr><tr><td>

KM: Knowledge Base Level Subscriptions

</td><td>

Verify that users can subscribe to a Knowledge Base.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: AQI

</td><td>

Verify the creation, assignment, and review of an AQI checklist.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Requestor performs search, view the article, provide feedback \(Helpful No with Feedback Task\)

</td><td>

Verify the search request, review, provision of feedback as not helpful, and creation of a feedback task for an article on the Knowledge Management Service Portal.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Create and edit an article from Feedback Task form

</td><td>

Confirm the availability of the **Create Article** and **Edit Article** buttons on a Knowledge Feedback Task form.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Search for pinned articles and checking the highest click rank

</td><td>

Verify the search request and that the click rank value of a pinned article was added to the Knowledge Searches \(ts\_query\_kb\) table.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Create an Ownership Group and check edit permissions and subscriptions

</td><td>

Verify the assignment of an article to an ownership group, that all members of the ownership group are subscribed to the article, and have permission to edit.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

New York

</td></tr><tr><td>

KM: Create, search for, and view knowledge articles with knowledge blocks

</td><td>

Verify the creation of a knowledge block and its addition to a knowledge article. Also, verify that the knowledge block content is searchable.**Note:** Requires the Knowledge Blocks plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate the Knowledge - Approval Retire workflow

</td><td>

Verify the success of Knowledge - Approval Retire workflow by retiring a published knowledge article.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate feedback task assignment to the ownership group manager

</td><td>

Verify the assignment of a feedback task to the ownership group manager of a knowledge article.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that the article template selector includes knowledge bases and article templates

</td><td>

Verify that the article template selector includes all knowledge bases with contribute access and article templates applicable to each knowledge base.**Note:** Requires Knowledge Management Advanced Installer.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate the Knowledge - Approval Publish workflow

</td><td>

Verify the success of a Knowledge - Approval Publish workflow by recalling, rejecting, and then approving a knowledge article through the approval process.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Make an outdated version of an article the latest version

</td><td>

Verify that an outdated version of a knowledge article is made the latest version.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that the mapped related articles appear in the Related articles widget

</td><td>

Verify that the related articles mapped to a knowledge article appear in the Related articles widget on the knowledge article view page.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that the mapped related catalog items appear in the Related items widget

</td><td>

Verify that the related catalog items mapped to a knowledge article appear in the Related items widget on the knowledge article view page.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Orlando

</td></tr><tr><td>

KM: Validate that a versioned article is created, published, checked out, and retired

</td><td>

Verify the success of UI actions on a versioned knowledge article by creating, publishing, updating, and retiring the knowledge article in Agent Workspace.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Quebec

</td></tr><tr><td>

KM: Verify the scheduled publish feature for knowledge articles

</td><td>

Verify the scheduled publish feature for knowledge articles by creating an article in approval publish workflow, putting it for scheduled for publish and observing the change in workflow state from the**Scheduled for publish** state to the **Published** state.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Quebec

</td></tr><tr><td>

KM: Validate the Knowledge - Approval Publish workflow in Agent Workspace

</td><td>

Verify the success of a Knowledge - Approval Publish workflow by recalling and then approving a knowledge article through the approval process in Agent Workspace.**Note:** Requires the Knowledge Management Advanced Installer plugin.

</td><td>

Quebec

</td></tr></tbody>
</table>To learn more about Knowledge Management, see [Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Leader Hub

Leader Hub quick start tests require activating the Leader Hub plugin \(sn\_egd\_lh\) and loading demo data.

<table id="table_ugs_4cx_2dc"><thead><tr><th>

Test

</th><th>

Description

</th><th class="filter">

Release version

</th></tr></thead><tbody><tr><td>

\[Leader hub\] - Validate LH flows

</td><td>

-   Verifies that the following widgets are present on the At a glance page for user Maria Davies:
    -   Org talent
    -   Skill growth area
    -   Growth engagement
-   Verifies the employee card for the leader who has accessed Leader Hub appears at the top of the organizational chart on the Org talent page.
-   Verifies that selecting the **View team details** button on a card for an employee navigates the leader to the Team details page.
-   Verifies that the Skills widget is present on the Org Skills page.

 **Note:** Requires demo data.

</td><td>

Xanadu

</td></tr></tbody>
</table>To learn more about Leader Hub, see [Leader Hub](https://www.servicenow.com/docs/access?context=td-lh-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

## Legal Request Management

Legal Request Management quick start tests require installing the following apps:

-   Legal Request Management \(sn\_lg\_ops\)
-   Legal Counsel Center \(sn\_lg\_workspace\)

|Test|Description|Release version|
|----|-----------|---------------|
|LRM: Privacy Request Test|Tests to validate submission and fulfillment of Privacy legal requests.|Utah|

To learn more about Legal Request Management, see [Legal Request Management](https://www.servicenow.com/docs/access?context=legal-management-overview&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

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

To learn more about Major Incident Management, see [Major Incident Management](https://www.servicenow.com/docs/access?context=major-incident-management&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## On-Call Scheduling

Activate the On-Call Scheduling plugin \(com.snc.on\_call\_rotation\) to run the On-Call Scheduling quick start tests.

|Test|Description|Release version|
|----|-----------|---------------|
|On-Call: Verify request time-off when PTO approval preferences is Not allowed|Verify whether you can request a time-off when PTO approval preferences is set to **Not allowed**|Orlando|
|On-Call: Create overlapping shifts without selecting a template|Verify whether you can create overlapping shifts without selecting a template.|Orlando|
|On-Call: Create overlapping shifts when allow shift overlap is set to No|Verify whether you can create overlapping shifts when **Allow overlap** is set to **No**.|Orlando|
|On-Call: Request time-off when PTO approval preferences is with approval|Verify whether you can request a time-off when PTO approval preference is **With approval**.|Orlando|
|On-Call: Assign shift managers for maintaining on-call schedules.|Verify whether shift managers can maintain on-call schedules.|Orlando|
|On-Call: Search on-call schedules by user name|Verify whether you can search for on-call schedules by user name.|Orlando|
|On-Call: Search on-call schedules by group name or schedule name|Verify whether you can search for on-call schedules by group name or schedule.|Orlando|
|On-Call: Roster details for overlapping shifts with the escalation rule 'Escalate to incoming shift'|Verify the roster details for overlapping shifts when the escalation rule is set to **Escalate to incoming shifts**.|Orlando|
|On-Call: Calendar preview with timezone options|Verify whether the calendar preview is available with the timezone options.|Orlando|
|On-Call: Create overlapping shifts by selecting a template|Verify whether you can create overlapping shifts by selecting a template.|Orlando|
|On-Call: Show active shifts| |Orlando|
|On-Call: Make shift draft/publish form shift form|Verify whether you can publish/unpublish a shift and alternate between making the rota **Draft** and **Publish** state from the form.|Orlando|
|On-Call: Roster Details for overlapping shifts with the escalation rule 'Escalate to outgoing shift'|Verify the roster details for overlapping shifts when the escalation rule is set to **Escalate to outgoing shifts**.|Orlando|
|On-Call: Roster Details for overlapping shifts with the escalation rule 'Escalate to all shifts'|Verify the roster details for overlapping shifts when the escalation rule is set to **Escalate to all shifts**.|Orlando|
|On-call: Verify On-Call workbench|Test to verify the On-Call workbench layout.|Orlando|
|On-call: Hide or show shifts|Verify whether you can hide or show shifts from On-Call calendar|Orlando|

To learn more about On-Call Scheduling, see [On-Call Scheduling](https://www.servicenow.com/docs/access?context=c_OnCallScheduling&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Metric Intelligence

Metric Intelligence quick start tests require activating the Metric Intelligence plugin \(com.snc.sa.metric\).

<table id="table_usl_4wy_vfb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

OI: Health Metrics Collection

</td><td>

An individual test that verifies the following:

-   There is at least one Metric Intelligence Metrics extension that is running.
-   There are entries for the ‘Health Metrics’ in the Metric to CI table.
-   For each of the Metric Intelligence Metrics extensions that are currently running, that there is data stored in MetricBase.

 If the test initially fails, wait until the Metric Intelligence Metrics extension runs for at least 10-15 minutes. Then try again.

</td><td>

Madrid

</td></tr></tbody>
</table>To learn more about Metric Intelligence, see [Metric Intelligence](https://www.servicenow.com/docs/access?context=operational-metrics&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

## Predictive Intelligence

Predictive Intelligence quick start tests require activating the Predictive Intelligence \[com.glide.platform\_ml\] plugin. In order to execute critical upgrade tests on existing machine learning solutions, you need to create a basic authorization profile named ml\_atfin the Basic Auth Configurations table \(sys\_auth\_profile\_basic.list\). To run the tests successfully, the user attached to the ml\_atf authorization profile must have the ml\_admin role.

|Test|Description|Release version|
|----|-----------|---------------|
|PI: Presence of ML model artifacts persisted in glide|Verify all the trained ML model artifacts are persisted in glide \(sys\_attachments table\) after model training/instance cloning so that ML prediction calls are successful.|New York|
|PI: Valid setup of ML user \(sharedservice.worker\) in glide|Validate if the ML user in glide \(sharedservice.worker\) is active and not logged out so that model training is successful.|New York|
|PI: Glide upgrade test for Classification solution|Validate that the classification model prediction on existing active models is producing the same class membership and confidence value results after a glide upgrade.|New York|
|PI: Glide upgrade test for Similarity solution|Validate that the similarity model prediction API calls on active models are successful after a glide upgrade.|New York|

## Problem Management

Problem Management quick start tests require activating the Problem Management Best Practice — Madrid plugin \(com.snc.best\_practice.problem.madrid\) and the Problem Management — ATF Tests plugin \(com.snc.problem.atf\). For all state related test, the Problem Management State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin needs to be active.

<table id="table_bjf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

PRB MGMT: Cancel a Problem when the state of the Problem is Assess

</td><td>

Verify that when a Problem in the **Assess** state is canceled, the state of the Problem changes to **Closed** with **Resolution code** as **Canceled**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Cancel a Problem when the state of the Problem is Root Cause Analysis

</td><td>

Verify that when a Problem is in the **Root Cause Analysis** state and is canceled, the state of the Problem changes to **Closed** with **Resolution code** as **Canceled**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Mark a Problem as Duplicate when the state of the Problem is Assess

</td><td>

Verify that when a Problem is in the **Assess** state and is marked as duplicate, the state of the Problem changes to **Closed** with **Resolution code** as **Duplicate**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Mark a Problem as Duplicate when the state of the Problem is Root Cause analysis

</td><td>

Verify that when a Problem is in the **Root Cause Analysis** state and is marked as duplicate, the state of the Problem changes to **Closed** with **Resolution code** as **Duplicate**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem \(problem.acceptrisk.move\_to\_closed:false,state:Fix in Progress\)

</td><td>

Verify that when a Problem state is **Fix in Progress** and the risk is accepted, then the Problem state changes to **Resolved** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is false.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem \(problem.acceptrisk.move\_to\_closed:true,state:Fix in Progress\)

</td><td>

Verify that when a Problem state is **Fix in Progress** and the risk is accepted, then the Problem state changes to **Closed** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is true.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem \(problem.acceptrisk.move\_to\_closed:false,state:Root Cause Analysis\)

</td><td>

Verify that when a Problem state is **Root Cause Analysis** and the risk is accepted, then the Problem state changes to **Resolved** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is false.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Accept Risk of Problem\(problem.acceptrisk.move\_to\_closed:true,state:Root Cause Analysis\)

</td><td>

Verify that when a Problem state is **Root Cause Analysis** and the risk is accepted, then the Problem state changes to **Closed** with **Resolution code** as **Risk Accepted**. **Note:** The test is valid when Problem property **Accept Risk moves the Problem to Closed state instead of Resolved state** **\(problem.acceptrisk.move\_to\_closed\)** is true.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze Problem which is closed-Risk Accepted from state Root Cause Analysis

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Risk Accepted**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Create Emergency Change from Problem

</td><td>

Verify the creation of Emergency Change from a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Create Normal Change from Problem

</td><td>

Verify the creation of Normal Change from a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Problem State Management

</td><td>

Verify problem state management.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze a Problem from Complete

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Fix Applied**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze a Problem which is canceled from state Assess

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Canceled**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze a Problem which is canceled from state Root Cause Analysis

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Canceled**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Reanalyze Problem which is closed-Risk Accepted from state Fix in progress

</td><td>

Verify that when a Problem is reanalyzed after it is **Closed** with the **Resolution code** as **Risk Accepted**, Problem state changes to **Root Cause Analysis**.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Create a Known Error article from Problem

</td><td>

Verify creation of Known Error article from a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Risk Accept reason on Incident

</td><td>

Verify the **Risk Accepted reason** is copied to the Incidents which are awaiting resolution of a Problem.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Communicate Fix

</td><td>

Verify the communicate fix functionality.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Communicate Workaround

</td><td>

Verify the communicate workaround functionality.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Fix information on Incident

</td><td>

Verify that when a Problem is resolved, the state of the Incidents that are awaiting resolution of the Problem changes to **Resolved**. The fix notes of the Problem are copied to the Incidents.

</td><td>

Madrid

</td></tr><tr><td>

PRB MGMT: Problem task \(Type:General\) state management

</td><td>

Verify Problem task state management of a general type Problem.

</td><td>

Madrid

</td></tr></tbody>
</table>To learn more about Problem Management, see [Problem Management](https://www.servicenow.com/docs/access?context=c_ProblemManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Project Portfolio Management

Project Portfolio Management quick start tests require activating the PPM Standard - ATF Tests plugin \(com.snc.financial\_planning\_pmo.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|PMO: Verify cost plan roll up to project/demand and program|Validate the total planned cost rollup from project and demand to program.|Madrid|
|PMO: Verify cost plan roll up to project/demand, program and portfolio|Validate the total planned cost rollup from project and demand to portfolio.|Madrid|
|PMO: Verify financials of Project created from Demand - Simple Financials|Validate the financial tab fields of a project created from a demand.|Madrid|
|PMO: Verify financials of Project created from Demand - With budget, cost plans, benefit plans|Validate the budget, cost plan, and benefit plan of a project created from a demand.|Madrid|
|PMO: Verify ETC/EAC at cost plan breakdown and project level|Validate the EAC and ETC values at cost plan breakdown and project level.|Tokyo|

|Test|Description|Release version|
|----|-----------|---------------|
|Validate state changes of Idea|Validate that the state of idea is changed when an idea is accepted, rejected, or any other task is created from an idea.|San Diego|

<table id="table_yct_vng_sjb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Validate PPM Cycle from Ideation to demand to project closure

</td><td>

Validate the flow of creating an idea, converting the idea to a demand, and then converting the demand to a project.**Note:** This test fails if the PPM Standard Multicurrency \(com.snc.ppm\_multicurrency\) plugin is active.

</td><td>

Madrid

</td></tr><tr><td>

Validation of State and Date Rollup for Automatic Project

</td><td>

Validate the date and state rollup from tasks for a project of type Automatic.

</td><td>

Madrid

</td></tr><tr><td>

Validation of State and Date rollup for Manual Project

</td><td>

Validate the date and state rollup from tasks for a project of type Manual.

</td><td>

Madrid

</td></tr><tr><td>

Validation of project percent complete when all tasks are Closed Incomplete

</td><td>

Validate the project percent complete when all the tasks are closed as Closed Incomplete.

</td><td>

Orlando

</td></tr><tr><td>

Validate Project is not 100 percent complete if it has atleast one task as closed incomplete

</td><td>

Validate the project percent complete is not 100% when at least one of the tasks is closed as Closed Incomplete or Closed Skipped with task % complete less than 100%.

</td><td>

Orlando

</td></tr><tr><td>

Validate waterfall project does not show Agile Planning Board

</td><td>

Validate that the waterfall projects cannot use the following: -   Add stories or epics
-   Add agile phase
-   Access Agile board from the project

</td><td>

Orlando

</td></tr><tr><td>

Validate dates are rolled up from existing projects to program

</td><td>

Validate that the start and end dates of the project are rolled up to the program to which the project belongs.

</td><td>

Paris

</td></tr><tr><td>

Validate dates are rolled up from new projects to program

</td><td>

Validate that the start and end dates of a new project are rolled up to the program to which the project belongs.

</td><td>

Paris

</td></tr><tr><td>

Add projects and demands with risks or issues to program

</td><td>

Validate that the projects and demands with risks or issue records associated with them are added to the program.

</td><td>

Paris

</td></tr><tr><td>

Add projects and demands with benefit plans to program

</td><td>

Validate that the projects and demands with benefit plans associated with them are added to the program.

</td><td>

Paris

</td></tr><tr><td>

Add projects and demands with cost plans to program

</td><td>

Validate that the projects and demands with cost plans associated with them are added to the program.

</td><td>

Paris

</td></tr><tr><td>

Validate program dates on addition of existing demands

</td><td>

Validate that the start and end date of the program are adjusted on addition of an existing demand.

</td><td>

Paris

</td></tr><tr><td>

Validate program dates on addition of new demands

</td><td>

Validate that the start and end date of the program are adjusted on addition of a new demand.

</td><td>

Paris

</td></tr><tr><td>

Validate program state rollup

</td><td>

Validate that the program state is rolled up from state of all the projects in the program.

</td><td>

Paris

</td></tr><tr><td>

Verify Demand task due date column field value empty

</td><td>

Validate that the **Due date** field is empty for a new demand task.

</td><td>

Rome

</td></tr><tr><td>

Verify baseline is created on Project &amp; Demand when demand is converted to project

</td><td>

Validate that a project and demand baseline is created when a demand is converted to a project.

</td><td>

Rome

</td></tr><tr><td>

Verify timecard financial appears on Demand when time card submitted against demand task

</td><td>

Validate that the actual cost of the demand is updated when a time card is processed for a demand task.

</td><td>

Rome

</td></tr><tr><td>

Validate demand approved date

</td><td>

Validate that the approved dates for demand and the project created from the demand are the same.

</td><td>

Tokyo

</td></tr><tr><td>

Validate project preference "close project milestone tasks when they change to work state"

</td><td>

Validate that the milestone tasks are closed when their state is changed to Work in Progress after setting the project preference to "close project milestone tasks when they change to work state".

</td><td>

Tokyo

</td></tr><tr><td>

Validate project preference "Enable move project for WIP projects"

</td><td>

Validate that the project start date is changed appropriately for a project in WIP state when the project start date is changed after setting the project preference to "Enable move project for WIP projects".

</td><td>

Tokyo

</td></tr><tr><td>

Validate project preference "Rollup project start date from tasks"

</td><td>

Validate that the start date of a project task does not roll up to the project when the project planned dates are different than the project task start date after deselecting the project preference "Rollup project start date from tasks".

</td><td>

Tokyo

</td></tr></tbody>
</table><table id="table_jgn_tvz_2dc"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Validate Planned start date of a project can be shifted by using the Move project action

</td><td>

Validate that the Planned start date of a project in Planning or Open state can be updated to a later or earlier date than the current planned start date using the Move project related link.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project is disabled when Project is selected for execution

</td><td>

Validate that the Move Project option is not available if the Project is in Execution phase.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project functionality with sprint dates populated for an agile phase

</td><td>

Validate that the sprint start and end dates are cleared when the project is moved using the Move Project related link.**Note:** This test is available only when Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) is activated.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project functionality with external dependencies and related entities

</td><td>

Validate that the external dependencies and related entities are also shifted and redrawn when the project is moved using the Move Project related link.

</td><td>

Orlando

</td></tr><tr><td>

Validate Move Project functionality with different project states

</td><td>

Validate that the Move Project does not work when the project is in Work In Progress or Closed Complete state.

</td><td>

Orlando

</td></tr></tbody>
</table>|Test|Description|Release version|
|----|-----------|---------------|
|Verify RIDAC flow for Risk|Validate the RIDAC flow for a risk associated with a project.|Quebec|
|Verify RIDAC flow for Issue|Validate the RIDAC flow for an issue associated with a project.|Quebec|
|Verify RIDAC flow for Decision|Validate the RIDAC flow for a decision associated with a project.|Quebec|
|Verify RIDAC flow for Action|Validate the RIDAC flow for an action associated with a project.|Quebec|
|Verify changes in fields of risk form|Validate that any change is the Risk form fields such as Risk rank, Risk value, and Probability is updated successfully upon submission.|Quebec|

|Test|Description|Release version|
|----|-----------|---------------|
|Verify RIDAC flow for Risk|Validate the RIDAC flow for a risk associated with a demand.|Quebec|
|Verify RIDAC flow for Issue|Validate the RIDAC flow for an issue associated with a demand.|Quebec|
|Verify RIDAC flow for Decision|Validate the RIDAC flow for a decision associated with a demand.|Quebec|
|Verify RIDAC flow for Action|Validate the RIDAC flow for an action associated with a demand.|Quebec|
|Verify changes in fields of risk form|Validate that any change is the Risk form fields such as Risk rank, Risk value, and Probability is updated successfully upon submission.|Quebec|

<table id="table_bdt_vng_sjb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Verify user resource plan flow from Planned to Canceled state

</td><td>

Validate that the resource plan of a project can be moved to canceled state from planned state.

</td><td>

Madrid

</td></tr><tr><td>

Verify group resource plan flow from Planned to Complete state

</td><td>

Validate that the resource plan of a project can be moved to complete state from planned state.

</td><td>

Madrid

</td></tr><tr><td>

Verify role resource plan flow from Planned to Allocated state

</td><td>

Validate that the resource plan of a project can be moved to allocated state from planned state.

</td><td>

Madrid

</td></tr><tr><td>

Verify aggregated cost of all resource plans roll up to the corresponding project or demand fields

</td><td>

Validate that the aggregated cost of all resource plans on a project or demand roll up to the Planned Cost and Allocated Cost fields and the Resource Cost section of respective projects and demands.

</td><td>

Orlando

</td></tr><tr><td>

Verify Copy Resource plan option

</td><td>

Validate that the Copy Resource plan option creates an exact copy of the source resource plan in the Planning state

</td><td>

Orlando

</td></tr><tr><td>

Verify resource plan aggregate roll up from project/demand to program

</td><td>

Validate that the aggregated cost of all resource plans on a project or demand roll up to the total planned cost of the associated program.

</td><td>

Orlando

</td></tr><tr><td>

Verify records on completion of a resource plan

</td><td>

Validate the changes in a resource plan on completion:-   The state of the resource plan is updated to Completed.
-   If the completion date is earlier than the resource plan end date, the end date of the resource plan is updated with the completion date. If the completion date entered is later than the resource plan end date, the resource plan end date is retained.
-   All the requested and allocation records for the resource plan for the period after the completion date are deleted. If there are any actual hours logged against an allocation, that allocation is not deleted. For those allocation records, the allocated hours become zero and the actual hours are retained.
-   The available and allocated hours for resources are updated in the aggregate tables.

</td><td>

Orlando

</td></tr><tr><td>

Verify records on completion of a resource plan with Planned Duration as allocation type

</td><td>

Validate the following on completion of a resource plan with Planned Duration as allocation type:-   The state of the resource plan is updated to Completed.
-   Allocations are not deleted.
-   End date of the allocation is updated to the completion date.

</td><td>

Orlando

</td></tr><tr><td>

Verify the RP replan Capability

</td><td>

Validate that when a cancelled resource plan is re-planned, the state of the resource plan changes to Planning.

</td><td>

Orlando

</td></tr><tr><td>

Verify whether change in resource plan is reflected in corresponding cost plan

</td><td>

Validate that when a resource plan is updated, the corresponding cost plan is updated accordingly. For example, if the total planned cost is 500 USD, and the planned hours is 10, and you change the planned hours to 20, the total planned cost is updated to 1000 USD.

</td><td>

Paris

</td></tr><tr><td>

Resource-Test the default population of resource plan start &amp; end date

</td><td>

Validate the following on creating a user or group resource plan from the related list of a demand:-   If a demand is created without a start date and end date, the user or group resource plan has task as demand and no start and end date.
-   If a demand is created with a start date and end date, the user resource plan has task as demand and the start date and end date as added for the demand.

</td><td>

Paris

</td></tr><tr><td>

Validate that actual hours in operational resource plan and time card are equal

</td><td>

Validate that when a time card category is mapped with an operational work type, on submitting the time card for the operational resource plan associated with that work type, the actual hours in the resource plan and the time card are equal.

</td><td>

Quebec

</td></tr><tr><td>

Verify Resource plan auto population for Operational plans

</td><td>

Validate that the operational resource plans associated with a time card are automatically retrieved on the time card when time is logged.

</td><td>

Rome

</td></tr><tr><td>

Verify resource plan auto population for non-operational resource plans

</td><td>

Validate that the resource plans associated with a project, project task, or demand for a time card are automatically retrieved on the time card when time is logged.

</td><td>

Rome

</td></tr></tbody>
</table>To learn more about Project Portfolio Management, see [Project Portfolio Management](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuite&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Project Currency test suite

Project currency quick start tests require activating the PPM Standard Multicurrency – ATF Tests plugin \(com.snc.ppm\_multicurrency.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|Verify cost in project currency on cost plan|Validate the calculation of cost line breakdown with budget reference rate and verify roll up to cost plan and also for the project in project currency.|Orlando|
|Verify benefit in project currency on benefit plan|Validate the calculation of benefit line breakdown with budget reference rate and verify roll up to benefit plan and also for the project in project currency.|Orlando|

To learn more about PPM Standard, see [PPM Standard](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuiteWithFinancials&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Reporting

The Reporting quick start test Automated Test Framework - Reporting plugin \(com.glide.automated\_testing\_impl.report\) is active by default or instance reboot.

**Note:** Reporting quick start tests do not test report access from dashboards. To test dashboards, see [Quick start tests for Dashboards](https://www.servicenow.com/docs/access?context=quick-start-tests-dashboards&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

|Test|Description|Release version|
|----|-----------|---------------|
|Report Visibility|Confirm whether reports are still visible to users whom they are shared with.|Madrid|

## Software Asset Management Foundation plugin Software Asset Management

Software Asset Management Foundation plugin Software Asset Management quick start tests require activating the Software Asset Management Professional plugin \(com.snc.samp\). Some quick start tests require activating the following additional plugins.

-   Software Asset Management - Spend Detection \(com.sn\_sam\_spend\)
-   Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\)
-   Software Asset Management Professional for SAP \(com.sn\_samp\_sap\)
-   Software Asset Management Professional for Oracle \(com.snc.samp.oracle\)
-   Software Asset Management - SaaS License Management Integrations \(sn\_sam\_saas\_int\)

<table id="atf-tests-sam"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

SAM - Mapping Custom PPN/DMAP to newly published PPN and Content

</td><td>

Validates the replacement of a custom publisher part number \(PPN\) with a new Software Asset Management Content Service PPN.

</td><td>

San Diego

</td></tr><tr><td>

SAM - Oracle PaaS BYOL

</td><td>

-   Validates the addition of the new Serverless Hardware \[cmdb\_ci\_serverless\_hardware\] table, which stores information about PaaS devices.
-   Validates the license compliance of Oracle Database servers in Amazon Web Services \(AWS\) PaaS environments.

 **Note:** Requires the Software Asset Management Professional for Oracle \(com.snc.samp.oracle\) plugin and the CMDB CI Class Models store application.

</td><td>

Rome

</td></tr><tr><td>

SAM - Software Product Lifecycles records on Software Model

</td><td>

Validates that the Software Lifecycle tab on the Software Model form is showing records.**Note:** Requires demo data and the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Quebec

</td></tr><tr><td>

SAM - BYOL

</td><td>

-   Validates the purchase date on the Software Entitlement form
-   Validates the addition of newly added column legacy\_license on the License Metric Results \[samp\_license\_metric\_result\] and License Position Report \[samp\_license\_position\_report\] tables
-   Validates the addition of newly added columns, cloud\_license\_type and cloud\_license \_type\_source in the Software Installations \[cmdb\_sam\_sw\_install\] table

**Note:** Requires the Software Asset Management Professional for Micorosft \(com.snc.samp.microsoft\) plugin.

</td><td>

Quebec

</td></tr><tr><td>

SAM - Validate CIS Suites

</td><td>

Validates reconciliation of Core Infrastructure Server \(CIS\) suites along with downgrade rights.**Note:** Requires demo data and the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - PerCoreForMSCluster

</td><td>

Verifies the reconciliation functionality for Microsoft per core with cluster.**Note:** Requires the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Validate upgrade/downgrade during Reconciliation for Microsoft publisher

</td><td>

Validates upgrade and downgrade rights during reconciliation for Microsoft products.**Note:** Requires demo data and the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Generate demand to consolidate SaaS applications

</td><td>

Validates generation and submission of a demand on SaaS applications.**Note:** Requires the Software Asset Management - Spend Detection \(com.sn\_sam\_spend\) plugin and the PPM standard \(com.snc.financial\_planning\_pmo\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Software Model and Software Entitlement checks for SAP Engines

</td><td>

Verifies that the Software Model and Software Entitlement forms change when the product is an SAP engine.**Note:** Requires the Software Asset Management Professional for SAP \(com.sn\_samp\_sap\) plugin.

</td><td>

Paris

</td></tr><tr><td>

SAM - Downgrade Rights on Software Model

</td><td>

Validates that the downgrade rights pushed from the content service are correctly populated on the Downgrade Rights related list on the software model form.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Multi-core pack validation on Software Entitlement

</td><td>

Validates the functionality of new fields for a multi-core pack on software entitlements.**Note:** Requires the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Downgrade Rights on Software Entitlement

</td><td>

Validates that the downgrade rights pushed from the content service are correctly populated on the Downgrade Rights related list on the software entitlement form.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Software Spend Transaction

</td><td>

Validates the creation of a Software Spend Transaction.**Note:** Requires the Software Asset Management - Spend Detection \(com.sn\_sam\_spend\) plugin.

</td><td>

Orlando

</td></tr><tr><td>

SAM - Software Model and Software Entitlement

</td><td>

Tests that a user can create a software model and software entitlement and validates those records.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Installation and Discovery Model

</td><td>

Tests that a user can create a software installation and discovery model and validates those records.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Entitlement Creation Using Custom PPN

</td><td>

Creates a custom software product, a custom DMAP for the custom product, a custom Part Number for the custom DMAP, a software entitlement using the custom Part Number, and verifies that a software model is automatically created.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Model Checks for SAP Named Users

</td><td>

Tests that the software model form changes when the publisher is SAP and the product is Named Users.**Note:** Requires the Software Asset Management Professional for SAP \(com.sn\_samp\_sap\) plugin.

</td><td>

New York

</td></tr><tr><td>

SAM - Software Model Checks for SaaS

</td><td>

Tests that the Software Model form changes when a SaaS product is selected.**Note:** Requires the Software Asset Management - SaaS License Management Integrations \(sn\_sam\_saas\_int\) plugin.

</td><td>

New York

</td></tr><tr><td>

SAM - Validate Fields on SaaS Software Products

</td><td>

Tests that the **Subscription software** and **Ignore installs** fields are present on the Software Product form.**Note:** Requires the Software Asset Management - SaaS License Management Integrations \(sn\_sam\_saas\_int\) plugin.

</td><td>

New York

</td></tr></tbody>
</table>To learn more about Software Asset Management, see [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

## Security Incident Response

Security Incident Response quick start tests require activating Security Incident Response plugin \(com.snc.security\_incident\) and loading the demo data.

<table id="table_fkf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

SIR: Create Security Incident

</td><td>

Determine whether a user can successfully create a security incident from the security incident form.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: Create Security Incident via Security Incident Catalog

</td><td>

Determine whether a user can successfully create a security incident from the catalog.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: Security Incident life cycle

</td><td>

Validate the response tasks of the Policy Violation workflow.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: Threat Lookup

</td><td>

Validates the Threat Lookup capability.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: PIR Assessments OOTB configuration

</td><td>

Use this test to validate PIR assessments and base system configurations.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: PIR Assessments conditional configuration

</td><td>

Verify that security incidents matching the mandatory conditional rule are not closed without completing the post incident assessment.

 Verify that the security incidents matching the optional conditional rule can be closed without completing the post incident assessment.

 Verify that assessments are not generated for the security incidents that do not match any rule.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: PIR run time verification

</td><td>

Verify that PIR reports are configured and attached to the security incidents as per the new design.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: PIR design time setup verification

</td><td>

Verify that the security incident is mapped with the report template based on the administrator configuration.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: Link Security Incident to a existing Major Security Incident

</td><td>

Link a Security Incident to an existing Major Security Incident and validate data from Security Incident rolled up to Major Security Incident.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: Promote Security Incident as Major Security Incident

</td><td>

Promote a Security Incident as Major Security Incident and validate data from Security Incident rolled up to Major Security Incident.

</td><td>

Xanadu

</td></tr><tr><td>

SIR: Propose Security Incident as Major Security Incident

</td><td>

Propose a Security Incident as Major Security Incident and validate data from Security Incident rolled up to Major Security Incident.

</td><td>

Xanadu

</td></tr><tr><td>

Verify that only Allowed Members can access the security incident once Enforce Restriction is ON

</td><td>

Verify that only the allowed members can access the security incident once the Enforce Restriction is enabled.

</td><td>

Xanadu

</td></tr><tr><td>

Verify that only Allowed Groups can access the security incident once Enforce Restriction is ON

</td><td>

Verify that only the allowed groups can access the security incident once the Enforce Restriction is enabled.

</td><td>

Xanadu

</td></tr><tr><td>

Validate Read Access

</td><td>

Validate the view access.

</td><td>

Xanadu

</td></tr><tr><td>

Validate Write Access

</td><td>

Validate the edit access.

</td><td>

Xanadu

</td></tr></tbody>
</table>To learn more about Security Incident Response, see [Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).

## Service Level Management

Service Level Management quick start tests require activating the Service Level Management - ATF Tests plugin \(com.snc.service\_level\_management.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|SLM: Service Level Management Task SLA completed workflow|Tests that a user can create a task SLA and complete the workflow.|Orlando|
|SLM: Service Level Management Task SLA cancelled workflow|Tests that a user can create a task SLA and cancel the workflow.|Orlando|
|SLM: Service Level Management Task SLA timer REST API|Tests that the SLA Timer API response matches data expected by SLA Timer Seismic component.|Paris|

To learn more about Service Level Management, see [Service Level Management](https://www.servicenow.com/docs/access?context=service-level-mgmt-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Service Mapping

Service Mapping quick start tests require activating the Service Mapping \(com.snc.service-mapping\) plugin and loading the demo data.

<table id="table_lkf_nfg_h1c"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

SM OOTB: Tests SM application visibility by roles

</td><td>

Validate the visibility of Service Mapping applications and modules for different roles. For example, the test verifies that a user logged in with the service\_mapping\_user role cannot access the Administration module under Service Mapping.

</td><td>

Madrid

</td></tr><tr><td>

SM OOTB: Service map verification

</td><td>

Use this test template to create custom tests for verifying that the topology of the most significant services is unchanged.

 Configure values under Test Run Data Sets, to identify the name of the service to test and the nodes that you expect to find in this service.

 For the node name values, enter the node attribute exactly as it appears on the map, for example, "Apache server." If the attribute name for a node is truncated or shows that a node is a CI cluster, configure this node name value to reflect the way it appears on the map, for example, "11x ExchangeF" for a group of 11 Exchange FrontEnd servers.

**Note:** You cannot use this test to verify the service content beyond the top, unexpanded level.

</td><td>

Orlando, updated Paris

</td></tr><tr><td>

SM OOTB: Check UI accessibility after an upgrade

</td><td>

Run this test to check that the Service Mapping UI is fully functional after an upgrade.

</td><td>

Orlando

</td></tr></tbody>
</table>To learn more about Service Mapping, see [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

## Service Portfolio Management Premium

Service Portfolio Management Premium quick start tests require activating the Service Portfolio Management Premium plugin \(com.snc.spm\).

<table id="table_l12_tvt_rjb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

Portfolio Editor: Not Portfolio Owner, Read Only Taxonomy Access

</td><td>

Ensure a portfolio editor can only read associated non-owned portfolio taxonomies.

</td><td>

Orlando

</td></tr><tr><td>

Portfolio Editor: Cannot create new Portfolios

</td><td>

Ensure a portfolio editor cannot create new portfolios.

</td><td>

Orlando

</td></tr><tr><td>

Portfolio Editor: Valid Portfolio Owner Taxonomy Access

</td><td>

Ensure a portfolio owner has access to taxonomies within owned portfolios.

</td><td>

Orlando

</td></tr><tr><td>

Service Editor: Access

</td><td>

Ensure a service editor can only edit owned services and offerings.

</td><td>

Orlando

</td></tr><tr><td>

Portfolio Editor: Can Modify Owned Portfolios

</td><td>

Ensure a portfolio editor can modify and update owned portfolios.

</td><td>

Orlando

</td></tr><tr><td>

Create a Portfolio

</td><td>

Ensure a portfolio admin can create a new portfolio.

</td><td>

Orlando

</td></tr><tr><td>

Portfolio Editor: Cannot Modify Non-Owned Portfolios

</td><td>

Ensure a portfolio editor cannot modify non-owned portfolios.

</td><td>

Orlando

</td></tr><tr><td>

Service Workflow

</td><td>

Verify that a service cannot move forward to Catalog phase without a service portfolio, taxonomy node, and service offering attached to it.

 Verify a service cannot move backward from the Catalog phase to the Pipeline phase.

</td><td>

Orlando

</td></tr><tr><td>

Service Portfolio \(Normal\)

</td><td>

Create a service portfolio, taxonomy layer, and taxonomy nodes.

</td><td>

Orlando

</td></tr><tr><td>

Create a Portfolio + 3 Taxonomy Layers

</td><td>

Create a service portfolio with three taxonomy layers.

</td><td>

Orlando

</td></tr><tr><td>

Service Portfolio \(Exception\) - Taxonomy Layer Definition Set 01

</td><td>

Create a service portfolio, taxonomy layer, and taxonomy nodes.

</td><td>

Orlando

</td></tr><tr><td>

SPM: Create a Portfolio

</td><td>

Create a service portfolio.

</td><td>

Paris

</td></tr><tr><td>

SPM: Create a Portfolio + 3 Taxonomy Layers

</td><td>

Create a service portfolio, with three taxonomy layers.

</td><td>

Paris

</td></tr><tr><td>

SPM: Service Portfolio \(Normal\)

</td><td>

Create a service portfolio, taxonomy layer, and taxonomy nodes.

</td><td>

Paris

</td></tr><tr><td>

SPM: Service Portfolio \(Exception\) - Taxonomy Layer Definition Set 01

</td><td>

Create a service portfolio, taxonomy layer, and taxonomy nodes.

</td><td>

Paris

</td></tr><tr><td>

SPM: Portfolio Editor: Can Modify Owned Portfolios

</td><td>

Ensure a portfolio editor can modify portfolios that they own.

</td><td>

Paris

</td></tr><tr><td>

SPM: Portfolio Editor: Cannot Modify Non-Owned Portfolios

</td><td>

Ensure a portfolio editor cannot modify portfolios that they do not own.

</td><td>

Paris

</td></tr><tr><td>

SPM: Portfolio Editor: Cannot create new Portfolios

</td><td>

Ensure a portfolio editor cannot create new Portfolios.

</td><td>

Paris

</td></tr><tr><td>

SPM: Portfolio Editor: Valid Portfolio Owner Taxonomy Access

</td><td>

Ensure portfolio owners have access to taxonomies that they own.

</td><td>

Paris

</td></tr><tr><td>

SPM: Portfolio Editor: Not Portfolio Owner, Read Only Taxonomy Access

</td><td>

Ensure a portfolio editor can only read the taxonomies of portfolios they do not own.

</td><td>

Paris

</td></tr><tr><td>

SPM: Service Editor: Access

</td><td>

Ensure a service editor can only edit services and offerings that they own or are a delegate of.

</td><td>

Paris

</td></tr><tr><td>

SPM: Service Viewer: Access

</td><td>

Ensure a service viewer has access to view services.

</td><td>

Paris

</td></tr><tr><td>

SPM: Service Workflow

</td><td>

Verify a service cannot move forward to Catalog phase without a service portfolio, taxonomy node, and service offering attached to it.

 Verify a service cannot move backward from Catalog to Pipeline phase.

</td><td>

Paris

</td></tr></tbody>
</table>To learn more about Service Portfolio Management Premium, see [Service Portfolio Management Premium](https://www.servicenow.com/docs/access?context=SPM2-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Skills Management

Skills Management quick start tests require activating the Skills Management plugin \(com.snc.skills\_management\).

|Test|Description|Release version|
|----|-----------|---------------|
|Skills MGMT: User skill level inheritance when user is part of multiple groups|Verify that the user is assigned the highest skill level when the user belongs to multiple groups that have been assigned the same skills with different skill levels.|New York|
|Skills MGMT: Add skills to lowest level category|Verify that skills can be added to the lowest level category.|New York|
|Skills MGMT: Create a child category under a parent category|Verify that a lower-level category can be created when the flag for **Add skills** is unchecked in the parent category.|New York|
|Skills MGMT: Create a skill category|Verify that a skill category can be created on the skill category form.|New York|
|Skills MGMT: Create skill level type and skill levels|Define the skill level type and different skill levels for the type.|New York|
|Skill MGMT: Skill level inheritance from group to user|Verify that skill levels can be inherited from a group to the users of the group and that the **Inherited** and **Skill level inherited** fields are set to true.|New York|
|Skills MGMT: Create a skill from Manage IT Skills user interface.|Verify that you can create a skill from the Manage IT Skills user interface.|Orlando|
|Skills MGMT: Add skills and skill levels to users in the Manage IT Skills user interface.|Verify that you can add skills and associated skill levels to users in the Manage IT Skills user interface.|Orlando|
|Skills MGMT: Select a skill and add users to the skill in the Manage IT Skills user interface.|Verify that you can select a skill and add the skill and associated skill levels to one or more users in the Manage IT Skills user interface.|Orlando|
|Skills MGMT: Select a skill that does not have a skill level and add users to that skill in the Manage IT Skills user interface.|Verify that you can select a skill that does not have a skill level and add the skill to one or more users in the Manage IT skills user interface.|Orlando|

To learn more about Skills Management, see [Skills Management](https://www.servicenow.com/docs/access?context=skills-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Test Management 2.0

Test Management 2.0 quick start tests require activating the Test Management 2.0 plugin \(com.snc.test\_management.2.0\). and the Test Management 2.0 - ATF Tests plugin \(com.snc.test\_management.2.0.atf\).

|Test|Description|Release version|
|----|-----------|---------------|
|Create test version should create test|Validate test creation and version.|Madrid|
|Should be able to mark test version as ready when it contains verification steps|Validate test state when test has verification steps.|Madrid|
|Should not able to mark test version as ready when it does not contain verification step|Validate test state when test does not have verification steps.|Madrid|
|Marking a test version as ready should retire other test version in ready state|Validate test state when marking test ready.|Madrid|

|Test|Description|Release version|
|----|-----------|---------------|
|When test run closed, should update execution suite progress|Validate execution state progress.|Madrid|
|Should not be able to assign a test not in ready state|Validate test assignment.|Madrid|
|Test progress should roll up for test plan and test cycle|Validate test progress for test plan and test cycle.|Madrid|

To learn more about Test Management 2.0, see [Test Management 2.0](https://www.servicenow.com/docs/access?context=test-management2-landing-page&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US).

## Universal Request

Universal Request quick start tests require activating the Universal Request \(com.snc.universal\_request\), Universal Request: Integration for Incident management \(com.snc.incident.universal\_request\), and Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugins.

<table id="table_ubx_4ry_nnb"><thead><tr><th>

Test

</th><th>

Description

</th><th>

Release version

</th></tr></thead><tbody><tr><td>

UR: Transferring an HR case to an Incident

</td><td>

Validate if an HR case is transferred to an incident and an incident is created.

</td><td>

Quebec

</td></tr><tr><td>

UR: Restrict or Unrestrict universal request

</td><td>

Validates the following:-   The fields are restricted and hidden when a routing agent restricts a UR.
-   Only agents with **sensitiveinfo\_agent** role are allowed to unrestrict the request.
-   And, after the request is unrestricted all fields are visible.
-   sys-audit log access is available for agents.

</td><td>

Xanadu

</td></tr><tr><td>

UR: Universal Request creation with RITM

</td><td>

Verifies a catalog request for any item from self-service can be created when Universal Request Certified is enabled.

</td><td>

San Diego

</td></tr></tbody>
</table>## Vendor Management Workspace

Vendor Management Workspace quick start tests require activating the Vendor Manager Workspace plugin \(com.snc.vlm.vmw\) and loading demo data.

|Test|Description|Release version|
|----|-----------|---------------|
|VLM: Create a Vendor|Track problems with the Vendor Manager Workspace plugin after upgrade. Create a new vendor.|New York|

To learn more about Vendor Management Workspace, see [Vendor Management Workspace](https://www.servicenow.com/docs/access?context=vendor-management-workspace-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

## Vendor Manager Workspace and Third-party Risk Management

GRC: Vendor Manager Workspace and Third-party Risk Management quick start tests require activating the Vendor Manager Workspace and Third-party Risk Management plugin \(com.sn\_vdr\_risk\_asmt\) and loading demo data.

|Test|Description|
|----|-----------|
|GRC: Create Engagement Risk Assessment|Creates and submits an engagement risk assessment to an engagement.|
|GRC: Vendor Risk Scoring - Cancel assessment for engagement|Verifies a request to recalculate a risk rating is automatically created on an Engagement and Third party after one assessment for the Engagement is cancelled.|
|GRC: Vendor Issue ATF|Creates and submits a third-party risk issue form and third-party risk task form.|
|GRC: Create Vendor Risk Assessment|Creates and submits a vendor risk assessment to a vendor.|
|GRC: Vendor Portal - Answer and Return Assessment|Vendor contact answers and submits assessment in the Service Vendor Portal.|
|GRC: Vendor Tiering Assessment|Selects and submits an assessment to respective assessors after changing the duration.|

Verify that TPRM still works after you make configuration changes such as applying an upgrade or developing an application. Copy and customize the quick-start tests to pass when using your instance-specific data.

## Vulnerability Response

Vulnerability Response quick start tests require activating the Vulnerability Response application \(sn\_vul\) and loading the demo data.

|Test|Description|Release version|
|----|-----------|---------------|
|VR: Create Remediation Target Rule|Create a Remediation Target Rule.|Madrid|
|VR: Create Vulnerability Group Rule|Create a Vulnerability Group Rule.|Madrid|
|VR: Create Vulnerable Item via Form|Determine whether a user can successfully create a vulnerable item from the Vulnerable Item form.|Madrid|
|VR: Vulnerability Group Life Cycle|Determine whether a user can successfully resolve a vulnerability group.|Madrid|
|VR: Vulnerable Item life cycle|Determine whether a user can successfully move a vulnerable item through its life cycle, and also determine whether a closed vulnerable item can be reopened.|Madrid|
|VR: Rollup Calculator|Determine whether the rollup risk calculator can provide an overall risk score for an entire group of vulnerable items using the scores for all the vulnerable items in a vulnerability group.|New York|
|VR: Vulnerability Response Assignment Rules|Determine whether a sample set of assignment rules can successfully auto-assign vulnerable items to an assignment group for remediation.|New York|
|VR: Vulnerability Calculators|Test the vulnerability calculators.|New York|
|VR: CI Lookup - Qualys|Create a new lookup rule with method "field\_matching" called "Lookup By Network Adapter" for Qualys. Determine whether a configuration item is successfully matched in the Discovered Item table by network adapter and IP address with the new lookup rule.|Orlando|
|VR: Create Normal and Emergency Change Request|Determine whether the user can successfully create normal and emergency change requests from a vulnerability group.|Orlando|
|VR: Split Vulnerability Group|Determine whether the user can successfully split a vulnerability group.|Orlando|
|VR: Update VG state when a CHG is cancelled.|Determine whether the State field on a vulnerability group successfully transitions when a change request that is associated with the vulnerability group is cancelled.|Orlando|
|VR: Update VG state when a CHG transitions to Review.|Determine whether the State field on a vulnerability group successfully transitions when a change request that is associated with it moves to the Review state.|Orlando|
|VR: CI Lookup - Rapid7|Test CI lookup using the existing Rapid7 Vulnerability Integration lookup rule, **IP Address**.|Orlando|
|VR: CI lookup - Qualys|Test CI lookup by creating a new lookup rule for the Qualys Vulnerability Integration|Orlando|
|VR: Exception Approval Workflow for VI|Create an exception request and verify that the approval process is working.|Orlando|
|VR: False Positive Approval Workflow for VI|Create a false positive exception request and verify that the approval process is working.|Orlando|
|VR: Application Vulnerability Response \(AVR\)|Determine whether your rules and calculators are working correctly. Verify that updates are working.|Orlando|
|Remediation target rules: VI import test|Tests VR remediation target rules during import.|Paris|
|VR: Classification Rule|A sample classification rule that automatically classifies a vulnerability.|Tokyo|

To learn more about Vulnerability Response, see [Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US).

## Walk-up Experience

Walk-up Experience quick start tests require activating the Walk-up Experience plugin \(com.snc.walkup\) and loading demo data.

|Test|Description|Release version|
|----|-----------|---------------|
|Create a location|Ensure users with the Walk-up administrator \[sn\_walkup.walkup\_admin\] role can access all existing walk-up queues, create new queue locations, and configure queues appropriately.|Orlando|
|Onsite checkin \(ITIL User\)|Verify that users with the ITIL role can check into an onsite queue location.|Orlando|
|Onsite checkin \(ESS User\)|Verify that users with the ESS role can check into an onsite queue location.|Orlando|
|Onsite checkin \(Guest\)|Verify that guest users can check into an onsite queue location.|Orlando|

To learn more about Walk-up Experience, see [Walk-up Experience](https://www.servicenow.com/docs/access?context=walkup-experience-landing-page&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).


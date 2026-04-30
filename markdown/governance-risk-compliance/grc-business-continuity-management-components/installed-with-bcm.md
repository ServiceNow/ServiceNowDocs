---
title: Components installed with Business Continuity Management
description: Several types of components are installed with activation of the Business Continuity Management application.When you download the Business Continuity Management application, several scripts includes are added to your instance.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Reference, Business Continuity Management, Governance, Risk, and Compliance]
---

# Components installed with Business Continuity Management

Several types of components are installed with activation of the Business Continuity Management application.

## Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th><th>

Available with scope

</th></tr></thead><tbody><tr><td>

BCM administrator\(sn\_bcm.admin\)

</td><td>

Create, read, write, and delete access to all tables including the core data.

 Has create, read, and write access to the phase records.

 **Note:** Starting with Release 9.x.x, BCM administrator \(sn\_bcm.admin\) role is now used for ACLs, replacing the System Administrator role.

</td><td>

-   sn\_bcp.plan\_admin
-   sn\_grc\_workspace.admin
-   sn\_crisis\_ebn.admin
-   sn\_grc\_workspace.task\_admin
-   sn\_data\_registry.admin
-   sn\_grc\_doc\_design.admin
-   sn\_bcm.core\_manager
-   sn\_irm\_shared\_cmn.word\_template\_creator
-   dependency\_views
-   sn\_smart\_asmt.template\_manager: Provides access to create a Smart Assessment template.
-   sn\_bia.bia\_admin
-   sn\_bcm.program\_manager
-   sn\_grc\_appr.admin

**Note:**

The BCM admin contains the Approver Configurator admin role, but it doesn’t contain the Approver Configurator developer role.

For security reasons, the Approver Configurator admin has read access to the **Script** field on the Approval Rule form. If you have the Approver Configurator developer role in the GRC: Approver Configurator application, you’ve create and write access to the **Script** field on the Approval Rule form.

For more information on the roles in the GRC: Approver Configurator application, see [Roles installed with GRC: Approver Configurator](../../grc-common/reference/roles-installed-with-approver-configurator.md).


</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

BCM Program Manager\(sn\_bcm.program\_manager\)

</td><td>

Create, read, write, and delete access to all BCM application tables.

</td><td>

-   sn\_bia.bia\_manager
-   sn\_bcp.plan\_manager
-   sn\_recovery.event\_manager

: Has read access to the phase records.

-   sn\_bcm.core\_viewer
-   workspace\_user
-   service\_viewer
-   sn\_bcp.plan\_contributor
-   sn\_smart\_asmt.actor: Contains a Smart Assessment actor role to give update access to Smart Assessment instance.
-   sn\_smart\_asmt.reassign: Contains the Smart assessment reassign role.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

BCM Planner \(sn\_bcm.planner\)

</td><td>

Create, read, write, and delete access to all BCPs, BIAs, exercises, and crisis events that are created or owned by the planner.**Note:** If you have the BCM planner role and you are not the owner of the exercise, you cannot remove the assets from an exercise or remove a plan from the exercise, but you can add the assets or a plan. Additionally, if you are not the plan owner, you can only add the approved plans in an exercise or crisis event.

</td><td>

-   sn\_smart\_asmt.actor: Contains a Smart Assessment actor role to give update access to Smart Assessment instance.
-   canvas\_user
-   sn\_bia.bia\_planner
-   sn\_bcm.core\_viewer
-   sn\_crisis\_ebn.user
-   service\_viewer
-   sn\_recovery.event\_user

: Has read access to the phase records.

-   sn\_bia.bia\_viewer
-   sn\_smart\_asmt.reassign: Contains the Smart assessment reassign role.
-   workspace\_user
-   sn\_bcp.plan\_contributor

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

BCM Contributor \(sn\_bcm.contributor\)

</td><td>

-   Read access to all BIAs, exercises, and crisis events tables.
-   Read access to BCP tables if the contributor is included in the contributor list.
-   Create and delete existing dependencies when the group is in pending state.
-   Write access to the RTO, RPO, and dependency category state fields, disruptive duration of RTO and RPO editable fields, and dependency assessment editable fields.
-   Update RTO, RPO, and dependency assessment state.
-   Note that the contributor field is not a regular field on the form. You cannot use the asterisk \(\*\) to perform a search on the contributors.

</td><td>

-   sn\_bia.bia\_contributor
-   service\_viewer
-   sn\_smart\_asmt.reassign: Contains the Smart assessment reassign role.
-   sn\_bcm.core\_viewer
-   sn\_smart\_asmt.actor: Contains a Smart assessment actor role to give update access to Smart assessment instance.

 **Note:** To access records where you are added as a contributor, add the BCM Viewer \(sn\_bcm.viewer\) role to the BCM Contributor \(sn\_bcm.contributor\) role.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

BCM Viewer\(sn\_bcm.viewer\)

</td><td>

View all data of the BCM applications.

 Has read access to the phase records.

</td><td>

-   sn\_fam.user
-   canvas\_user
-   service\_viewer
-   sn\_crisis\_ebn.viewer
-   workspace\_user
-   sn\_bcp.plan\_viewer
-   sn\_bia.bia\_viewer
-   sn\_bcm.core\_viewer
-   sn\_recovery.event\_viewer

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

BCM core\_viewer \(sn\_bcm.core\_viewer\)

</td><td>

BCM core viewer role that can read the Smart assessment template.

</td><td>

-   sn\_grc\_workspace.task\_reader
-   sn\_smart\_asmt.assessment\_reader: Contains a Smart assessment reader role to give read access to Smart assessment instance.
-   sn\_smart\_asmt.template\_reader: Contains a Smart assessment template reader role.
-   sn\_data\_registry.reader
-   sn\_grc\_workspace.user
-   sn\_grc\_rel\_config.reader

</td><td>

 

</td></tr><tr><td>

BCM Recovery Team member \(sn\_bcm.recovery\_team\_member\)

</td><td>

View the list of recovery tasks for crisis events and exercises assigned by the BCM Program Manager.

</td><td>

-   sn\_recovery.event\_member
-   sn\_recovery.event\_viewer
-   sn\_bcp.plan\_viewer
-   sn\_bcm.core\_viewer

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

BCP Plan Manager \(sn\_bcp.plan\_manager\)

</td><td>

Create, read, write, and delete access on all the plans.

</td><td>

-   sn\_doc.writer
-   fd\_read\_flows

</td><td>

 

</td></tr><tr><td>

BIA Manager \(sn\_bcp.plan\_manager\)

</td><td>

Create, read, write, and delete access on all the BIAs.

</td><td>

sn\_doc.writer

</td><td>

 

</td></tr><tr><td>

Doc writer \(sn\_doc.writer\)

</td><td>

Read and write permissions to the document templates.

</td><td>

-   sn\_doc.reader
-   doc\_page\_number\_config\_writer
-   doc\_toc\_config\_writer
-   localization\_editor

</td><td>

 

</td></tr><tr><td>

Approval configuration admin \(sn\_grc\_appr.admin\)

</td><td>

Create, read, write, and delete access to all approver configurator setup tables.

</td><td>

**Note:** To approve an approval configuration record in the BCM application, you must have a BCM role. If you add a user with a non- BCM role to the approval process of an approval configuration record, the record may become inaccessible due to being in an inaccessible state.

</td><td>

Business Continuity Management – Approver Configurator

</td></tr><tr><td>

Approver \(sn\_grc\_appr.approver\)

</td><td>

Create, read, write, and delete access to the Approval table.

</td><td>

 

</td><td>

Business Continuity Management – Approver Configurator

</td></tr></tbody>
</table><table id="table_zdr_42f_12c"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Contains roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_recovery.event\_manager

</td><td>

Operator

</td><td>

-   sn\_doc.writer
-   fd\_read\_flows

</td><td>

Allows read, write, create, and delete access to all the recovery events.

</td></tr><tr><td>

sn\_recovery.event\_member

</td><td>

Lite Operator

</td><td>

fd\_read\_flows

</td><td>

Allows read, write, and create access on recovery events.

</td></tr><tr><td>

sn\_recovery.event\_user

</td><td>

Operator

</td><td>

fd\_read\_flows

</td><td>

Allows read, write, and create access on recovery events.

</td></tr><tr><td>

sn\_recovery.event\_viewer

</td><td>

Lite Operator

</td><td>

fd\_read\_flows

</td><td>

Allows read access on all recovery events.

</td></tr></tbody>
</table>## BCM lite operator role

For information on the BCM lite operator role, see [BCM lite operators](../concept/bcm-lite-operators.md).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Installed with scope

</th></tr></thead><tbody><tr><td>

BCM Choice \[sn\_bcm\_choice\]

</td><td>

For the BCM admin to configure choice options in BCM applications.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Documentation Section\[sn\_bcm\_document\]

</td><td>

Stores sections of a document for a plan.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Element Definition\[sn\_bcm\_element\_definition\]

</td><td>

Stores all data for activity definitions.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Element variable \[sn\_bcm\_element\_variable\]

</td><td>

Stores custom columns configured for an element definition.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Grid configuration \[sn\_bcm\_grid\_configuration\]

</td><td>

Stores configuration for a particular grid. For example, the dependency assessment grid. Grid configuration can have multiple grid column configurations.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Grid column configuration \[sn\_bcm\_grid\_column\_configuration\]

</td><td>

Stores data for columns that should be displayed for a grid configuration.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Impact analysis question \[sn\_bcm\_impact\_analysis\_question\]

</td><td>

Stores impact analysis questions for an impact category.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Impact Category\[sn\_bcm\_impact\_category\]

</td><td>

Stores the applicable timeframes and the maximum RTO value of a BIA.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Impact Rating\[sn\_bcm\_impact\_rating\]

</td><td>

Stores the impact ratings for an impact category.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Loss Scenario\[sn\_bcm\_loss\_scenario\]

</td><td>

Stores the elements impacted in a loss scenario.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Recovery Tier\[sn\_bcm\_recovery\_tier\]

</td><td>

Stores recovery timeframes applicable for a recovery tier level.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Recovery Timeframe\[sn\_bcm\_timeframe\]

</td><td>

Stores the time duration at which a recovery timeframe starts.

</td><td>

Business Continuity Management – Core

</td></tr><tr><td>

Recovery Tasks\[sn\_bcp\_recovery\_task\]

</td><td>

Stores the activity tasks of all business continuity and recovery plans.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Related Plan \[sn\_bcp\_plan\_plan\]

</td><td>

Stores related plans for the primary plan in BCP.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Plan Documentation\[sn\_bcp\_document\]

</td><td>

Stores the contents of a documentation section that is a part of a plan template.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Plan\[sn\_bcp\_plan\]

</td><td>

Stores the status of business continuity and recovery plans.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Plan Assets\[sn\_bcp\_plan\_asset\]

</td><td>

Stores the RPO, RTO, RTA, and RTO gap of the plan assets of all plans.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Related Asset Dependency\[sn\_bcp\_plan\_asset\_dependency\]

</td><td>

Stores the assets as configuration items that are dependent on a plan loss scenario.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Plan Loss Scenario\[sn\_bcp\_plan\_loss\_scenario\]

</td><td>

Stores the relationship between a plan and a loss scenario.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Plan Task\[sn\_bcp\_plan\_task\]

</td><td>

Stores the configuration items identified for a plan task.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Recovery Strategy\[sn\_bcp\_recovery\_strategy\]

</td><td>

Stores the recovery strategy associated with an asset identified in a plan loss scenario.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Recovery Team\[sn\_bcp\_recovery\_team\]

</td><td>

Stores the users and groups assigned to the recovery team of a plan.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Plan Template\[sn\_bcp\_template\]

</td><td>

Stores the document sections, element definitions, and loss scenarios identified for each plan template.

</td><td>

Business Continuity Management – Planning

</td></tr><tr><td>

Dependency report source \[sn\_bia\_dependency\_report\_source\]

</td><td>

Stores columns that are tracked in a report. Used while creating an ad-hoc report on the dependency table.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Impact Analysis\[sn\_bia\_analysis\]

</td><td>

Stores all data related to BIA and the template it uses.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Impact Category Result\[sn\_bia\_category\_result\]

</td><td>

Stores the impact category results of all BIAs.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Dependency\[sn\_bia\_dependency\]

</td><td>

Stores the dependency groups and their item details.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Impact Dependency Group\[sn\_bia\_dependency\_group\]

</td><td>

Stores element definitions or the dependency groups associated with a BIA.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Result\[sn\_bia\_result\]

</td><td>

Stores the category result, disruption duration, and the impact rating data.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

BIA Template\[sn\_bia\_template\]

</td><td>

Stores the impact categories and dependency groups that a business process depends on.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Score timeframe mapping \[sn\_bia\_score\_timeframe\_mapping\]

</td><td>

Stores the mapping results of the threshold score and the timeframe.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Activated Plan\[sn\_recovery\_activated\_plan\]

</td><td>

Stores the list of recovery plans activated in an exercise or actual event.

</td><td>

Business Continuity Management – Recovery Exercise Management

</td></tr><tr><td>

Event\[sn\_recovery\_event\]

</td><td>

Stores the status and owner details of events.

</td><td>

Business Continuity Management – Recovery Exercise Management

</td></tr><tr><td>

Event Assets \[sn\_recovery\_event\_asset\]

</td><td>

Stores the asset name and the state whether the asset is recovered or not in an actual or exercise event.

</td><td>

Business Continuity Management – Recovery Exercise Management

</td></tr><tr><td>

Event Task\[sn\_recovery\_event\_task\]

</td><td>

Stores the status details and assignees of event tasks.

</td><td>

Business Continuity Management – Recovery Exercise Management

</td></tr><tr><td>

Impacted Asset to Activated Plan \[sn\_recovery\_impacted\_asset\_to\_activated\_plan\]

</td><td>

Maps impacted assets with the activated plans.

</td><td>

Business Continuity Management – Recovery Exercise Management

</td></tr><tr><td>

Approval \[sn\_recovery\_approval\]

</td><td>

Store approval details of the event.

</td><td>

Business Continuity Management – Recovery Exercise Management

</td></tr><tr><td>

Approval Configuration \[sn\_grc\_appr\_approval\_configuration\]

</td><td>

Stores approval configuration information that applies to any business document like BIA, BCP, events, or any table.

</td><td>

Business Continuity Management – Approver Configurator

</td></tr><tr><td>

Approval Level \[sn\_grc\_appr\_approval\_level\]

</td><td>

Stores approval level information for an approval configuration of a business document.

</td><td>

Business Continuity Management – Approver Configurator

</td></tr><tr><td>

Approval Rule \[sn\_grc\_appr\_approval\_rule\]

</td><td>

Stores information of the approval rule applied to the business document.

</td><td>

Business Continuity Management – Approver Configurator

</td></tr><tr><td>

Approval \[sn\_grc\_appr\_approval\]

</td><td>

Stores information of the approvers for each approval level.

</td><td>

Business Continuity Management – Approver Configurator

</td></tr><tr><td>

Approval \[sn\_bia\_approval\]

</td><td>

Stores information of the BIA approvers for each approval level.

</td><td>

Business Continuity Management – Impact Analysis

</td></tr><tr><td>

Approval \[sn\_bcp\_approval\]

</td><td>

Stores information of the BCP approvers for each approval level.

</td><td>

Business Continuity Management – Planning

</td></tr></tbody>
</table>## Properties installed

For properties installed with the Business Continuity Management application, see [Properties installed with BCM](properties-bcm.md).

**Parent Topic:**[BCM reference](bcm-reference.md)

## Script includes in Business Continuity Management

When you download the Business Continuity Management application, several scripts includes are added to your instance.

### Script includes updated for the Yokohama release

|Script-includes|Description|
|---------------|-----------|
|ActivePlanCandidateFilter|Contains the utility functions that are used in the BCP active plan filter.|
|AssessmentTemplateBIAFieldsUtilBase|Functions used in creating AssessmentTemplateBIAFields record from selected assessment templates.|
|AssessmentTemplateBIAFieldsUtil|Script include to override BIA creation functions in AssessmentTemplateBIAFieldsUtilBase.|
|BCPConstants|Contains the utility functions that are used in the BCP constants.|
|BCPDataVisualizationUtilsBase|Contains the utility functions that are used in the BCP data visualization.|
|BCPDependencySnapshotUpdateStrategyBase|Contains the API for updating the dependencies in plans.|
|BCPDocumentationRecordAPIBase|Contains the utility functions that are used in the BCP documentation record API base.|
|BCPDocumentationRecordAPI|Contains the utility functions that are used in the BCP documentation record APIs.​|
|BCPRecordUI|Contains the utility functions that are used in the BCP record UI pages.​|
|BCPRecordUIBase|Contains the utility functions that are used in the BCP record UI base.​|
|BCPRecordAPI|Contains the utility functions that are used in the BCP record API.|
|BCPTemplateUtilsBase|Contains the utility functions that are used in the BCP template utilities base.|
|BIAAjaxProcessor|Helper class to handle Ajax requests from client scripts. Implementing methods:1. To determine visibility of "Include CIA" field on BIA Template form.2. To set "Applies to table" field with source table name of primary element assessed.|
|BIARecordAPIBase|An API built to interact with BIA records. The goal of this API is to hide the implementation details about BIA records, and provide the consumers with a structured API to retrieve and update data for BIA records.|
|BIAAssessmentUIBase|Utility class to support Business Impact Analysis Assessment UI pages.|
|BIAUtil|Script to handle insert and updates on BIA table, including validationsSetting depends on table field based on dependency group element definition.|
|BIASmartAssessmentBase|Utility class to support all Smart Assessment functionality.|
|BIASmartAssessment|Script include to override Smart Assessment related functions in BIASmartAssessmentBase|
|BIAConstants|Generic class for BIA constants|
|BIACopyUtilBase|Utility to copy existing BIA and generate a new BIA in draft state.|
|BIARecordCreationUtilBase|Functions used in creating BIAs from templates|
|BIAFilterUtilBase|Script which contains functions to provide reference qualifiers on BIA tables.|
|BIADependencySnapshotUpdateStrategyBase|Contains the API for updating the dependencies in the BIAs.|
|DependencySnapshotUpdateStrategyBase|Contains the API for the Update dependencies action and scheduled job​.|
|EventDependencyUpdateStrategyBase|Contains the API for updating the dependencies in the events.|
|PlanRestAPIResourceUtil|Contains the utility functions that are used in the BCP Plan Rest API resource utility.|
|PlanRestAPIResourceUtil|Contains the utility functions that are used in the BCP plan Rest API resource utility.|
|PopulateBIAForPlanAsset|Contains the utility functions that are used to populate the BIA for the plan and asset.|
|PlanCopyUtilBase|Contains the utility functions that are used in the BCP plan copy utility base.|
|PlanUtil|Contains the utility functions that are used in the BCP plan utility.|
|PlanCommonUtils|Contains the utility functions that are used in the plan common utility.|
|RecoveryTasksUtil|Contains the utility functions that are used in the BCP recovery tasks utility.|

### Scripts used for Nested events

|Name|Description|
|----|-----------|
|EventTaskGanttUIBase|Utility class to support event task hierarchical view.|
|EventTaskGanttUI|Script include to override event task hierarchical view functions in EventTaskGanttUIBase.|
|EventSandboxCallableUtilsBase|Utility class containing sandbox callable functions.|
|EventSandboxCallableUtils|Script include to override event related functions in EventSandboxCallableUtilsBase.|
|EventRecordProgressTrackerBase|Utility class to support progress tracker functionality for event.|
|EventRecordProgressTracker|Script include to override progress tracker related functions in EventRecordProgressTrackerBase.|
|BCMRecoveryConstants|Generic class for recovery constants.|
|EventRecordAPIBase|An API to interact with event record.|
|EventTaskUtil|Utility class for event tasks.|
|ActivatedPlanRecordAPIBase|An API to interact with activated plan record.|


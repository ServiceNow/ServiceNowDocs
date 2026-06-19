---
title: Components installed with Business Continuity Management
description: Several types of components are installed with activation of the Business Continuity Management application.When you download the Business Continuity Management application, several scripts includes are added to your instance.Use this reference to integrate the shared Microsoft Excel import and export library into your ServiceNow application. It lists the library components, configuration class methods, artifacts that you must create, and example code for export, import, and combined integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/installed-with-bcm.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 23
keywords: [BCM, import, export, Excel, integration, extension point, Record Transform Engine]
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

For more information on the roles in the GRC: Approver Configurator application, see [Roles installed with GRC: Approver Configurator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/roles-installed-with-approver-configurator.md).


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

Read access**Note:** If you have the BCM planner role and you are not the owner of the exercise, you cannot remove the assets from an exercise or remove a plan from the exercise, but you can add the assets or a plan. Additionally, if you are not the plan owner, you can only add the approved plans in an exercise or crisis event.

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

For information on the BCM lite operator role, see [BCM lite operators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-lite-operators.md).

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

For properties installed with the Business Continuity Management application, see [Properties installed with BCM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/properties-bcm.md).

**Parent Topic:**[BCM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-reference.md)

## Script includes in Business Continuity Management

When you download the Business Continuity Management application, several scripts includes are added to your instance.

### Script includes updated for the Australia release

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

## Import and export integration reference

Use this reference to integrate the shared Microsoft Excel import and export library into your ServiceNow application. It lists the library components, configuration class methods, artifacts that you must create, and example code for export, import, and combined integrations.

### How the shared library works

The shared library is delivered in the scope \(repository\). Consumer applications such as Business Continuity Management provide configuration only and do not modify the shared library.

The architecture uses an extension point pattern:

-   The shared library defines an extension point.
-   Your application creates a configuration class that implements this extension point.
-   The shared library discovers your configuration at runtime by matching the value of `getTable()` against the target table.

One configuration class drives both export and import. The same field list and dot-walk configuration ensure round-trip consistency: export writes the dot-walked value \(for example, `user_name`\) to Microsoft Excel, and import resolves that value back to `sys_id`.

### Shared layer components

You do not modify these shared layer components. The following table describes each component and its responsibility in the import and export flow.

|Component|Description|
|---------|-----------|
|ImportExportConfigReader|Resolves your configuration, builds the export URL, and resolves dot-walk values during import.|
|ExcelExportAjax|Fetches metadata, drop-down options, and records that are written to the Microsoft Excel file.|
|excel\_export\_modal \(UI Page\)|Builds the Microsoft Excel workbook on the client side using the ExcelJS library.|
|ImportDataUtils|Validates the attachment, queues the asynchronous import, parses the Microsoft Excel file, loads data into the staging table, and triggers the Record Transform Engine \(RTE\) transform.|
|Event Registration and Script Action|Asynchronous event queue \(`process_import_data`\) that connects the import queue to the processing logic.|
|ImportProgressTracker|Tracks import progress and provides per-row updates that drive the inline progress tracker on the parent record.|

### Artifacts to create in your application scope

Everything described in this section is created in your application scope. The following table lists the artifacts that are always required, regardless of whether you implement export, import, or both.

|Artifact|Description|
|--------|-----------|
|&lt;Table&gt;ImportExportConfigBase|Script include \(sys\_policy: read\). Contains all configuration method implementations.|
|&lt;Table&gt;ImportExportConfig|Script include. Thin concrete class that extends the base class and is registered as the extension instance.|
|Extension Instance|A `sys_extension_instance` record that points to your configuration class.|

The following table lists the additional artifacts that are required for export.

|Artifact|Description|
|--------|-----------|
|Declarative Action \(client script\)|Calls `ImportExportConfigReader.getExportUrl()` through GlideAjax and opens the export modal.|
|System Properties|Recommended. `<scope>.<table>_excel_export_max_rows` and `<scope>.<table>_excel_export_max_dropdown_records`.|

The following table lists the additional artifacts that are required for import.

|Artifact|Description|
|--------|-----------|
|Declarative Action \(UXF client action or server script\)|Calls `ImportDataUtils.queueImport()`.|
|Dictionary field|A `file_attachment` field on the parent table that is used to upload the Microsoft Excel file.|
|Staging table|Extends `sys_import_set_row`. String columns that match the import fields.|
|ACLs on the staging table|CRUD and `report_view` access for your admin role.|
|RTE configuration|ETL Definition, Staging Entity, Target Entity, Entity Mapping, Robust Import Set Transformer, and Field Mappings \(one per column\).|
|RTE Script Operations \(optional\)|Required only for reference fields with dot-walk configuration. Resolves display values to sys\_ids.|

### Configuration class methods

The configuration base class implements the methods that are described in this section. Implement only the methods that your use case requires.

The following table describes the shared methods that are required for both export and import.

|Method|Returns|Description|
|------|-------|-----------|
|getTable\(\)|string|Target table name, for example `sn_recovery_event_task`.|
|getFields\(\)|string\[\]|Ordered field list. Drives export columns and import mapping.|
|getDotWalkFields\(\)|Object|Object of the form `{ fieldName: dotWalkField }`, for example `{ assigned_to: 'user_name' }`. Export shows the dot-walk value and import resolves it back to `sys_id`.|
|getOrderByField\(\)|string|Sort field used by export queries. Defaults to `number`.|
|setSourceRecord\(gr\)|void|Optional. Called by the shared layer when a parent record is available. Store the parent record so that `getRefQualOverrides()` can reference it.|

The following table describes the export-related methods.

|Method|Returns|Description|
|------|-------|-----------|
|getProtectedFields\(\)|string\[\]|Read-only columns in the Microsoft Excel sheet \(locked cells\).|
|getUniqueFields\(\)|string\[\]|Columns that use duplicate highlighting through conditional formatting.|
|getHiddenColumns\(\)|string\[\]|Columns that are exported but hidden from the user.|
|getNoValidationFields\(\)|string\[\]|Fields that skip drop-down and reference validation.|
|getRefQualOverrides\(\)|Object|Reference qualifier overrides per field. Can use the stored source record for dynamic filtering.|
|getInfoSheetsDetails\(\)|Object|Extra sheets, in the form `{ sheetName: [{ key: value }] }`.|
|getMaxRows\(\)|string \| number|Maximum rows to export, read from the system property.|
|getMaxDropdownRecords\(\)|string \| number|Maximum drop-down options before falling back to a plain text string.|
|getAllowTemplateDownload\(\)|boolean|When `true`, users can download an empty template even when no data rows exist.|
|getRestrictEditsToExportedRows\(\)|boolean|When `true`, only the exported data rows have drop-down lists and validation. Rows beyond the data are locked.|

The following table describes the import-related methods.

<table id="table_import_methods"><thead><tr><th>

Method

</th><th>

Returns

</th><th>

Description

</th></tr></thead><tbody><tr><td>

getStagingTableName\(\)

</td><td>

string

</td><td>

Staging table name, which extends `sys_import_set_row`.

</td></tr><tr><td>

getImportFieldMapping\(\)

</td><td>

Object

</td><td>

Object of the form `{ fieldKey: stagingColumnName }`. Maps configuration fields to staging table columns.

</td></tr><tr><td>

getSheetConfig\(\)

</td><td>

Object

</td><td>

Object of the form `{ sheetName: string, headerRowsToSkip: number }`. Specifies which sheet to read and how many header rows to skip.

</td></tr><tr><td>

getImportAttachmentField\(\)

</td><td>

string

</td><td>

Name of the `file_attachment` field on the parent record. The shared layer clears this field after the import completes \(whether it succeeds or fails\) so that the user can re-import.

</td></tr><tr><td>

onBeforeStagingInsert\(recordGr\)

</td><td>

void

</td><td>

Optional. Called for each row before it is inserted into the staging table. Use this method to stamp parent context, for example `recordGr.setValue('event', this._sourceRecordSysId)`.

</td></tr><tr><td>

validateAttachment\(sysId\)

</td><td>

string\|null

</td><td>

Optional. Custom validation on the uploaded file. Return an error message string to abort the import. Return null if the file is valid.

</td></tr><tr><td>

validateRow \(Source, Target\)

</td><td>

Void

</td><td>

Optional. Called per staging row before transform \(`ETL on_before_script`\). To reject a row, set `ignore = true` and `ignore_reason` to a user-facing message. The Record Transform Engine skips rejected rows and logs the reason.

 **Note:** ETL stands for Extract, Transform, Load—a data integration process used to collect, process, and store data for analysis and reporting.

</td></tr><tr><td>

postProcessRow \(Source, Target\)

</td><td>

Void

</td><td>

Optional. Called per row after transform \(`ETL on_after_script`\). Use for post-transform operations such as updating related records or resolving cross-row dependencies.

</td></tr></tbody>
</table>### Method usage matrix

The following table indicates which methods are required, optional, or not needed for each integration mode. A check mark \(✓\) indicates that the method is required. A dot \(·\) indicates that it is not needed, and a circle \(○\) indicates that the method is optional.

|Method|Export only|Import only|Both|
|------|-----------|-----------|----|
|getTable\(\)|✓|✓|✓|
|getFields\(\)|✓|✓|✓|
|getDotWalkFields\(\)|o|o|o|
|getOrderByField\(\)|✓|·|✓|
|setSourceRecord\(gr\)|o|o|o|
|getProtectedFields\(\)|✓|·|✓|
|getUniqueFields\(\)|✓|·|✓|
|getHiddenColumns\(\)|o|o|o|
|getNoValidationFields\(\)|o|o|o|
|getRefQualOverrides\(\)|o|o|o|
|getInfoSheetsDetails\(\)|o|o|o|
|getMaxRows\(\)|✓|·|✓|
|getMaxDropdownRecords\(\)|✓|·|✓|
|getAllowTemplateDownload\(\)|✓|·|✓|
|getRestrictEditsToExportedRows\(\)|o|·|o|
|getStagingTableName\(\)|·|✓|✓|
|getImportFieldMapping\(\)|·|✓|✓|
|getSheetConfig\(\)|·|✓|✓|
|getImportAttachmentField\(\)|·|✓|✓|
|onBeforeStagingInsert\(recordGr\)|·|o|o|
|validateAttachment\(sysId\)|·|o|o|
|validateRow \(Source, Target\)|o|o|o|
|postProcessRow \(Source, Target\)|o|o|o|

### Export setup

The following example shows an export-only configuration base class.

```
const YourTableImportExportConfigBase = Class.create();
YourTableImportExportConfigBase.prototype = {
    initialize: function() {},

    getTable: function() {
        return 'your_table_name';
    },

    getFields: function() {
        return ['number', 'name', 'status', 'assigned_to', 'due_date'];
    },

    getDotWalkFields: function() {
        return { assigned_to: 'user_name' };
    },

    getOrderByField: function() {
        return 'number';
    },

    getProtectedFields: function() {
        return ['number', 'name'];
    },

    getUniqueFields: function() {
        return ['number'];
    },

    getHiddenColumns: function() {
        return [];
    },

    getNoValidationFields: function() {
        return [];
    },

    getRefQualOverrides: function() {
        return {};
    },

    getInfoSheetsDetails: function() {
        return {
            'Instructions': [
                {
                    column: gs.getMessage('Number*'),
                    instruction: gs.getMessage('Unique identifier'),
                    validation: gs.getMessage('Read-only'),
                    example: gs.getMessage('RA0001001'),
                },
            ],
        };
    },

    getMaxRows: function() {
        return parseInt(gs.getProperty('your_scope.your_table_excel_export_max_rows', '10000'), 10);
    },

    getMaxDropdownRecords: function() {
        return parseInt(gs.getProperty('your_scope.your_table_excel_export_max_dropdown_records', '10000'), 10);
    },

    getAllowTemplateDownload: function() {
        return true;
    },

    type: 'YourTableImportExportConfigBase'
};
```

**Note:** The `sysparm_sourceTable` and `sysparm_sourceId` parameters are optional. Include them only when your configuration uses `setSourceRecord()` for dynamic reference qualifiers, such as filtering drop-down lists by parent record.

Create two system properties in your application scope. The following table describes the properties.

|Property name|Default|Purpose|
|-------------|-------|-------|
|&lt;scope&gt;.&lt;table&gt;\_excel\_export\_max\_rows|10000|Maximum number of data rows in an export.|
|&lt;scope&gt;.&lt;table&gt;\_excel\_export\_max\_dropdown\_records|10000|Maximum number of drop-down options per field before the column falls back to a plain text string.|

### Import setup

Add the following methods to your configuration base class, in addition to the shared methods.

```
getStagingTableName: function() {
    return 'your_table_import';
},

getImportFieldMapping: function() {
    return {
        number: 'number',
        name: 'name',
        status: 'status',
        assigned_to: 'assigned_to',
    };
},

getSheetConfig: function() {
    return {
        sheetName: 'Your Sheet Name',
        headerRowsToSkip: 1,
    };
},

getImportAttachmentField: function() {
    return 'your_import_file_field';
},

onBeforeStagingInsert: function(recordGr) {
    if (this._sourceRecordSysId) {
        recordGr.setValue('parent_field', this._sourceRecordSysId);
    }
},
```

**Note:** The `sheetName` value must match the tab name in the Microsoft Excel file. When you implement both export and import, this value must match the data sheet tab name that is generated during export.

Create a staging table that extends `sys_import_set_row` with string columns that match the import fields. The following table describes the columns for a typical staging table.

|Column|Type|Notes|
|------|----|-----|
|Number|String \(50\)|Coalesce field. Used to match existing records.|
|Name|String \(255\)|—|
|Status|String \(40\)|—|
|Assigned\_to|String \(150\)|Stored as raw text from Microsoft Excel. The Record Transform Engine resolves the value to `sys_id`.|

All columns are strings, regardless of the target field type. The RTE transform handles type conversion. Create CRUD and `report_view` ACLs on the staging table for your admin role.

Add a `file_attachment` dictionary field to the parent table \(for example, the event table\). Users upload the Microsoft Excel file to this field before they trigger the import.

Create the following records in your application scope to configure the Record Transform Engine.

|Record|Purpose|
|------|-------|
|ETL Definition|Top-level container for the transform.|
|Staging Entity|Points to your staging table.|
|Target Entity|Points to your target table.|
|Entity Mapping|Maps the staging entity to the target entity. Coalesce on `number` to ensure that the operation is an update, not an insert.|
|Robust Import Set Transformer|Connects the ETL definition to the staging table.|
|Field Mappings|One field mapping per staging column to target field.|

If you have reference fields with dot-walk configuration \(for example, `assigned_to` mapped to `user_name`\), create one RTE script operation per field. The following example shows a script operation that resolves dot-walk values during import.

**Important:** The Record Transform Engine runs ES5 only \(Rhino\). Use `var`, `function()`, and `.concat()`. Do not use `const`, `let`, arrow functions, or template literals.

### Combined import and export integration

When you implement both directions, use a single configuration class with all methods that are described in the export setup and import setup sections. A single configuration class ensures round-trip consistency.

|Direction|What happens|
|---------|------------|
|Export|`getDotWalkFields()` returns `{ assigned_to: 'user_name' }`. The Microsoft Excel file shows the user name value, for example, `abel.tuter`.|
|Import|The RTE script operation calls `resolveDotWalkValues(tableName, fieldName, batch, output)`, which resolves the value back to `sys_id`.|

The same dot-walk configuration drives both directions. Protected fields, which are locked in Microsoft Excel, prevent users from modifying the coalesce keys that the import relies on for matching. Create all artifacts that are listed for both export and import, but use a single shared configuration class.

### Onboarding checklist

Use the following checklist when you onboard a new consumer application. The checklist is grouped by integration mode.

<table id="table_onboarding"><thead><tr><th>

Mode

</th><th>

Items to complete

</th></tr></thead><tbody><tr><td>

Export only

</td><td>

-   Configuration base class with shared and export methods.
-   Configuration class that extends the base class.
-   Declarative action client script with GlideAjax that opens the export modal.
-   System properties for `max_rows` and `max_dropdown_records`.

</td></tr><tr><td>

Import only

</td><td>

-   Configuration base class with shared and import methods.
-   `getImportAttachmentField()` returns the parent attachment field name.
-   \(Optional\) `onBeforeStagingInsert(recordGr)` stamps parent context on each row.
-   Configuration class that extends the base class.
-   Staging table that extends `sys_import_set_row` with string columns.
-   ACLs on the staging table \(CRUD and `report_view`\).
-   `file_attachment` dictionary field on the parent table.
-   Declarative action that calls `ImportDataUtils.queueImport()`.
-   RTE: ETL Definition, Staging Entity, Target Entity, Entity Mapping, and transformer.
-   RTE: field mappings \(one per staging column to target field\).
-   RTE: script operations for dot-walk reference fields \(if applicable\).

</td></tr><tr><td>

Combined

</td><td>

-   All items from the export-only and import-only checklists.
-   A single configuration class that implements all methods.
-   Round-trip consistency verified: export dot-walk values, and confirm that import resolves the same values back.

</td></tr><tr><td>

ValidateRow and PostProcessRow

</td><td>

Optional per-row validation and post-processing hooks, implemented in the configuration class and integrated into the Extract, Transform, Load \(ETL\) pipeline through `on_before_script` and `on_after_script`.

</td></tr></tbody>
</table>### Troubleshooting

Use the following table to diagnose and resolve common issues that arise during integration.

|Problem|Cause|Fix|
|-------|-----|---|
|Extension point not found|Configuration class is not registered, or `getTable()` returns the wrong value.|Verify the extension instance record and the table name.|
|Export modal is blank|GlideAjax returns `null`.|Verify that `ImportExportConfigReader` has `client_callable=true`.|
|Import silently does nothing|`queueImport()` returns `false`.|Verify that the attachment exists, that it is an .xlsx file, and that the extension point resolves.|
|RTE transforms 0 records|Stale import set GlideRecord.|The shared layer re-fetches by `sys_id`. Verify that the staging table has data.|
|Dot-walk values not resolved|`getDotWalkFields()` is missing or has the wrong field name.|Verify that the configuration matches the `sys_dictionary` reference.|
|Data policy blocks import|`apply_import_set=true` on the target table.|Set `apply_import_set=false` on the blocking data policies.|
|ES6 syntax in RTE script operation|Use of `const`, `let`, or arrow functions.|RTE runs ES5 \(Rhino\). Use `var`, `function`, and `.concat()`.|
|Round-trip mismatch on a reference field|Export shows the display name, but import cannot resolve it.|Add the field to `getDotWalkFields()`. The RTE target must use the same dot-walk path.|
|Progress tracker stuck|Unhandled exception in `processAttachment`.|Check the system logs. The tracker automatically transitions to an error state when an exception is caught.|
|Import rejects valid rows|Row fails validation logic|Check validateRow.|
|GlideList values rejected|Dot-walk field format mismatch|Match dot-walk field format.|
|Protected fields edited after removing sheet protection|Fields are still protected at the import set level|Ignored by import.|


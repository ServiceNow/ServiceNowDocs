---
title: Installed with Service Management Core
description: Several types of components are installed with the Service Management Core plugin.Tables are added with Service Management Core.Properties are added with Service Management Core.Roles are added with Service Management Core.Script includes are added with Service Management Core.Client scripts are added with Service Management Core.Business rules are added with Service Management Core.Email notifications are added with Service Management Core.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 23
breadcrumb: [Service Management Core installation reference, Service Management]
---

# Installed with Service Management Core

Several types of components are installed with the Service Management Core plugin.

Demo data is available with Service Management Core.

**Parent Topic:**[Service Management Core installation reference](r_ServMgmtCoreInstallRef.md)

## Tables installed with Service Management Core

Tables are added with Service Management Core.

<table id="table_u5j_fry_dt"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Part Requirement\[cmdb\_model\_part\_requirement\]

</td><td>

Defines a relationship between a service order task an an asset \(part\) required to complete this task.

</td></tr><tr><td>

Service Order Model\[cmdb\_serviceorder\_product\_model\]

</td><td>

Stores service order templates.

</td></tr><tr><td>

Service Task Model\[cmdb\_servicetask\_product\_model\]

</td><td>

Stores service task templates.

</td></tr><tr><td>

Service Management Flow \[sf\_state\_flow\]

</td><td>

State flows for Service Management.

</td></tr><tr><td>

Service Order Flow \[sf\_sm\_order\]

</td><td>

State flows for service orders.

</td></tr><tr><td>

Service Task Flow \[sf\_sm\_task\]

</td><td>

State flows for service order tasks.

</td></tr><tr><td>

Asset Usage \[sm\_asset\_usage\]

</td><td>

Defines relationship between a service order task and the assets used to complete this task.

</td></tr><tr><td>

SM Category\[sm\_category\]

</td><td>

Links a single service order template to a service order category value.

</td></tr><tr><td>

SM Config Module \[sm\_config\_module\]

</td><td>

Links a configuration to a set of navigation modules that are shown or hidden based on configuration settings.

</td></tr><tr><td>

SM Config\[sm\_config\]

</td><td>

Service management application configuration.

</td></tr><tr><td>

Service Management Incidentals\[sm\_incidentals\]

</td><td>

Incidental items used to complete a service order task.

</td></tr><tr><td>

Service Order Groups Dependency\[sm\_m2m\_group\_dependency\]

</td><td>

Dispatch groups that handle scheduling for assignment groups.

</td></tr><tr><td>

SM Model Application\[sm\_m2m\_model\_application\]

</td><td>

Links SM applications to hardware and consumable models often used in part sourcing.

</td></tr><tr><td>

SM Model Knowledge\[sm\_m2m\_model\_knowledge\]

</td><td>

Relates any knowledge page to any model.

</td></tr><tr><td>

Affected CI \[sm\_m2m\_order\_affected\_ci\]

</td><td>

Configuration items related to a service order.

</td></tr><tr><td>

Service Order Task Models\[sm\_m2m\_somodel\_stmodel\]

</td><td>

Links service task models to service order models.

</td></tr><tr><td>

Task Affected CI \[sm\_m2m\_task\_affected\_ci\]

</td><td>

Configuration items related to a service order task.

</td></tr><tr><td>

Service Order Task Contract\[sm\_m2m\_task\_contract\]

</td><td>

Defines a relationship between a task and contract.

</td></tr><tr><td>

Service Order Task Dependency\[sm\_m2m\_task\_dependency\]

</td><td>

Defines a dependency between two service order tasks: downstream task cannot be started before upstream task gets completed.

</td></tr><tr><td>

Service Order Task Template Dependency\[sm\_m2m\_task\_template\_dependency\]

</td><td>

Defines a dependency between two service order task templates: downstream task cannot be started before upstream task gets completed.

</td></tr><tr><td>

SM Notification Rule \[sm\_notification\_rule\]

</td><td>

Service management notification rules.

</td></tr><tr><td>

Service Order \[sm\_order\]

</td><td>

Defines and manages work that needs to be performed.

</td></tr><tr><td>

Part Requirement \[sm\_part\_requirement\]

</td><td>

Defines a relationship between a service order task and an asset \(part\) required to complete this task.

</td></tr><tr><td>

Service Task \[sm\_task\]

</td><td>

Unit of work performed by one person in one session \(one location, one time\).

</td></tr><tr><td>

SM Template Definition\[sm\_template\_definition\]

</td><td>

Defines a field and value that will be included in a service order template.

</td></tr><tr><td>

Task Asset \[task\_asset\]

</td><td>

Assets related to a task.

</td></tr></tbody>
</table>## Properties installed with Service Management Core

Properties are added with Service Management Core.

|Property|Description|
|--------|-----------|
|Properties for service management core|
|sm.template.minute.step|Default minute step for date time or time fields on service order template page. Can be overridden for a specific application by replacing "sm.template" with the appropriate property prefix. See application configuration record.|
|sm.template.hour.step|Default hour step for date time or time fields on service order template page. Can be overridden for a specific application by replacing "sm.template" with the appropriate property prefix. See application configuration record.|
|glide.autodispatch.debug|Whether auto dispatch engine should output logs when assigning tasks.|

## Roles installed with Service Management Core

Roles are added with Service Management Core.

|Role title \[name\]|Description|
|-------------------|-----------|
|personalize\_read\_dictionary|Role allowing service management application admins the ability to see fields when modifying field controls \(for example, mandatory fields, read-only fields\) on the state flow form.|
|sm\_qualifier|Qualifier role used when creating SM applications. This role is a template only and it does not provide actual access to any navigation modules or records.|
|sm\_agent|Agent role used when creating SM applications. Performs work on a task. This role is a template only and it does not provide actual access to any navigation modules or records.|
|sm\_approver\_user|Approver user role used when creating SM application. Approves requests. This role is a template only and it does not provide actual access to any navigation modules or records|
|sm\_initiator|Initiator user role used when creating SM application. Grants UI access, as well as performing the same functions as Basic. This role is a template only and it does not provide actual access to any navigation modules or records.|
|service\_fulfiller|Role allowing service management users the ability to see the Service Desk modules.|
|sm\_admin|Admin user role used when creating SM application. Controls all data. This role is a template only and it does not provide actual access to any navigation modules or records|
|sm\_basic|Basic user role used when creating SM application. Reads and creates requests, and follows up on those requests. This role is a template only and it does not provide actual access to any navigation modules or records.|
|sm\_dispatcher|Dispatcher user role used when creating SM application. Schedules and assigns tasks to agents. This role is a template only and it does not provide actual access to any navigation modules or record.|
|sm\_read|Read-only user role used when creating SM application. This role is a template only and it does not provide actual access to any navigation modules or records.|
|template\_admin|Grants the ability to create and administer Service Management templates.|

## Script includes installed with Service Management Core

Script includes are added with Service Management Core.

|Script includes|Description|
|---------------|-----------|
|PartRequirementStateHandler|Marks a part requirement Sourced or Delivered based on the transfer orders.|
|SMTemplates|Builds a service order and related tasks from an SM Template.|
|SMAutoAssignment|Javascript wrapper around SNC.SMAutoassignment that automatically determines property prefix needed.|
|SMStockRooms|Retrieves and creates personal stockrooms.|
|BaseSMControls|Provides functions used to control access to service management records like the configuration and notification rules. Modify the SMControls Script Include to make changes rather than modifying this Script Include.|
|SMConfigProcessor|Handles changes that are made to the configuration page. Also handles sending notifications set up on the configuration page.|
|SMTemplateHelper|Backend-code for the SM Template page. Should not be customized.|
|AppCreatorCMSCreation|Creates CMS pages for apps created by Service Management template.|
|SMDateRollup|Rolls up the dates from service order tasks to service orders.|
|SMI18nUtils|Utilities for internationalizing the Service Management and Configuration Pages.|
|SMAJAX|Handles Service management AJAX calls.|
|AJAXMileageCalculator|Calculates mileage costs for incidentals.|
|SMCIControls|Service Management CI controls for adding and removing CI's from Orders and Tasks.|
|SharedServiceUtils|Shared Service Utilities|
|SMSourcingDispatch|Contains methods supporting the Agent Schedule section in the lower portion of the Source popup.|
|SMStateFlowCreator|Methods for creating state flows for ESM-based applications.|
|SMAgentStatusAJAX|AJAX wrapper around the updateStatus function available in SMScheduleStatus.|
|SMDateValidation|Verifies that dates in service order tasks are valid and consistent with one another in terms of scheduling.|
|SMTask|Service Management Task utility functions.|
|AppCreatorKnowledgeCreation|Methods for "app creator" engine to create knowledgebase pages.|
|SMAgentStatus|Code for updating the "on schedule" and status of an agent.|
|SMAppCreator|Methods for creating Service management applications.|
|SMScheduleGrapper|Schedule APIs. Gets schedule times from a work order task in milliseconds. Actual times are given priority, if those are not available, return scheduled times.|
|SMTableCreator|Methods for creating tables for Service management applications|
|SMControls|Extension of BaseSMControls. Modify this script for controlling access to service management records like the configuration and notification rules|
|AssetUsageFilters|Reference qualifier filters for AssetUsage.|
|SMTaskDependency|Collection of methods that control the data integrity of the Service Order Tasks Dependency \[sm\_m2m\_task\_dependency\] table.|
|AppCreatorCatalogCreation|Creates an SM application catalog.|
|SMAssetUsage|Asset Usage APIs|
|SMConstants|List of constants used in the State field of the Service Management \(SM\) flows \(sm\_order and sm\_task\) and extended tables \(for example, wm\_order, wm\_task\).|
|SMNotifRuleTables|Restricts tables that are displayed on the SM Notification Rule form to the request and task table of the application.|
|SMTransferOrders|Collection of methods that create or update service management-related transfer order lines.|
|SMPortalCreator|Methods for creating a portal and reports for SM-based applications.|
|WMSourcingAjax|AJAX calls used in the "Source" popup available from Work Orders and Work Order Tasks. Contains methods for displaying work order tasks and part requirements in the tree-section \(left-hand side\), deleting and copying part requirements using the tree, and retrieving task information and agent information for the lower section.|
|SMFilters|Filters for service management.|
|SMUpgradeManager|Handles finding SM application items that need upgrades, storing information, upgrading.|
|SMTemplateMigration|Handles migrating SM templates from previous version of Geneva.|

## Client script includes installed with Service Management Core

Client scripts are added with Service Management Core.

<table id="table_wtf_krf_2t"><thead><tr><th>

Client script includes

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Hide excluded fields

</td><td>

SM Config\[sm\_config\]

</td><td>

Hide sm\_config fields based on exclusion list.

</td></tr><tr><td>

Start work read-only \(exp. travel chg\)

</td><td>

Service order task \[sm\_task\]

</td><td>

Start work read-only when travel is required and not started.

</td></tr><tr><td>

Start work read-only when travel is required and not started

</td><td>

Service order task \[sm\_task\]

</td><td>

Displays an error after a location change when no dispatch group or assignment group covers the location of the work order task.

</td></tr><tr><td>

Show or hide/clear contract field

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

If type is Vendor cost, then show the contract field. Otherwise, clear and hide the contract field.

</td></tr><tr><td>

check order of start date and end date

</td><td>

Service order task \[sm\_task\]

</td><td>

Verify that the start date happens before the end date.

</td></tr><tr><td>

Update Assigned to \(Assign Group change\)

</td><td>

Service order \[sm\_order\]

</td><td>

Update Assigned to when Assignment group changes: - clear the Assigned to field.

</td></tr><tr><td>

Ci update

</td><td>

Service order \[sm\_order\]

</td><td>

Updates the associated asset and location based on changes to the affected CI.

</td></tr><tr><td>

Populate CI Location

</td><td>

Service order \[sm\_order\]

</td><td>

Populates work order location based on CI location.

</td></tr><tr><td>

check\_work\_duration

</td><td>

Service order task \[sm\_task\]

</td><td>

Verify that the work duration is not 0 or empty.

</td></tr><tr><td>

Calculate total amount - quantity

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

Calculates the total mileage costs when the quantity changes.

</td></tr><tr><td>

Validate Estimated Travel Duration

</td><td>

Service order task \[sm\_task\]

</td><td>

Ensure that the estimated travel duration does not carry into the expected start time.

</td></tr><tr><td>

Validate Scheduled Travel Start

</td><td>

Service order task\[sm\_task\]

</td><td>

Ensure that the scheduled travel start \(with its duration\) is before scheduled work start.

</td></tr><tr><td>

Template selected

</td><td>

Service order \[sm\_order\]

</td><td>

Populates form based on template values.

</td></tr><tr><td>

Populate Caller Location

</td><td>

Service order \[sm\_order\]

</td><td>

Sets the location field when the caller is changed.

</td></tr><tr><td>

Check for group errors

</td><td>

Service order \[sm\_order\]

</td><td>

Displays an error on load if no qualification group covers the location of the work order.

</td></tr><tr><td>

Hide unused related lists/fields

</td><td>

Service order \[sm\_order\]

</td><td>

Hides related lists that are not relevant based on application configuration

</td></tr><tr><td>

Ci update

</td><td>

Service order task \[sm\_task\]

</td><td>

Updates the associated asset and location based on changes to the affected CI.

</td></tr><tr><td>

New fields type control

</td><td>

SM Template Definition\[sm\_template\_definition\]

</td><td>

Displays the appropriate field type based on selection of field on template definition page.

</td></tr><tr><td>

Asset update

</td><td>

Service order \[sm\_order\]\[sm\_order\]

</td><td>

Updates the associated configuration item and location based on changes to the affected asset.

</td></tr><tr><td>

Field onload helper

</td><td>

SM Template Definition \[sm\_template\_definition\]

</td><td>

Displays the appropriate field type based on selection of field on template definition page \(onload\).

</td></tr><tr><td>

Read only task templates dependencies

</td><td>

Service Order Task Template Dependency \[sm\_m2m\_task\_template\_dependency\]

</td><td>

Makes the dependent field read only when creating task template dependencies in sm\_m2m\_task\_template\_dependencies table.

</td></tr><tr><td>

Make Location not mandatory

</td><td>

Stockroom \[alm\_stockroom\]

</td><td>

Makes Location not mandatory for stockroom type field\_agent

</td></tr><tr><td>

Calculate End Time \(Duration change\)

</td><td>

Service order task\[sm\_task\]

</td><td>

Calculates Estimated End Time in a Work Order Task based on a change of estimated work duration.

</td></tr><tr><td>

Show error when no application installed

</td><td>

Service Order Model \[cmdb\_serviceorder\_product\_model\]

</td><td>

Show error when no application installed.

</td></tr><tr><td>

Calculate total amount - cost per mile

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

Calculates the total mileage costs when the quantity changes.

</td></tr><tr><td>

Priority assignment

</td><td>

SM Config \[sm\_config\]

</td><td>

Set scheduling to true and hide consistent assignment of priority assignment is turned on.

</td></tr><tr><td>

Asset update

</td><td>

Service order task \[sm\_task\]

</td><td>

Updates the associated configuration item and location based on changes to the affected asset.

</td></tr><tr><td>

Read only group dependencies

</td><td>

Service Order Group Dependency \[sm\_m2m\_group\_dependency\]

</td><td>

Once set, fields are read-only.

</td></tr><tr><td>

Add sourcing UI Listeners

</td><td>

Service order task\[sm\_task\]

</td><td>

Sets up event listeners for changes to travel duration, work duration, or expected work start so that they are automatically updated in the sourcing UI \(if the task is opened via the sourcing UI\).

</td></tr><tr><td>

check window\_start

</td><td>

Service order task \[sm\_task\]

</td><td>

Verify that window start is before window end.

</td></tr><tr><td>

Set required quantity read-only

</td><td>

Part Requirement \[sm\_part\_requirement\]

</td><td>

Sets the Required quantity field to read-only when the required number of assets are sourced for the part requirement

</td></tr><tr><td>

Show messages

</td><td>

Service order task \[sm\_task\]

</td><td>

Shows messages if the expected due date for the task is after the requested due date of the request, or if auto-assignment does not work.

</td></tr><tr><td>

Calculate total amount - type

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

Calculates the total mileage costs when the type changes.

</td></tr><tr><td>

Update Assigned to \(Assign Group change\)

</td><td>

Service order task \[sm\_task\]

</td><td>

Update Assigned to when Assignment group changes: - clear the Assigned to field.

</td></tr><tr><td>

Hide group field

</td><td>

Service Task Model\[cmdb\_servicetask\_product\_model\]

</td><td>

Hides the dispatch group field when dispatch queue is off

</td></tr><tr><td>

Hide state flow field

</td><td>

SM Config \[sm\_config\]

</td><td>

When state flow is turned off, hide the field from the form.

</td></tr><tr><td>

Check TOs before reassigning

</td><td>

Service order task \[sm\_task\]

</td><td>

When reassigning or unassigning a work order task, prompt user to cancel all transfer orders to personal stock rooms for a task if the task only has cancelable transfer orders.

</td></tr><tr><td>

Verify Group Post Dispatch Group Change

</td><td>

Service order task\[sm\_task\]

</td><td>

Displays an error on load if no assignment group covers the location of the work order task.

</td></tr><tr><td>

Set Tables

</td><td>

SM Notification Rule \[sm\_notification\_rule\]

</td><td>

Limit the tables to the two possible tables, if none is chosen, set the first one as the default.

</td></tr><tr><td>

Calculate End Time \(Start time change\)

</td><td>

Service order task \[sm\_task\]

</td><td>

Calculate the Estimated End Time based on Expected Start Time changing. Also checks for inconsistencies that may have been created with estimated travel start.

</td></tr><tr><td>

Update Model and Quantity based on Asset

</td><td>

Asset Usage\[sm\_asset\_usage\]

</td><td>

Synchronizes model and quantity information of an asset usage record based on the asset it references.

</td></tr><tr><td>

Read Only Order Affected Cis

</td><td>

Affected CI\[sm\_m2m\_order\_affected\_ci\]

</td><td>

Makes a field read only once a value is selected for that field.

</td></tr><tr><td>

Reset quantity

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

When the type changes back to car rental, the Qty is set back to 1.

</td></tr><tr><td>

Read Only Task Affected CIs

</td><td>

Task Affected CI\[sm\_m2m\_task\_affected\_ci\]

</td><td>

Makes a field read only once a value is selected for that field.

</td></tr><tr><td>

Hide group field

</td><td>

Service Order Model \[cmdb\_serviceorder\_product\_model\]

</td><td>

Hide the assignment group field if application is not request driven, hide the qualification group field if qualification is off.

</td></tr><tr><td>

Check TOs before reassigning

</td><td>

Service order task \[sm\_task\]

</td><td>

When reassigning or unassigning a work order task, prompt user to cancel all transfer orders to personal stock rooms for a task if the task only has cancelable transfer orders.

</td></tr><tr><td>

Notify parent on submit

</td><td>

Part Requirement \[sm\_part\_requirement\]

</td><td>

Updates the Source tree whenever a new part requirement is created inside the Source popup window.

</td></tr><tr><td>

Show warning msg of templates upgrade

</td><td>

SM Config \[sm\_config\]

</td><td>

Show warning message when the templates must be migrated.

</td></tr><tr><td>

Verify Group Fields

</td><td>

Service order task\[sm\_task\]

</td><td>

Displays an error on load if no dispatch group or assignment group covers the location of the work order task.

</td></tr><tr><td>

Ensure no negative and decimal quantity

</td><td>

Part Requirement\[sm\_part\_requirement\]

</td><td>

Ensures the quantity required for a part is valid.

</td></tr><tr><td>

Read only task dependencies

</td><td>

Service Order Task Dependency \[sm\_m2m\_task\_dependency\]

</td><td>

Making the dependent field read only on creating task dependencies in sm\_m2m\_task\_order table.

</td></tr><tr><td>

Start work read-only \(actual travel chg\)

</td><td>

Service order task \[sm\_task\]

</td><td>

Start work read-only when travel is required and not started. 'Schedule travel start' and 'Schedule start' are mandatory when 'Agent Track Time' is on.

</td></tr><tr><td>

Show warning message of disable SF

</td><td>

SM Config \[sm\_config\]

</td><td>

Shows a warning message when state flows are disabled.

</td></tr><tr><td>

Populate from stockroom for drop off

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Sets the from stock room to the logged in user's personal stockroom when creating a drop off transfer order.

</td></tr><tr><td>

Set value before submit

</td><td>

SM Template Definition\[sm\_template\_definition\]

</td><td>

Sets the value from the various widgets to the appropriate value before submitting the template definition form.

</td></tr><tr><td>

Template selected

</td><td>

Service order task \[sm\_task\]

</td><td>

Populates form based on template values.

</td></tr><tr><td>

Personal Stockroom Name by Type

</td><td>

Stockroom \[alm\_stockroom\]

</td><td>

Sets the name of a stockroom based on its manager when it becomes a personal stockroom.

</td></tr><tr><td>

Update agent status

</td><td>

Service order task \[sm\_task\]

</td><td>

Update the status of assigned agent.

</td></tr><tr><td>

Update UI on load and model change

</td><td>

Asset Usage \[sm\_asset\_usage\]

</td><td>

Update UI on load and model change

</td></tr><tr><td>

Personal Stockroom Name by Manager

</td><td>

Stockroom \[alm\_stockroom\]

</td><td>

Updates the name of a personal stockroom when its manager changes.

</td></tr><tr><td>

Hide unused related lists/fields

</td><td>

Service order task \[sm\_task\]

</td><td>

Hides related lists that are not relevant based on application configuration.

</td></tr><tr><td>

use schedule

</td><td>

SM Config \[sm\_config\]

</td><td>

Turn off priority assignment and show consistent assignment if scheduling is turned off.

</td></tr><tr><td>

Verify Group Post Location Change

</td><td>

Service order \[sm\_order\]\[alm\_stockroom\]

</td><td>

Displays an error after a location change when no qualification group covers the location of the work order.

</td></tr></tbody>
</table>## Business rules installed with Service Management Core

Business rules are added with Service Management Core.

<table id="table_ngl_zwx_dt"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Build scratchpad &amp; display info messages

</td><td>

Service order task \[sm\_task\]

</td><td>

Build scratchpad variables that are used to display initial info messages on page.

</td></tr><tr><td>

Affected CI changed or removed

</td><td>

Service Order \[sm\_order\]

</td><td>

Synchronizes the primary CI field and the Affected CIs related list on the Service Order form.

</td></tr><tr><td>

Verify Work Notes

</td><td>

Service Order \[sm\_order\]

</td><td>

Ensures that the Work notes field is populated in work orders that transition to the Cancel state.

</td></tr><tr><td>

Set default values

</td><td>

SM Template Definition\[sm\_template\_definition\]

</td><td>

Sets the **table** field by default.

</td></tr><tr><td>

Set Personal Stockroom

</td><td>

Transfer Order \[alm\_transfer\_order\]

</td><td>

Automatically sets the stockroom to the personal stockroom of the logged in user for drop-off transfer orders.

</td></tr><tr><td>

Export to update set

</td><td>

Part Requirement \[cmdb\_model\_part\_requirement\]

</td><td>

Exports part requirement templates to the current update set and creates a sys\_metadata\_link record to associate template with current application.

</td></tr><tr><td>

Export to update set

</td><td>

Service Order Task Models \[sm\_m2m\_somodel\_stmodell\]

</td><td>

Exports link between service order template and service task template to the current update set and creates a sys\_metadata\_link record to associate template with current application.

</td></tr><tr><td>

Export to update set

</td><td>

Service Order Task Template\[cmdb\_servicetask\_product\_model\]

</td><td>

Exports service task templates to the current update set and creates a sys\_metadata\_link record to associate template with current application.

</td></tr><tr><td>

Export to update set

</td><td>

Service Order Template\[cmdb\_serviceorder\_product\_model\]

</td><td>

Exports service order templates to the current update set and creates a sys\_metadata\_link record to associate template with current application.

</td></tr><tr><td>

Sync update of associated variables

</td><td>

SM Template Definition \[sm\_template\_definition\]

</td><td>

Synchronizes template definition with associated catalog variable.

</td></tr><tr><td>

Date Checks

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Validates the window, estimated, and actual start and end dates.

</td></tr><tr><td>

Populate Location - New SOT

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Populates the location, if possible, based on parent work order location.

</td></tr><tr><td>

add\_model\_filter

</td><td>

Global \[global\]

</td><td>

Filter for SM Model Application slush bucket, limits available models to hardware and consumable models.

</td></tr><tr><td>

Reset qty to 1

</td><td>

Service Management Incidentals\[sm\_incidentals\]

</td><td>

Sets the quantity field to 1 when the type is Car Rental.

</td></tr><tr><td>

Validate notification

</td><td>

SM Notification Rule\[sm\_notification\_rule\]

</td><td>

Validates that a user or group is selected when inserting or updating a notification rule.

</td></tr><tr><td>

Validate Field Agent Type

</td><td>

Stockroom \[alm\_stockroom\]

</td><td>

Prevents duplicate personal stockrooms.

</td></tr><tr><td>

Calculate cost

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

Helps to calculate the **Cost**when the **Type** is **Mileage** \(starting with the Eureka release\).

</td></tr><tr><td>

Check asset and CI

</td><td>

Service order task \[sm\_task\]

</td><td>

Synchronizes affected Cis and affected assets.

</td></tr><tr><td>

Assign the previous agent on task

</td><td>

Service order task \[sm\_task\]

</td><td>

Sets the previous agent whenever the task assigned to changes.

</td></tr><tr><td>

Populate Service Order from Template

</td><td>

Service Order \[sm\_order\]

</td><td>

Populates a new work order from the work order model selected as a template.

</td></tr><tr><td>

Validate quantity requested

</td><td>

Transfer Order Line \[alm\_transfer\_order\_line\]

</td><td>

Checks that the quantity requested on a transfer order line with a part requirement does not exceed the quantity that is required to fulfill the part requirement \(starting with the Eureka release\).

</td></tr><tr><td>

Close service order on workflow complete

</td><td>

Workflow contexts \[wf\_context\]

</td><td>

Prevents rollup of task closures when there are active workflows on service orders.

</td></tr><tr><td>

Create Sub Tasks

</td><td>

Service Order \[sm\_order\]

</td><td>

When service order leaves draft state, creates tasks from template if service order built from template, or creates default task if task-driven.

</td></tr><tr><td>

Validate Field Agent Name

</td><td>

Stockroom \[alm\_stockroom\]

</td><td>

Validates that a personal stockroom has a valid, associated agent.

</td></tr><tr><td>

Create expense line

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

Creates or updates an expense line based on the incidental's cost when the incidental is saved and all of the following are true: -   The state is Incurred

 -   The type is not None

 -   The cost is not zero

</td></tr><tr><td>

Validation

</td><td>

Service Order Groups Dependency \[sm\_m2m\_group\_dependency\]

</td><td>

Validates that the dependency is valid.

</td></tr><tr><td>

Verify CI on SM Task

</td><td>

Cis Affected \[task\_ci\]

</td><td>

Verifies that the affected CI for a task is also an affected CI for the order.

</td></tr><tr><td>

Vendor type requires manager

</td><td>

User Group \[sys\_user\_group\]

</td><td>

Vendor is required for vendor groups.

</td></tr><tr><td>

Part Requirements

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Creates part requirements for a service order task from the part requirements configured for a service order task model used as a template. Free up assets when unassigned or reassigned. Update asset usages when tasks are closed.

</td></tr><tr><td>

Apply dispatch method

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Automatically assigns a task once it is marked as ready for assignment when assignment method of the application is workflow or auto.

</td></tr><tr><td>

Group change validation

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Validates changes to assignment and dispatch groups in work order tasks.

</td></tr><tr><td>

Assign the previous agent on order

</td><td>

Service Order \[sm\_order\]

</td><td>

Sets the previous agent whenever the order assigned to changes.

</td></tr><tr><td>

ValidateChanges

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Validates dispatch group and assignment group types match and that worknotes are provided if required.

</td></tr><tr><td>

Transitions

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Sets a task into work in progress when the task is accepted and work start is populated.

</td></tr><tr><td>

Sync catalog

</td><td>

SM Config \[sm\_config\]

</td><td>

Synchronizes the application catalog when the service management configuration changes.

</td></tr><tr><td>

Set required by date on display

</td><td>

Part Requirement\[sm\_part\_requirement\]

</td><td>

Sets part requirement required by to the expected travel start of the associate service order task.

</td></tr><tr><td>

Request driven dispatch

</td><td>

Service Order \[sm\_order\]

</td><td>

Responsible for dispatching service orders based on application configuration.

</td></tr><tr><td>

Build scratchpad &amp; display info messages

</td><td>

Service Order \[sm\_order\]

</td><td>

Build scratchpad variables that are used to display initial info messages on page.

</td></tr><tr><td>

Prevent Loop In TaskTemplateDependencies

</td><td>

Service Order Task Template Dependency \[sm\_m2m\_task\_template\_dependency\]

</td><td>

Prevents loops in task template dependencies

</td></tr><tr><td>

getMainSMModels

</td><td>

Global\[global\]

</td><td>

Slush bucket filter when linking service order task templates to service order templates.

</td></tr><tr><td>

Task contract m2m

</td><td>

Service Management Incidentals \[sm\_incidentals\]

</td><td>

Synchronizes contracts, expense lines, and incidentals

</td></tr><tr><td>

Notification for task

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Sends notifications when task changes if values change for fields specified in the configuration page.

</td></tr><tr><td>

Build scratchpad tables

</td><td>

SM Notification Rule\[sm\_notification\_rule\]

</td><td>

Sets the tables that should be displayed on notification rule page.

</td></tr><tr><td>

Update PR based on TOL

</td><td>

Transfer Order Line\[alm\_transfer\_order\_line\]

</td><td>

Updates the part requirement when the associated transfer order line changes stage.

</td></tr><tr><td>

Add removed asset

</td><td>

Asset Usage \[sm\_asset\_usage\]

</td><td>

Determines validity of asset removal and updates the removed asset accordingly.

</td></tr><tr><td>

Add/remove manager to/from vendor group

</td><td>

Group \[sys\_user\_group\]

</td><td>

When group manager changes for a vendor group, add the new manager as a group member and remove the previous manager as a group member.

</td></tr><tr><td>

Service Management Group Types

</td><td>

Group \[sys\_user\_group\]

</td><td>

Ensures data integrity for dispatch group coverage information.

</td></tr><tr><td>

Deletion of Affected CI

</td><td>

Cis Affected \[task\_ci\]

</td><td>

Part of the synchronization mechanism between the primary CI field and the Affected CIs related list on the Service Order form.

</td></tr><tr><td>

Prevent Loop In Tasks Dependencies

</td><td>

Service Order Task Dependency \[sm\_m2m\_task\_dependency\]

</td><td>

Prevents circular work order task dependencies.

</td></tr><tr><td>

Cascade SO deletion

</td><td>

Service Order \[sm\_order\]

</td><td>

Delete service order tasks and checklists when service order is deleted.

</td></tr><tr><td>

Create Personal Stockroom

</td><td>

User Role \[sys\_user\_has\_role\]

</td><td>

Creates a personal stockroom for users \(if they do not have one already\) when they are assigned an agent role.

</td></tr><tr><td>

Delete Personal Stockroom

</td><td>

User Role\[sys\_user\_has\_role\]

</td><td>

Deletes a user's personal stockroom when all agent roles are removed from the user.

</td></tr><tr><td>

Validate Part Requirement

</td><td>

Part Requirement\[sm\_part\_requirement\]

</td><td>

Validates the part requirement and checks for availability of the part. Validates sourcing information.

</td></tr><tr><td>

Invoke template workflow &amp; move task

</td><td>

Service Order \[sm\_order\]

</td><td>

Start workflow for service order and move subtasks to pending dispatch.

</td></tr><tr><td>

Populate Group - Qualification

</td><td>

Service Order \[sm\_order\]

</td><td>

Populates the qualification group, if possible, based on location.

</td></tr><tr><td>

Create catalog

</td><td>

Service Order Template\[cmdb\_serviceorder\_product\_model\]

</td><td>

Create a corresponding record producer if automatic publishing is on.

</td></tr><tr><td>

Populate schedule

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Populates scheduling fields if they are not already set. They are set, only if the state changes to Pending Dispatch.

</td></tr><tr><td>

Notification for request

</td><td>

Service Order \[sm\_order\]

</td><td>

Sends notifications when task changes if values change for fields specified in the configuration page.

</td></tr><tr><td>

Cascade delete checklist

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Delete checklists when service order task is deleted.

</td></tr><tr><td>

Scratchpad

</td><td>

SM Config\[sm\_config\]

</td><td>

Builds scratchpad for SM config form.

</td></tr><tr><td>

Validate TOL and check availability

</td><td>

Transfer Order Line\[alm\_transfer\_order\_line\]

</td><td>

Validates transfer order line state changes and ensures that the asset is available in the stockroom.

</td></tr><tr><td>

Delete all expense lines

</td><td>

SM Incidentals\[sm\_incidentals\]

</td><td>

Delete expense lines when incidentals are deleted.

</td></tr><tr><td>

Populate Schedule - New SOT

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Populates scheduling fields if they are not already set. They are set only if the state changes to Pending Dispatch.

</td></tr><tr><td>

Populate Location

</td><td>

Service Order \[sm\_order\]

</td><td>

Populates the location, if possible, based on the affected CI identified by the caller.

</td></tr><tr><td>

Add as Primary if none set

</td><td>

Cis Affected \[task\_ci\]

</td><td>

Add configuration item as primary affected CI if no primary CI exists.

</td></tr><tr><td>

Roll Up Changes

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Rollup state changes and estimated work times to service order.

</td></tr><tr><td>

Build scratchpad

</td><td>

Service Order Template\[cmdb\_serviceorder\_product\_model\]

</td><td>

Sets scratchpad for service order template form.

</td></tr><tr><td>

Check asset and CI

</td><td>

Service order \[sm\_order\]

</td><td>

Synchronizes affected Cis and affected assets.

</td></tr><tr><td>

Unassigned

</td><td>

Service order \[sm\_order\]

</td><td>

Sets state of service order back to ready when it becomes unassigned.

</td></tr><tr><td>

Propagate priority

</td><td>

Service order \[sm\_order\]

</td><td>

Propagates priority from service order to service order tasks.

</td></tr><tr><td>

Apply configuration settings

</td><td>

SM Config \[sm\_config\]

</td><td>

Handles changes to SM Config record.

</td></tr><tr><td>

Update agent status

</td><td>

Service Order Task \[sm\_task\]

</td><td>

Updates the status of an agent assigned to a task.

</td></tr><tr><td>

Build scratchpad

</td><td>

Service Order Task Template\[cmdb\_servicetask\_product\_model\]

</td><td>

Sets scratchpad for service order task template form.

</td></tr><tr><td>

Check TOs before reassigning

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Sets scratchpad to prevent reassigning a task when there are transfer orders in transit.

</td></tr><tr><td>

Prevent Duplicate Order Affected CIs

</td><td>

Cis Affected \[task\_ci\]

</td><td>

Prevent duplicated affected Cis

</td></tr><tr><td>

Unassigned

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Prevent reassigning a task if there are transfer orders in transit.

</td></tr><tr><td>

SNC - Run parent workflows \(Approval\)

</td><td>

Approval \[sysapproval\_approver\]

</td><td>

Handles order workflows when approval set to "More info required" or "Duplicate".

</td></tr><tr><td>

getTaskSMModels

</td><td>

Global \[global\]

</td><td>

Slush bucket filter when linking service order templates to service task templates.

</td></tr><tr><td>

Prevent model change after sourced

</td><td>

Part Requirement\[sm\_part\_requirement\]

</td><td>

Prevent changing the model after the part requirement is sourced.

</td></tr><tr><td>

Create AssetUsage when TOL delivered

</td><td>

Transfer Order Line\[alm\_transfer\_order\_line\]

</td><td>

Create asset usage once a transfer order line is delivered.

</td></tr><tr><td>

Release Asset on AssetUsage delete

</td><td>

Asset Usage \[sm\_asset\_usage\]

</td><td>

Make asset available when asset usage is deleted.

</td></tr><tr><td>

Redirect TOL to existing TO under WOT

</td><td>

Transfer Order Line\[alm\_transfer\_order\_line\]

</td><td>

Attempts to group transfer order lines under the same transfer order for a service order if the transfer order lines have the same "from" and "to" locations.

</td></tr><tr><td>

Populate Group - Dispatch/Work

</td><td>

Service Order Task\[sm\_task\]

</td><td>

Populates the dispatch group and assignment groups when only one dispatch group covers the location of a task, and only one assignment group is covered by the dispatch group.

</td></tr></tbody>
</table>## Email notifications installed with Service Management Core

Email notifications are added with Service Management Core.

<table id="table_o2m_2mw_dp"><thead><tr><th>

Notification

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

$\{Request\_Label\} created from email

</td><td>

Service Order\[sm\_order\]

</td><td>

Template that is used to build notifications for new applications created from a Service Management template. This notification should remain inactive and not be used.

</td></tr><tr><td>

$\{Request\_Label\} changed

</td><td>

Service Order\[sm\_order\]

</td><td>

Template that is used to build notifications for new applications created from a Service Management template. This notification should remain inactive and not be used.

</td></tr><tr><td>

$\{Task\_Label\} changed

</td><td>

Service Order\[sm\_order\]

</td><td>

Template that is used to build notifications for new applications created from a Service Management template. This notification should remain inactive and not be used.

</td></tr></tbody>
</table>
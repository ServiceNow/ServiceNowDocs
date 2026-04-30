---
title: Flow API - ServiceNow Fluent
description: The Flow API defines flows and subflows \[sys\_hub\_flow\], which automate business processes with reusable multiple-step components.Create a flow \[sys\_hub\_flow\] to run a sequence of actions and flow logic when a set of trigger conditions occur.Create a subflow \[sys\_hub\_flow\] to run a reusbale sequence of actions and flow logic when called by a flow or API.Run a flow when the start conditions of a specific trigger type are met. Triggers determine when a flow runs and what data is available from the flow start conditions.Run a specific action instance from a flow or subflow. Actions determine what data is generated, updated, or retrieved.Run a specific flow logic instance from a flow or subflow. Flow logic determines how and when data is used.Reference a specific runtime data pill value from an action or flow logic input.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 26
keywords: [servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api, servicenow fluent, fluent api]
---

# Flow API - ServiceNow Fluent

The Flow API defines flows and subflows \[sys\_hub\_flow\], which automate business processes with reusable multiple-step components.

Create a flow using the Flow object. For more information, see [Flow object](fluent-flow-api.md#).

Create a subflow using the Subflow object. For more information, see [Subflow object](fluent-flow-api.md#).

For general information about flows, see [Exploring flows](https://www.servicenow.com/docs/access?context=exploring-flows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US). For general information about subflows, see [Exploring subflows](https://www.servicenow.com/docs/access?context=exploring-subflows&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

**Parent Topic:**[ServiceNow Fluent API reference](servicenow-fluent-api-reference.md)

**Related topics**  


[ServiceNow Fluent](../concept/servicenow-fluent.md)

## Flow object

Create a flow \[sys\_hub\_flow\] to run a sequence of actions and flow logic when a set of trigger conditions occur.

Flows only run when their trigger conditions are met. Use flows for event-driven automation that requires a consistent and predefined trigger.

A Flow object consists of these components.

-   One configuration object that defines the flow configuration properties.
-   One wfa.trigger function that defines when to run the flow.
-   One Body function that defines what actions and flow logic to run.
    -   Zero or more wfa.action functions
    -   Zero or more wfa.flow\_logic functions

<table id="table_dyc_v5n_rhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

Object

</td><td>

Required. An object containing the metadata configuration properties for the Fluent object or function.

</td></tr><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. Display name of the flow. The flow name should be meaningful and descriptive to easily identify its purpose.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

Description of what the flow does.

</td></tr><tr><td>

runAs

</td><td>

String

</td><td>

Determines under which user context the flow actions are run. The system user setting runs as a privileged user that bypasses role-based ACLs. The user setting runs with the privileges and roles of the user who started the flow.

 Valid values: system, user

 Default: user

</td></tr><tr><td>

runWithRoles

</td><td>

String

</td><td>

Specify the roles that the flow uses while running. For more information about running a flow with roles, see [Flow roles](https://www.servicenow.com/docs/access?context=flow-roles&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

</td></tr><tr><td>

flowPriority

</td><td>

String

</td><td>

Defines the execution priority of the flow in the Flow Engine.

 Valid values: LOW, MEDIUM, HIGH

 Default: MEDIUM

</td></tr><tr><td>

protection

</td><td>

String

</td><td>

Defines whether the flow is read-only \(read\) or editable \(empty string\).

 Valid values: read, ''

 Default: ''

</td></tr><tr><td>

access

</td><td>

String

</td><td>

Defines whether a flow is public or private.

 Valid values: public, package\_private

 Default: public

</td></tr><tr><td>

flowVariables

</td><td>

Object

</td><td>

Object defining data variables available to the flow using Column types. Use the get\_table\_schema function to fetch field definitions.

</td></tr><tr><td>

wfa.trigger

</td><td>

Function

</td><td>

Defines when to run the flow. When the trigger conditions are met, the system runs the flow using the data provided by the trigger. For more information about the wfa.trigger function, see [wfa.trigger function](fluent-flow-api.md#).

</td></tr><tr><td>

Flow body

</td><td>

Function

</td><td>

**Flow body** is an **Arrow function** in TypeScript that represents the execution steps in the flow. The Flow Body receives the **params** parameter as its input, which contains the **wfa.trigger** and **flowVariables** objects.The steps in the **Flow body** consist of these function types:

-   **wfa.action** function: Execute specific tasks and operations within a flow, such as creating records, sending emails, requesting approvals, or integrating with external systems. For more information about the wfa.action function, see [wfa.action function](fluent-flow-api.md#).
-   **wfa.flow\_logic** function: Control how flows execute, providing conditional branching, iteration, and flow structuring capabilities. For more information about wfa.flow\_logic function, see [wfa.flow\_logic function](fluent-flow-api.md#).

 You can use these parameter values in the Flow body function.

 -   **params.trigger.current**

Data type: Record. Parameter that stores the current record that started a create record, update record, or create or update record flow.

-   **params.trigger.previous**

Data type: Record. Parameter that stores the previous record values that started an update record flow.

-   **params.trigger.table\_name**

Data type: String. Parameter that stores the table name of the current record that started the flow.

-   **params.trigger.flowVariables**

Data type: Object. Parameter that stores the flow variables defined in this flow.


</td></tr></tbody>
</table>This example creates a flow that runs when an incident is created with an empty origin field value. The flow alerts managers and team members based on the incident severity.

```javascript
import { action, Flow, wfa, trigger } from '@servicenow/sdk/automation'

export const incidentSeverityAlertFlow = Flow(
    {
        $id: Now.ID['incident_severity_alert_flow'],
        name: 'Incident Severity Alert Flow',
        description: 'Alerts managers and team members based on incident severity for incidents with empty origin',
    },
    wfa.trigger(
        trigger.record.created,
        { $id: Now.ID['empty_origin_incident_trigger'] },
        {
            table: 'incident',
            condition: 'origin=NULL',
            run_flow_in: 'background',
            run_on_extended: 'false',
            run_when_setting: 'both',
            run_when_user_setting: 'any',
            run_when_user_list: [],
        }
    ),
    (params) => {
        wfa.action(
            action.core.log,
            { $id: Now.ID['log_incident_short_description'] },
            {
                log_level: 'info',
                log_message: `Incident created: ${wfa.dataPill(params.trigger.current.short_description, 'string')}`,
            }
        )

        wfa.flowLogic.if(
            {
                $id: Now.ID['check_severity_high'],
                condition: `${wfa.dataPill(params.trigger.current.severity, 'string')}=1`,
                annotation: 'High severity (1)',
            },
            () => {
                const assignmentGroup = wfa.action(
                    action.core.lookUpRecord,
                    { $id: Now.ID['lookup_assignment_group'] },
                    {
                        table: 'sys_user_group',
                        conditions: `sys_id=${wfa.dataPill(params.trigger.current.assignment_group, 'reference')}`,
                        sort_type: 'sort_asc',
                        if_multiple_records_are_found_action: 'use_first_record',
                    }
                )

                const manager = wfa.action(
                    action.core.lookUpRecord,
                    { $id: Now.ID['lookup_manager_details'] },
                    {
                        table: 'sys_user',
                        conditions: `sys_id=${wfa.dataPill(assignmentGroup.Record.manager, 'reference')}`,
                        sort_type: 'sort_asc',
                        if_multiple_records_are_found_action: 'use_first_record',
                    }
                )

                wfa.action(
                    action.core.sendNotification,
                    { $id: Now.ID['send_urgent_email_to_manager'] },
                    {
                        table_name: 'incident',
                        record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                        notification: 'high_severity_incident_manager_notification',
                    }
                )

                wfa.flowLogic.forEach(
                    wfa.dataPill(params.trigger.current.additional_assignee_list, 'array.string'),
                    { $id: Now.ID['foreach_additional_assignees_high'] },
                    () => {
                        const assignee = wfa.action(
                            action.core.lookUpRecord,
                            { $id: Now.ID['lookup_assignee_details_high'] },
                            {
                                table: 'sys_user',
                                conditions: `sys_id=${wfa.dataPill(params.trigger.current.additional_assignee_list, 'array.string')}`,
                                sort_type: 'sort_asc',
                                if_multiple_records_are_found_action: 'use_first_record',
                            }
                        )

                        wfa.action(
                            action.core.sendSms,
                            { $id: Now.ID['send_sms_to_assignee_high'] },
                            {
                                recipients: `${wfa.dataPill(assignee.Record.phone, 'string')}`,
                                message: `High severity incident: ${wfa.dataPill(params.trigger.current.short_description, 'string')}`,
                            }
                        )
                    }
                )

                wfa.action(
                    action.core.updateRecord,
                    { $id: Now.ID['update_work_notes_high'] },
                    {
                        table_name: 'incident',
                        record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                        values: TemplateValue({
                            work_notes: `Manager ${wfa.dataPill(manager.Record.name, 'string')} notified via email and team notified via SMS.`,
                        }),
                    }
                )
            }
        )

        wfa.flowLogic.elseIf(
            {
                $id: Now.ID['check_severity_medium'],
                condition: `${wfa.dataPill(params.trigger.current.severity, 'string')}=2`,
                annotation: 'Medium severity (2)',
            },
            () => {
                wfa.flowLogic.forEach(
                    wfa.dataPill(params.trigger.current.additional_assignee_list, 'array.string'),
                    { $id: Now.ID['foreach_additional_assignees_medium'] },
                    () => {
                        const assignee = wfa.action(
                            action.core.lookUpRecord,
                            { $id: Now.ID['lookup_assignee_details_medium'] },
                            {
                                table: 'sys_user',
                                conditions: `sys_id=${wfa.dataPill(params.trigger.current.additional_assignee_list, 'array.string')}`,
                                sort_type: 'sort_asc',
                                if_multiple_records_are_found_action: 'use_first_record',
                            }
                        )

                        wfa.action(
                            action.core.sendSms,
                            { $id: Now.ID['send_sms_to_assignee_medium'] },
                            {
                                recipients: `${wfa.dataPill(assignee.Record.phone, 'string')}`,
                                message: `Medium severity incident: ${wfa.dataPill(params.trigger.current.short_description, 'string')}`,
                            }
                        )
                    }
                )
            }
        )

        wfa.action(
            action.core.updateRecord,
            { $id: Now.ID['update_incident_to_in_progress'] },
            {
                table_name: 'incident',
                record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                values: TemplateValue({ state: '2' }),
            }
        )
    }
)
```

This example runs when a change request is approved and notifies the requester.

```javascript
import { action, Flow, wfa, trigger } from '@servicenow/sdk/automation'

export const changeRequestApprovalNotificationFlow = Flow(
    {
        $id: Now.ID['change_request_approval_notification_flow'],
        name: 'Change Request Approval Notification Flow',
        description: 'Sends formatted notification to requester when change request is approved',
    },
    wfa.trigger(
        trigger.record.updated,
        { $id: Now.ID['change_request_approved_trigger'] },
        {
            table: 'change_request',
            condition: 'approval=approved',
            run_flow_in: 'background',
            trigger_strategy: 'unique_changes',
            run_when_user_list: [],
            run_when_setting: 'both',
            run_on_extended: 'false',
            run_when_user_setting: 'any',
        }
    ),
    (params) => {
        const requester = wfa.action(
            action.core.lookUpRecord,
            { $id: Now.ID['lookup_requester_details'] },
            {
                table: 'sys_user',
                conditions: `sys_id=${wfa.dataPill(params.trigger.current.requested_by, 'reference')}`,
                sort_type: 'sort_asc',
                if_multiple_records_are_found_action: 'use_first_record',
            }
        )

        wfa.action(
            action.core.sendEmail,
            { $id: Now.ID['send_approval_notification_email'] },
            {
                table_name: 'change_request',
                watermark_email: true,
                ah_subject: `Change Request ${wfa.dataPill(params.trigger.current.number, 'string')} - Approved`,
                ah_body: `Your change request has been approved.`,
                record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                ah_to: wfa.dataPill(requester.Record.email, 'string'),
            }
        )

        wfa.action(
            action.core.updateRecord,
            { $id: Now.ID['update_work_notes_notification_sent'] },
            {
                table_name: 'change_request',
                record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                values: TemplateValue({
                    work_notes: `Approval notification sent to ${wfa.dataPill(requester.Record.name, 'string')} (${wfa.dataPill(requester.Record.email, 'string')})`,
                }),
            }
        )
    }
)
```

## Subflow object

Create a subflow \[sys\_hub\_flow\] to run a reusbale sequence of actions and flow logic when called by a flow or API.

Subflows run when called by a flow or an API. Use subflows for on-demand automation that can be called by multiple flows.

Subflows consist of these components.

-   One configuration object that defines the subflow configuration properties.
    -   Zero or one inputs object that defines subflow inputs.
    -   Zero or one outputs object that defines subflow outputs.
    -   Zero or one flow variables object that defines flow variables.
-   One Body function that defines what actions, flow logic, and subflows to run.
    -   Zero or more wfa.action functions
    -   Zero or more wfa.flow\_logic functions

<table id="table_ozc_zd4_rhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

Object

</td><td>

Required. An object containing the metadata configuration properties for the Fluent object or function.

</td></tr><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

name

</td><td>

String

</td><td>

Required. Display name of the subflow. The subflow name should be meaningful and descriptive to easily identify its purpose. This property is part of the Subflow configuration object.

</td></tr><tr><td>

description

</td><td>

String

</td><td>

Description of what the flow does. This property is part of the Subflow configuration object.

</td></tr><tr><td>

runAs

</td><td>

String

</td><td>

Determines under which user context the subflow actions are executed.

 Valid values: system, user

 Default: user

 This property is part of the Subflow configuration object.

</td></tr><tr><td>

runWithRoles

</td><td>

Array

</td><td>

Specify the roles that the subflow uses while running. This property is part of the Subflow configuration object.

</td></tr><tr><td>

flowPriority

</td><td>

String

</td><td>

Defines the execution priority of the subflow in the Flow Engine.

 Valid values: LOW, MEDIUM, HIGH

 Default: Medium

 This property is part of the Subflow configuration object.

</td></tr><tr><td>

protection

</td><td>

String

</td><td>

Defines whether the subflow is read-only \(read\) or editable \(empty string\).

 Valid values: read, ' '

 This property is part of the Subflow configuration object.

</td></tr><tr><td>

access

</td><td>

String

</td><td>

Defines the visibility/accessibility of the subflow to other subflow authors.

 Valid values: public, package\_private

 Default: public

 This property is part of the Subflow configuration object.

</td></tr><tr><td>

category

</td><td>

String

</td><td>

Category for organizing the subflow. This property is part of the Subflow configuration object.

</td></tr><tr><td>

inputs

</td><td>

Object

</td><td>

Object defining input parameters using Column types. This property is part of the Subflow configuration object.

</td></tr><tr><td>

outputs

</td><td>

Object

</td><td>

Object defining output parameters using Column types. This property is part of the Subflow configuration object.

</td></tr><tr><td>

flowVariables

</td><td>

Object

</td><td>

Object defining data variables available to the subflow using Column types. This property is part of the Subflow configuration object.

</td></tr><tr><td>

Flow body

</td><td>

Function

</td><td>

**Flow body** is an **Arrow function** in TypeScript that represents the execution steps in the flow. The Flow Body receives the **\_params** parameter as its input, which contains the **inputs** and **flowVariables** objects.The steps in the **Flow body** consist of these function types:

-   **wfa.action** function: Execute specific tasks and operations within a flow, such as creating records, sending emails, requesting approvals, or integrating with external systems. For more information about the wfa.action function, see [wfa.action function](fluent-flow-api.md#).
-   **wfa.flow\_logic** function: Control how flows execute, providing conditional branching, iteration, and flow structuring capabilities. For more information about wfa.flow\_logic function, see [wfa.flow\_logic function](fluent-flow-api.md#).

 You can use these parameter values in the Flow body function.

 -   **\_params.trigger.current**

Data type: Record. Parameter that stores the current record that started a create record, update record, or create or update record flow.

-   **\_params.trigger.previous**

Data type: Record. Parameter that stores the previous record values that started an update record flow.

-   **\_params.trigger.table\_name**

Data type: String. Parameter that stores the table name of the current record that started the flow.

-   **\_params.trigger.flowVariables**

Data type: Object. Parameter that stores the flow variables defined in this flow.


</td></tr></tbody>
</table>This example uses a new user's name and office location to look up a User record, send a welcome notification, and look up an unassigned hardware asset and an available office location. If there is an available laptop asset and office location, then each are assigned to the new user.

```javascript
import { Subflow, action, wfa } from '@servicenow/sdk/automation'
import { BooleanColumn, ReferenceColumn, StringColumn } from '@servicenow/sdk/core'

export const newUserOnboardingSubflow = Subflow(
    {
        $id: Now.ID['new_user_onboarding_subflow'],
        name: 'New User Onboarding Subflow',
        description: 'Sends welcome notification, assigns laptop and desk, returns assignment results',
        inputs: {
            user_sys_id: ReferenceColumn({
                label: 'User',
                referenceTable: 'sys_user',
                mandatory: true,
            }),
            office_location: ReferenceColumn({
                label: 'Office Location',
                referenceTable: 'cmn_location',
                mandatory: true,
            }),
        },
        outputs: {
            laptop_assigned: BooleanColumn({ label: 'Laptop Assigned' }),
            desk_assigned: BooleanColumn({ label: 'Desk Assigned' }),
            laptop_number: StringColumn({ label: 'Laptop Asset Number', maxLength: 40 }),
            desk_number: StringColumn({ label: 'Desk Asset Number', maxLength: 40 }),
        },
        flowVariables: {
            laptop_found: BooleanColumn({ label: 'Laptop Found Flag', default: false }),
            desk_found: BooleanColumn({ label: 'Desk Found Flag', default: false }),
        },
    },
    (params) => {
        const user = wfa.action(
            action.core.lookUpRecord,
            { $id: Now.ID['lookup_user'] },
            {
                table: 'sys_user',
                conditions: `sys_id=${wfa.dataPill(params.inputs.user_sys_id, 'reference')}`,
                sort_type: 'sort_asc',
                if_multiple_records_are_found_action: 'use_first_record',
            }
        )

        wfa.action(
            action.core.sendNotification,
            { $id: Now.ID['send_welcome_notification'] },
            {
                table_name: 'sys_user',
                record: wfa.dataPill(params.inputs.user_sys_id, 'reference'),
                notification: 'new_user_welcome_notification',
            }
        )

        const availableLaptop = wfa.action(
            action.core.lookUpRecord,
            { $id: Now.ID['lookup_available_laptop'] },
            {
                table: 'alm_hardware',
                conditions: 'assigned_to=NULL^install_status=1^substatus=available',
                sort_type: 'sort_asc',
                if_multiple_records_are_found_action: 'use_first_record',
            }
        )

        wfa.flowLogic.if(
            {
                $id: Now.ID['check_laptop_available'],
                condition: `${wfa.dataPill(availableLaptop.Record.sys_id, 'reference')}!=NULL`,
                annotation: 'Available laptop found',
            },
            () => {
                wfa.action(
                    action.core.updateRecord,
                    { $id: Now.ID['assign_laptop'] },
                    {
                        table_name: 'alm_hardware',
                        record: wfa.dataPill(availableLaptop.Record.sys_id, 'reference'),
                        values: TemplateValue({
                            assigned_to: wfa.dataPill(params.inputs.user_sys_id, 'reference'),
                            install_status: '2',
                            substatus: 'in_use',
                        }),
                    }
                )
            }
        )

        wfa.flowLogic.else(
            { $id: Now.ID['no_laptop_available'] },
            () => {
                wfa.action(
                    action.core.log,
                    { $id: Now.ID['log_no_laptop'] },
                    {
                        log_level: 'warn',
                        log_message: `No available laptop found for ${wfa.dataPill(user.Record.name, 'string')} — manual assignment required.`,
                    }
                )
            }
        )

        const availableDesk = wfa.action(
            action.core.lookUpRecord,
            { $id: Now.ID['lookup_available_desk'] },
            {
                table: 'alm_asset',
                conditions: `assigned_to=NULL^location=${wfa.dataPill(params.inputs.office_location, 'reference')}^install_status=1^substatus=available`,
                sort_type: 'sort_asc',
                if_multiple_records_are_found_action: 'use_first_record',
            }
        )

        wfa.flowLogic.if(
            {
                $id: Now.ID['check_desk_available'],
                condition: `${wfa.dataPill(availableDesk.Record.sys_id, 'reference')}!=NULL`,
                annotation: 'Available desk found at office location',
            },
            () => {
                wfa.action(
                    action.core.updateRecord,
                    { $id: Now.ID['assign_desk'] },
                    {
                        table_name: 'alm_asset',
                        record: wfa.dataPill(availableDesk.Record.sys_id, 'reference'),
                        values: TemplateValue({
                            assigned_to: wfa.dataPill(params.inputs.user_sys_id, 'reference'),
                            install_status: '2',
                            substatus: 'in_use',
                        }),
                    }
                )
            }
        )

        wfa.flowLogic.else(
            { $id: Now.ID['no_desk_available'] },
            () => {
                wfa.action(
                    action.core.log,
                    { $id: Now.ID['log_no_desk'] },
                    {
                        log_level: 'warn',
                        log_message: `No available desk at office location for ${wfa.dataPill(user.Record.name, 'string')} — manual assignment required.`,
                    }
                )
            }
        )

        wfa.action(
            action.core.sendNotification,
            { $id: Now.ID['send_onboarding_complete'] },
            {
                table_name: 'sys_user',
                record: wfa.dataPill(params.inputs.user_sys_id, 'reference'),
                notification: 'user_onboarding_complete_notification',
            }
        )

        wfa.flowLogic.assignSubflowOutputs(
            {
                $id: Now.ID['assign_outputs'],
                annotation: 'Return laptop and desk assignment results',
            },
            params.outputs,
            {
                laptop_assigned: true,
                desk_assigned: true,
                laptop_number: wfa.dataPill(availableLaptop.Record.asset_tag, 'string'),
                desk_number: wfa.dataPill(availableDesk.Record.asset_tag, 'string'),
            }
        )
    }
)
```

## wfa.trigger function

Run a flow when the start conditions of a specific trigger type are met. Triggers determine when a flow runs and what data is available from the flow start conditions.

Add a wfa.trigger function to the **Flow Body** function of a Flow object.

The following types of action instances are supported:

-   trigger.record.created
-   trigger.record.updated
-   trigger.record.createdOrUpdated
-   trigger.scheduled.daily
-   trigger.scheduled.weekly
-   trigger.scheduled.monthly
-   trigger.scheduled.repeat
-   trigger.scheduled.runOnce
-   trigger.application.inboundEmail
-   trigger.application.slaTask
-   trigger.application.knowledgeManagement
-   trigger.application.remoteTableQuery

.

For more information about available actions, see [Workflow Studio flow trigger types](https://www.servicenow.com/docs/access?context=flow-triggers&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

<table id="table_tjy_23k_xhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

trigger

</td><td>

String

</td><td>

Name of the specific trigger to run. All action names use a dot notation that starts with `trigger`. For example, `trigger.record.created`, `trigger.scheduled.daily`, or `trigger.application.serviceCatalog`.

</td></tr><tr><td>

configuration

</td><td>

Object

</td><td>

Required. An object containing the metadata configuration properties for the Fluent object or function.

</td></tr><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

inputs

</td><td>

Object

</td><td>

An object containing any input parameters required by the trigger such as `table` or `condition`.

</td></tr></tbody>
</table>This example runs a flow when a high priority incident record is created.

```javascript
// Trigger definition - defines when the flow starts
wfa.trigger(
    trigger.record.created, // TriggerDefinition - record creation event
    { 
        $id: Now.ID['incident_trigger'], // string | guid, mandatory - unique identifier
        annotation: 'When high priority incident is created' // string, optional - describes trigger purpose
    },
    {
        table: 'incident', // string, mandatory - table name to monitor
        condition: 'priority=1^ORpriority=2', // string, optional - encoded query filter
        run_on_extended: 'false', // string, optional, default: 'false' - run on child tables
        run_flow_in: 'any', // string, optional, default: 'any' - 'any', 'background', or 'foreground'
        run_when_setting: 'both', // string, optional, default: 'both' - 'both', 'non_interactive', or 'interactive'
        run_when_user_list: [], // Array, optional, default: [] - need to use runQuery to get user sys_ids from sys_user table
        run_when_user_setting: 'any' // string, optional, default: 'any' - 'any', 'one_of', or 'not_one_of'
    }
)
```

This examples starts a flow daily at 9 AM.

```javascript
// ✅ CORRECT - Daily trigger at specific time
wfa.trigger(
    trigger.scheduled.daily,
    { 
        $id: Now.ID['daily_report_trigger'],
        annotation: 'Runs daily at 9 AM'
    },
    {
        time: Time({ hours: 9, minutes: 0, seconds: 0 })
    }
)
```

This examples starts a flow when there is an email reply to an incident record.

```javascript
// Trigger when email arrives for incident table
wfa.trigger(
    trigger.application.inboundEmail, // TriggerDefinition - inbound email event
    { 
        $id: Now.ID['incident_email_trigger'], // string | guid, mandatory
        annotation: 'Process emails for incident table' // string, optional
    },
    {
        target_table: 'incident', // string, optional - table for email replies/forwards
        email_conditions: '', // string, optional - filter which emails trigger the flow
        order: 100, // number, optional - execution order when multiple email triggers exist
        stop_condition_evaluation: true // boolean, optional - stop evaluating other triggers if this one matches
    }
)

// Access email data in flow body:
(_params) => {
    const emailSubject = _params.trigger.email.subject // Email subject
    const emailBody = _params.trigger.email.body // Email body
    const emailFrom = _params.trigger.email.from // Sender email address
}
```

## wfa.action function

Run a specific action instance from a flow or subflow. Actions determine what data is generated, updated, or retrieved.

Add wfa.action functions to the **Flow Body** function of a Flow or Subflow object.

The following types of action instances are supported:

-   action.core.createRecord
-   action.core.createOrUpdateRecord
-   action.core.deleteRecord
-   action.core.lookUpRecord
-   action.core.lookUpRecords
-   action.core.updateRecord
-   action.core.updateMultipleRecords
-   action.core.sendNotification
-   action.core.sendEmail
-   action.core.sendSms
-   action.core.askForApproval
-   action.core.waitForApproval
-   action.core.createTask
-   action.core.log
-   action.core.waitForCondition
-   action.core.waitForMessage
-   action.core.slaPercentageTimer

.

For more information about available actions, see [Workflow Studio actions](https://www.servicenow.com/docs/access?context=flow-actions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

<table id="table_zyb_kqj_xhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

action

</td><td>

String

</td><td>

Name of the specific action to run. All action names use a dot notation that starts with `action.core`. For example, `action.core.lookUpRecord`, `action.core.lookUpRecords`, `action.core.createRecord`, or `action.core.updateRecord`.

</td></tr><tr><td>

configuration

</td><td>

Object

</td><td>

Required. An object containing the metadata configuration properties for the Fluent object or function.

</td></tr><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

inputs

</td><td>

Object

</td><td>

An object containing any input parameters required by the action such as `table_name` or `values`.

</td></tr></tbody>
</table>This example runs when a change request is approved and notifies the requester. The flow uses the Look Up Records, Send Email, and Update Record actions.

```javascript
import { action, Flow, wfa, trigger } from '@servicenow/sdk/automation'

export const changeRequestApprovalNotificationFlow = Flow(
    {
        $id: Now.ID['change_request_approval_notification_flow'],
        name: 'Change Request Approval Notification Flow',
        description: 'Sends formatted notification to requester when change request is approved',
    },
    wfa.trigger(
        trigger.record.updated,
        { $id: Now.ID['change_request_approved_trigger'] },
        {
            table: 'change_request',
            condition: 'approval=approved',
            run_flow_in: 'background',
            trigger_strategy: 'unique_changes',
            run_when_user_list: [],
            run_when_setting: 'both',
            run_on_extended: 'false',
            run_when_user_setting: 'any',
        }
    ),
    (params) => {
        const requester = wfa.action(
            action.core.lookUpRecord,
            { $id: Now.ID['lookup_requester_details'] },
            {
                table: 'sys_user',
                conditions: `sys_id=${wfa.dataPill(params.trigger.current.requested_by, 'reference')}`,
                sort_type: 'sort_asc',
                if_multiple_records_are_found_action: 'use_first_record',
            }
        )

        wfa.action(
            action.core.sendEmail,
            { $id: Now.ID['send_approval_notification_email'] },
            {
                table_name: 'change_request',
                watermark_email: true,
                ah_subject: `Change Request ${wfa.dataPill(params.trigger.current.number, 'string')} - Approved`,
                ah_body: `Your change request has been approved.`,
                record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                ah_to: wfa.dataPill(requester.Record.email, 'string'),
            }
        )

        wfa.action(
            action.core.updateRecord,
            { $id: Now.ID['update_work_notes_notification_sent'] },
            {
                table_name: 'change_request',
                record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                values: TemplateValue({
                    work_notes: `Approval notification sent to ${wfa.dataPill(requester.Record.name, 'string')} (${wfa.dataPill(requester.Record.email, 'string')})`,
                }),
            }
        )
    }
)
```

This example runs a flow when a change request record is created or updated as high impact. The flow runs the Update Record to mark the change request as high risk, the Look Up Record to find the group with the name CAB, the Send Notification to send a high risk change notification to the CAB group, and the Log action to document both the record update and the notification sent.

```javascript
import { action, Flow, wfa, trigger } from '@servicenow/sdk/automation'

export const changeRiskTaggingFlow = Flow(
    {
        $id: Now.ID['change_risk_tagging_flow'],
        name: 'Change Risk Tagging Flow',
        description: 'Tags change requests with high-risk label when created or updated with high impact',
    },
    wfa.trigger(
        trigger.record.createdOrUpdated,
        { $id: Now.ID['change_risk_trigger'] },
        {
            table: 'change_request',
            condition: 'active=true^impact=1',
            run_flow_in: 'background',
            run_on_extended: 'false',
            run_when_setting: 'both',
            run_when_user_setting: 'any',
            run_when_user_list: [],
        }
    ),
    (params) => {
        wfa.action(
            action.core.updateRecord,
            { $id: Now.ID['tag_high_risk'] },
            {
                table_name: 'change_request',
                record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                values: TemplateValue({
                    risk: 'high',
                    work_notes: 'Automatically tagged as high-risk due to high impact.',
                }),
            }
        )

        const cab = wfa.action(
            action.core.lookUpRecord,
            { $id: Now.ID['lookup_cab_group'] },
            {
                table: 'sys_user_group',
                conditions: 'name=CAB^active=true',
                sort_type: 'sort_asc',
                if_multiple_records_are_found_action: 'use_first_record',
            }
        )

        wfa.action(
            action.core.sendNotification,
            { $id: Now.ID['notify_cab_high_risk'] },
            {
                table_name: 'change_request',
                record: wfa.dataPill(params.trigger.current.sys_id, 'reference'),
                notification: 'high_risk_change_cab_notification',
            }
        )

        wfa.action(
            action.core.log,
            { $id: Now.ID['log_risk_tagged'] },
            {
                log_level: 'warn',
                log_message: `Change ${wfa.dataPill(params.trigger.current.number, 'string')} tagged as high-risk. CAB group ${wfa.dataPill(cab.Record.name, 'string')} notified.`,
            }
        )
    }
)
```

## wfa.flow\_logic function

Run a specific flow logic instance from a flow or subflow. Flow logic determines how and when data is used.

Add wfa.flow\_logic functions to the **Flow Body** function of a Flow or Subflow object.

The following types of flow logic instances are supported:

-   if
-   elseIf
-   else
-   forEach
-   waitForADuration
-   exitLoop, endFlow, skipIteration, setFlowVariables, and assignSubflowOutputs

.

For more information about available flow logic, see [Workflow Studio flow logic](https://www.servicenow.com/docs/access?context=flow-logic&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

<table id="table_nbq_m5j_xhc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

Object

</td><td>

Required. An object containing the metadata configuration properties for the Fluent object or function.

</td></tr><tr><td>

$id

</td><td>

String or Number

</td><td>

Required. A unique ID for the metadata object. When you build the application, this ID is hashed into a unique sys\_id. For more information, see [ServiceNow Fluent language constructs](fluent-constructs.md).Format: `Now.ID['String' or Number]`

</td></tr><tr><td>

annotation

</td><td>

String

</td><td>

Describe what this instance of flow logic does. For example, `annotation: 'Priority is critical'`.

</td></tr><tr><td>

condition

</td><td>

String

</td><td>

Required in a wfa.flow\_logic.if and wfa.flow\_logic.elseIf function. Data values that must be true to run this flow logic. For example, `condition: `\${_params.trigger.current.priority}=1`,`.

</td></tr><tr><td>

item

</td><td>

Array

</td><td>

Required in a wfa.flow\_logic.forEach function. An array or a collection of records to iterate over. Typically, this list of records is dynamically generated from a wfa.action function call to the action.core.lookUpRecords action. For example, a `problems.Records` array can be generated from an action.core.lookUpRecords action.```javascript
(_params) => {
    //Find all the newly created problem records for the past day
    const problems = wfa.action(
        action.core.lookUpRecords,
        {
            $id: Now.ID['daily_unassigned_new_problems_triage_flow_step1'],
            annotation: 'Find all the newly created problem records for the past day',
        },
        {
            table: 'problem',
            conditions:
                'sys_created_onONYesterday@javascript:gs.beginningOfYesterday()@javascript:gs.endOfYesterday()',
        }
    )

    //Iterate over the problems
    wfa.flow_logic.forEach(
        problems.Records, { ... }
```

</td></tr><tr><td>

label

</td><td>

String

</td><td>

Display value describing this instance of flow logic. For example, `label: 'If Priority is critical',`.

</td></tr><tr><td>

variables

</td><td>

Schema

</td><td>

Required in a wfa.flow\_logic.assignSubflowOutputs and wfa.flow\_logic.setFlowVariables function. A schema produced by the FlowVariables API that defines the data structure of the flow variables. For example, the `flowVars` schema can be generated from FlowVariables.```javascript
import { FlowVariables } from '@servicenow/sdk/automation'

// Define flow variables
const flowVars = FlowVariables({
    status: StringColumn({ label: 'Status' }),
    count: IntegerColumn({ label: 'Count' }),
    isActive: BooleanColumn({ label: 'Is Active' }),
})

// Flow body
(_params) => {
    // Set flow variables with literal values
    wfa.flow_logic.setFlowVariables(
        {
            $id: Now.ID['initialize_variables'],
            annotation: 'Initialize flow variables with default values',
        },
        _params.flowVariables, { ... }
```

**Important:** Always use `_params.flowVariables` as the argument for this property. Passing the wrong schema will cause validation errors.

</td></tr><tr><td>

Flow logic body

</td><td>

Function

</td><td>

**Flow logic body** is an **Arrow function** in TypeScript that represents the execution steps in the flow logic. The Flow Body receives the **\_params** parameter as its input, which contains the **wfa.trigger** and **flowVariables** objects. The steps in the **Flow logic body** consist of these functions calls:-   **wfa.action** function: Run a specific action instance from a flow or subflow. Actions determine what data is generated, updated, or retrieved.. For more information about the wfa.action function, see [wfa.action function](fluent-flow-api.md#).
-   **wfa.flow\_logic** function: Run a specific flow logic instance from a flow or subflow. Flow logic determines how and when data is used. For more information about the wfa.flow\_logic function, see [wfa.flow\_logic function](fluent-flow-api.md#).

</td></tr></tbody>
</table>This example shows checking for conditions in the trigger record. If the current record has a priority of 1, it assigns the record to a critical priority team. Else If the current record has a priority value of 2, it assigns the record to a high priority team. If neither condition is met, the record is assigned to a general team.

```javascript
// Flow body showing if/elseIf/else usage
(_params) => {
    wfa.flow_logic.if(
        {
            $id: Now.ID['check_critical_priority'],
            condition: `\${_params.trigger.current.priority}=1`,
            annotation: 'Priority is critical',
        },
        () => {
            wfa.action(
                action.core.updateRecord,
                { $id: Now.ID['assign_critical_team'], annotation: 'Assign to critical team' },
                { record: _params.trigger.current, table_name: 'incident', values: 'assignment_group=critical_team' }
            )
        }
    )
    wfa.flow_logic.elseIf(
        { $id: Now.ID['check_high_priority'], condition: `\${_params.trigger.current.priority}=2`, annotation: 'Priority is high' },
        () => {
            wfa.action(
                action.core.updateRecord,
                { $id: Now.ID['assign_high_team'], annotation: 'Assign to high team' },
                { record: _params.trigger.current, table_name: 'incident', values: 'assignment_group=high_team' }
            )
        }
    )
    wfa.flow_logic.else(
        { $id: Now.ID['assign_default'], annotation: 'Default assignment' },
        () => {
            wfa.action(
                action.core.updateRecord,
                { $id: Now.ID['assign_general_team'], annotation: 'Assign to general team' },
                { record: _params.trigger.current, table_name: 'incident', values: 'assignment_group=general_team' }
            )
        }
    )
}
```

This example iterates through a list of problem records to find unassigned records, assign them to a problem triage group, and send an email to the group.

```javascript
// Flow body showing forEach usage with lookUpRecords
(_params) => {
    //Find all the newly created problem records for the past day
    const problems = wfa.action(
        action.core.lookUpRecords,
        {
            $id: Now.ID['daily_unassigned_new_problems_triage_flow_step1'],
            annotation: 'Find all the newly created problem records for the past day',
        },
        {
            table: 'problem',
            conditions:
                'sys_created_onONYesterday@javascript:gs.beginningOfYesterday()@javascript:gs.endOfYesterday()',
        }
    )

    //Iterate over the problems
    wfa.flow_logic.forEach(
        problems.Records,
        { $id: Now.ID['daily_unassigned_new_problems_triage_flow_step2'], annotation: 'Iterate each problem' },
        (item) => {
            //Check if the problem is not assigned
            wfa.flow_logic.if(
                {
                    $id: Now.ID['daily_unassigned_new_problems_triage_flow_step3'],
                    condition: `\${item.assignment_group}ISEMPTY`,
                    annotation: 'Check if problem is not assigned',
                },
                () => {
                    wfa.action(
                        action.core.updateRecord,
                        {
                            $id: Now.ID['daily_unassigned_new_problems_triage_flow_step4'],
                            annotation: 'Update the problem record state',
                        },
                        { table_name: 'problem', record: item, values: 'state=1' }
                    )

                    //Send notification to the group
                    wfa.action(
                        action.core.sendNotification,
                        {
                            $id: Now.ID['daily_unassigned_new_problems_triage_flow_step5'],
                            annotation: 'Send notification to the group',
                        },
                        {
                            table_name: 'problem',
                            record: item,
                            notification: '',
                        }
                    )
                }
            )
        }
    )
}
```

This example sets flow variables to dynamic values stored in data pills.

```javascript
import { FlowVariables } from '@servicenow/sdk/automation'

const flowVars = FlowVariables({
    incidentPriority: IntegerColumn({ label: 'Incident Priority' }),
    assignedGroup: StringColumn({ label: 'Assigned Group' }),
    threshold: IntegerColumn({ label: 'Threshold' }),
    actionResult: StringColumn({ label: 'Action Result' }),
})

(_params) => {
    // Lookup action result
    const lookupResult = wfa.action(
        action.core.lookUpRecord,
        { $id: Now.ID['lookup_config'], annotation: 'Get configuration' },
        { table: 'sys_properties', conditions: 'name=incident.threshold' }
    )

    // Set flow variables using datapills from trigger, action outputs, and other flow variables
    wfa.flow_logic.setFlowVariables(
        {
            $id: Now.ID['set_variables_with_datapills'],
            annotation: 'Set variables from trigger and action outputs',
        },
        _params.flowVariables,
        {
            incidentPriority: _params.trigger.current.priority,        // Trigger datapill
            assignedGroup: _params.trigger.current.assignment_group,   // Trigger datapill
            threshold: lookupResult.Record.value,                      // Action output datapill
            actionResult: _params.flowVariables.status,                // Flow variable datapill
        }
    )
}
```

This exampe assign subflow Outputs using flow variables.

```javascript
// Flow body showing assignSubflowOutputs usage with flow variables
import { FlowVariables } from '@servicenow/sdk/automation'

const flowVars = FlowVariables({
    userEmail: StringColumn({ label: 'User Email' }),
    userName: StringColumn({ label: 'User Name' }),
    isApproved: BooleanColumn({ label: 'Is Approved' }),
})

(_params) => {
    // Call a subflow that returns user information
    const subflowResult = wfa.subflow(
        userInfoSubflow,
        { $id: Now.ID['get_user_info'], annotation: 'Get user information' },
        { userId: _params.trigger.current.caller_id }
    )

    // Assign subflow outputs to flow variables in one operation
    wfa.flow_logic.assignSubflowOutputs(
        { $id: Now.ID['assign_outputs'], annotation: 'Assign user info to flow variables' },
        flowVars,
        {
            userEmail: subflowResult.email,
            userName: subflowResult.name,
            isApproved: subflowResult.approved,
        }
    )

    // Now flow variables can be used throughout the flow
    // Access via _params.flowVariables.userEmail, etc.
}
```

## wfa.dataPill function

Reference a specific runtime data pill value from an action or flow logic input.

Add wfa.dataPill functions to the input parameters of a action or flow\_logic function. Define a constant for each data pill you want to use. Typically, this constant stores the output of a wfa.action or wfa.flow\_logic function.

<table id="table_lhb_y5m_k3c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

expression

</td><td>

String

</td><td id="fluent-object-entry">

Required. Dot notation reference to the runtime data that you want use as an input value. Commonly used runtime values include trigger data, action outputs, and subflow outputs.-   **Trigger record data**

Field values from a trigger record. For example, \_params.trigger.current.fieldName.

-   **Trigger record table**

Table name of the trigger record. For example, \_params.trigger.table\_name.

-   **Action output values**

Output values from previously run actions. For example, actionResult.fieldName

-   **Subflow output values**

Output values from previously run subflows. For example, subflowResult.fieldName


</td></tr><tr><td>

Type

</td><td>

String

</td><td>

Required. Data type of the data such as string, boolean, integer, or reference. For a list of available field data types, see [Field types](https://www.servicenow.com/docs/access?context=r_FieldTypes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>This example uses an unbound email record to create either an incident or a task based on the values of the inbound email. This example uses the params object to refer to data in the trigger. This example also defines the constants sender, senderManager, p3Incident, and attachments to store the output of actions and flow logic for use in later wfa.dataPill functions.

```javascript
import { action, Flow, wfa, trigger } from '@servicenow/sdk/automation'

export const emailIncidentTaskFlow = Flow(
    {
        $id: Now.ID['email_incident_task_flow'],
        name: 'Email Incident/Task Creation Flow',
        description: 'Creates incidents or tasks based on email content with "raise incident or task" in subject',
    },
    wfa.trigger(
        trigger.application.inboundEmail,
        { $id: Now.ID['inbound_email_trigger'] },
        {
            email_conditions: 'subjectLIKEraise incident or task',
            target_table: 'incident',
        }
    ),
    (params) => {
        wfa.action(
            action.core.log,
            { $id: Now.ID['log_email_received'] },
            {
                log_level: 'info',
                log_message: `Email received from: ${wfa.dataPill(params.trigger.from_address, 'string')}, Subject: ${wfa.dataPill(params.trigger.subject, 'string')}`,
            }
        )

        const sender = wfa.action(
            action.core.lookUpRecord,
            { $id: Now.ID['lookup_sender'] },
            {
                table: 'sys_user',
                conditions: `email=${wfa.dataPill(params.trigger.from_address, 'string')}`,
                sort_type: 'sort_asc',
                if_multiple_records_are_found_action: 'use_first_record',
            }
        )

        // Internal P1 path — two tasks
        wfa.flowLogic.if(
            {
                $id: Now.ID['check_internal_p1'],
                condition: `${wfa.dataPill(sender.Record.email, 'string')}LIKEservicenow^${wfa.dataPill(params.trigger.subject, 'string')}LIKEP1`,
                annotation: 'Internal sender with P1 subject',
            },
            () => {
                const senderManager = wfa.action(
                    action.core.lookUpRecord,
                    { $id: Now.ID['lookup_sender_manager'] },
                    {
                        table: 'sys_user',
                        conditions: `sys_id=${wfa.dataPill(sender.Record.manager, 'reference')}`,
                        sort_type: 'sort_asc',
                        if_multiple_records_are_found_action: 'use_first_record',
                    }
                )

                wfa.action(
                    action.core.createTask,
                    { $id: Now.ID['task_for_manager'] },
                    {
                        task_table: 'incident',
                        field_values: TemplateValue({
                            priority: 1,
                            assigned_to: wfa.dataPill(senderManager.Record.sys_id, 'reference'),
                            short_description: wfa.dataPill(params.trigger.inbound_email.body, 'reference'),
                            urgency: 1,
                            impact: 1,
                        }),
                    }
                )

                wfa.action(
                    action.core.createTask,
                    { $id: Now.ID['task_for_sender'] },
                    {
                        task_table: 'incident',
                        field_values: TemplateValue({
                            priority: 1,
                            assigned_to: wfa.dataPill(sender.Record.sys_id, 'reference'),
                            short_description: wfa.dataPill(params.trigger.subject, 'string'),
                            urgency: 1,
                            impact: 1,
                        }),
                    }
                )
            }
        )

        // External / non-P1 path — P3 incident + copy attachments
        wfa.flowLogic.else({ $id: Now.ID['create_p3_incident_branch'] }, () => {
            const p3Incident = wfa.action(
                action.core.createRecord,
                { $id: Now.ID['create_p3_incident'] },
                {
                    table_name: 'incident',
                    values: TemplateValue({
                        priority: 4,
                        short_description: wfa.dataPill(params.trigger.subject, 'string'),
                        description: `From: ${wfa.dataPill(params.trigger.from_address, 'string')}\n\n${wfa.dataPill(params.trigger.inbound_email.body, 'reference')}`,
                        contact_type: 'email',
                        caller_id: wfa.dataPill(sender.Record.sys_id, 'reference'),
                    }),
                }
            )

            const attachments = wfa.action(
                action.core.getAttachmentsOnRecord,
                { $id: Now.ID['get_email_attachments'] },
                { source_record: wfa.dataPill(params.trigger.inbound_email.sys_id, 'reference') }
            )

            wfa.flowLogic.forEach(
                wfa.dataPill(attachments.parameter, 'records'),
                { $id: Now.ID['copy_attachments_loop'] },
                () => {
                    wfa.action(
                        action.core.copyAttachment,
                        { $id: Now.ID['copy_attachment'] },
                        {
                            target_record: wfa.dataPill(p3Incident.record, 'reference'),
                            attachment_record: wfa.dataPill(attachments.parameter, 'records'),
                            table: 'incident',
                        }
                    )
                }
            )

            wfa.action(
                action.core.sendEmail,
                { $id: Now.ID['confirm_p3_email'] },
                {
                    table_name: 'incident',
                    ah_to: wfa.dataPill(params.trigger.from_address, 'string'),
                    ah_subject: `Incident Created: ${wfa.dataPill(params.trigger.subject, 'string')}`,
                    ah_body: `Your request has been received and a P3 incident has been created. Our team will be in touch shortly.`,
                    record: wfa.dataPill(p3Incident.record, 'reference'),
                }
            )
        })
    }
)
```


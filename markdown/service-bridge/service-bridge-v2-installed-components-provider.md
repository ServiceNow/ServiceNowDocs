---
title: Components installed with Service Exchange for Providers
description: Several types of components are installed when you activate the Service Exchange for Providers application, including tables, user roles, and business rules.
locale: en-US
release: yokohama
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 11
breadcrumb: [Service Exchange reference, Service Exchange]
---

# Components installed with Service Exchange for Providers

Several types of components are installed when you activate the Service Exchange for Providers application, including tables, user roles, and business rules.

The Application Files \[sys\_metadata\] table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Roles installed

The following roles are installed with the Service Exchange for Providers application.

<table id="table_gtr_pw3_bmb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service Exchange requester \[sn\_sb.requestor\]

</td><td>

-   Enables members of the customer IT staff to request and monitor services from the provider from their service catalog.

**Note:** Any member of the customer's staff who needs access to the provider's remote record producers requires this role.

-   Provides access to the remote record producers and provider tasks.

</td><td>

N/A

</td></tr><tr><td>

Service Exchange read \[sn\_sb.read\]

</td><td>

-   Enables the provider's customer service agents to read the contents of the provider task record.
-   Provides read-only access to the Service Exchange application.

</td><td>

N/A

</td></tr><tr><td>

Service Exchange admin \[sn\_sb.admin\]

</td><td>

-   Typically assigned to an administrator for the Service Exchange applications on both the customer and the provider side.
-   Provides read access to all Service Exchange tables

</td><td>

-   sn\_sb.requestor
-   sn\_sb.remote\_task\_creator
-   sn\_sb.read
-   flow\_designer
-   sn\_customerservice.case\_viewer
-   sn\_customerservice.customer\_data\_viewer
-   catalog

</td></tr></tbody>
</table>## Business rules installed

The following business rules are installed with the Service Exchange for Providers application.

<table id="table_ejs_r4p_gzb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Abort duplicate remote task insert

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Aborts insert of remote task if it already exists.

</td></tr><tr><td>

Abort if duplicate transform is found

</td><td>

sn\_sb\_pro\_transform

</td><td>

Aborts insert or update of transform if duplicate found.

</td></tr><tr><td>

Abort if duplicate URL

</td><td>

sn\_sb\_pro\_consumer\_

 connection

</td><td>

Aborts insert of consumer connection if duplicate URL already exists.

</td></tr><tr><td>

Abort if field name already in use

</td><td>

sn\_sb\_pro\_inbound\_field

</td><td>

Aborts insert of inbound field if name is a duplicate.

</td></tr><tr><td>

Abort if field name already in use

</td><td>

sn\_sb\_pro.outbound\_field

</td><td>

Aborts insert of outbound field if name is a duplicate.

</td></tr><tr><td>

Abort if remote task def is not editable

</td><td>

sn\_sb\_pro\_remote\_task\_

 def\_customer\_criteria

</td><td>

Blocks creating or editing consumer criteria if associated remote task def is not in an editable state.

</td></tr><tr><td>

Abort if remote task def is not editable

</td><td>

sn\_sb\_pro\_inbound\_field

</td><td>

Blocks insert of inbound fields if associated remote task definition is not in an editable state.

</td></tr><tr><td>

Abort if remote task def is not editable

</td><td>

sn\_sb\_pro\_outbound\_field

</td><td>

Blocks insert of outbound fields if associated remote task definition is not in an editable state.

</td></tr><tr><td>

Abort publish if duplicate record

</td><td>

sn\_sb\_pro\_remote\_task\_def

</td><td>

Blocks publishing of remote task definition if is a duplicate record.

</td></tr><tr><td>

Abort Remote Task Create If Missing Conn

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Sets connection on remote task if present, or aborts insert if none found.

</td></tr><tr><td>

Abort remote task def delete by provider

</td><td>

sn\_sb\_pro\_remote\_task\_def

</td><td>

Prevents remote task definition deletion if definition is not in retired state.

</td></tr><tr><td>

Add cat\_item name to g\_scratchpad

</td><td>

item\_option\_new

</td><td>

Adds the catalog item name to the scratchpad on display.

</td></tr><tr><td>

Add consumer connection data to session

</td><td>

sn\_sb\_pro\_consumer\_

 connection

</td><td>

Adds consumer connection data to session data.

</td></tr><tr><td>

Approve approval record

</td><td>

sn\_sb\_pro\_provider\_task

</td><td>

Handles record approvals through provider tasks.

</td></tr><tr><td>

Assure deletable

</td><td>

sn\_sb\_pro\_remote\_

 choice\_definition

</td><td>

Checks that a remote task definition is deletable.

</td></tr><tr><td>

Assure persona name uniqueness

</td><td>

sn\_sb\_pro\_persona

</td><td>

Prevents persona records being created with same name.

</td></tr><tr><td>

Assure unique and updatable

</td><td>

sn\_sb\_pro\_remote\_choice\_

 definition

</td><td>

Ensures that only unique remote task definitions are inserted or updated.

</td></tr><tr><td>

Assure uniqueness of criteria for RRP

</td><td>

sn\_sb\_pro\_remote\_record\_

 producer\_consumer\_criteria

</td><td>

Ensures the criteria added to a remote record producer is unique.

</td></tr><tr><td>

Clear remote task client data

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Clears session data for remote task transactions.

</td></tr><tr><td>

Copy attachment from Provider Task

</td><td>

sys\_attachment

</td><td>

Copies attachments from synced provider tasks to parent task.

</td></tr><tr><td>

Copy attachment to Provider Task

</td><td>

sys\_attachment

</td><td>

Copies attachments from parent task to provider tasks.

</td></tr><tr><td>

Create default user criteria on Insert

</td><td>

sn\_sb\_pro\_remote\_

 record\_producer

</td><td>

Creates default user criteria on insert of remote record producer.

</td></tr><tr><td>

Create or Update transport connection

</td><td>

sn\_sb\_pro\_consumer\_

 connection

</td><td>

Manages transport connection on connection changes.

</td></tr><tr><td>

Create parent on synced remote task

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Creates parent task on synced remote task insert.

</td></tr><tr><td>

Delete associated criteria record

</td><td>

sn\_sb\_pro\_remote\_task\_def

</td><td>

Deletes associated criteria records on delete of a remote task definition.

</td></tr><tr><td>

Delete associated records

</td><td>

sn\_sb\_pro\_remote\_task\_def

</td><td>

Deletes inbound and outbound mapping records associated with remote task definition.

</td></tr><tr><td>

Disconnect RT when RTD Deleted

</td><td>

sn\_sb\_pro\_remote\_task\_def

</td><td>

Disconnects all associated remote tasks when a remote task definition is deleted.

</td></tr><tr><td>

Display Scope mismatch warning

</td><td>

Item\_option\_new

</td><td>

Shows warning on variable records when in incorrect scope.

</td></tr><tr><td>

Error RT when Parent Deleted

</td><td>

task

</td><td>

When a parent task is deleted, all associated remote tasks status is set to the Error state.

</td></tr><tr><td>

Force RRP to Draft State on Edits

</td><td>

catalog\_ui\_policy\_action

</td><td>

Sets remote record producer state to Draft when associated records are edited.

</td></tr><tr><td>

Force RRP to Draft State on Edits

</td><td>

sys\_attachment

</td><td>

Sets remote record producer state to Draft when associated records are edited.

</td></tr><tr><td>

Force RRP to Draft State on Edits

</td><td>

catalog\_ui\_policy

</td><td>

Sets remote record producer state to Draft when associated records are edited.

</td></tr><tr><td>

Force RRP to Draft State on Edits

</td><td>

question\_choice

</td><td>

Sets remote record producer state to Draft when associated records are edited.

</td></tr><tr><td>

Force RRP to Draft State on Edits

</td><td>

item\_option\_new

</td><td>

Sets remote record producer State to Draft when associated records are edited.

</td></tr><tr><td>

Force Updates to Update Sets

</td><td>

item\_option\_new

</td><td>

Forces update sets to update on record edits.

</td></tr><tr><td>

Force Updates to Update Sets

</td><td>

catalog\_ui\_policy

</td><td>

Forces update sets to update on record edits.

</td></tr><tr><td>

Force Updates to Update Sets

</td><td>

catalog\_ui\_policy\_action

</td><td>

Forces update sets to update on record edits.

</td></tr><tr><td>

Force Updates to Update Sets

</td><td>

question\_choice

</td><td>

Forces update sets to update on record edits.

</td></tr><tr><td>

Gen entitlements for publish/retire RRP

</td><td>

sn\_sb\_pro\_remote\_

 record\_producer

</td><td>

Generates entitlements for remote record producers that are published or retired.

</td></tr><tr><td>

Gen entitlements for update Persona

</td><td>

sn\_sb\_pro\_persona

</td><td>

Generates entitlements for personas when edited.

</td></tr><tr><td>

Generate entitlements for remote task def

</td><td>

sn\_sb\_pro\_remote\_

 task\_def

</td><td>

Generates entitlements for remote task definition changes.

</td></tr><tr><td>

Handle authorized user transport

</td><td>

sn\_sb\_pro\_authorized\_user

</td><td>

Manages transmission of authorized user changes through the transport layer.

</td></tr><tr><td>

Limit registration tasks by Company and URL

</td><td>

sn\_sb\_pro\_registration

</td><td>

Controls registration tasks by company and URL.

</td></tr><tr><td>

Populate customer details on provider

</td><td>

sn\_sb\_pro\_provider\_task

</td><td>

Populates inserted provider task information from consumer connection.

</td></tr><tr><td>

Populate scratchpad

</td><td>

sn\_sb\_pro\_registration

</td><td>

Populates scratchpad with relevant information on registration.

</td></tr><tr><td>

Propagate Service Exchange Version Changes

</td><td>

v\_plugin

</td><td>

Adds Service Exchange version changes on settings record.

</td></tr><tr><td>

Reject approval record

</td><td>

sn\_sb\_pro\_provider\_task

</td><td>

Handles rejection through provider tasks.

</td></tr><tr><td>

Remote Choice: Update attributes field

</td><td>

item\_option\_new

</td><td>

Updates Attributes field on remote choice for variable changes.

</td></tr><tr><td>

Reset Consumer table on mappings

</td><td>

sn\_sb\_pro\_remote\_

 task\_def

</td><td>

Resets the consumer table field on mappings associated with remote task definition when consumer table mappings change.

</td></tr><tr><td>

Reset Provider table on mappings

</td><td>

sn\_sb\_pro\_remote\_

 task\_def

</td><td>

Resets the provider table field on mappings associated with remote task definition on definition provider table change.

</td></tr><tr><td>

Restrict RRP variable types

</td><td>

item\_option\_new

</td><td>

Restricts the types of variables allowed when associated with a remote task definition.

</td></tr><tr><td>

Retry Errored RT on RTD Activation

</td><td>

sn\_sb\_pro\_remote\_

 task\_def

</td><td>

Retry parent creation for remote tasks if associated remote task definition is activated and remote task parent is null.

</td></tr><tr><td>

Send auto approval

</td><td>

sn\_sb\_pro\_authorized\_user

</td><td>

Manages automatic approvals of authorized users.

</td></tr><tr><td>

Service Exchange bootstrap

</td><td>

sn\_sb\_pro\_registration

</td><td>

Helps manage onboarding for Service Exchange.

</td></tr><tr><td>

Set company on remote task insert

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Sets the company \(and account if present\) on remote tasks on insert through sync.

</td></tr><tr><td>

Set copied RRP state to default

</td><td>

sn\_sb\_pro\_remote\_

 record\_producer

</td><td>

Manages setting remote record producer state when copied.

</td></tr><tr><td>

Set default values

</td><td>

sn\_sb\_pro\_authorized\_user

</td><td>

Sets default values on authorized users on insert.

</td></tr><tr><td>

Set outbound vars json on insert

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Sets the outbound vars json field on remote task insert by current instance.

</td></tr><tr><td>

Set Provider task number

</td><td>

sn\_sb\_pro\_provider\_task

</td><td>

Sets the provider task number to synced provider task number.

</td></tr><tr><td>

Set Remote task number

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Sets remote task number on synced remote task number.

</td></tr><tr><td>

Show warning messages

</td><td>

sn\_sb\_pro\_remote\_

 record\_producer

</td><td>

Shows warning messages for remote record producer errors.

</td></tr><tr><td>

Show warning on incomplete Remote Task Definition

</td><td>

sn\_sb\_pro\_remote\_task\_def

</td><td>

Shows warnings on remote task definition if required related records are missing.

</td></tr><tr><td>

Sync Attachment from Parent Task

</td><td>

sys\_attachment

</td><td>

Syncs attachments from parent tasks to associated remote tasks.

</td></tr><tr><td>

Sync comments from provider task

</td><td>

sys\_journal\_field

</td><td>

Syncs comments from synced provider tasks to parent task.

</td></tr><tr><td>

Sync Remote Task Attachment to Parent

</td><td>

sys\_attachment

</td><td>

Copies synced remote task attachments to parent task.

</td></tr><tr><td>

Trigger changed attachment transport

</td><td>

sys\_attachment

</td><td>

Handles attachment changes syncing through the transport layer.

</td></tr><tr><td>

Trigger entitlement transport

</td><td>

sn\_sb\_pro\_entitlement

</td><td>

Manages entitlements syncing through transport layer

</td></tr><tr><td>

Trigger inserted attachment transport

</td><td>

sys\_attachment

</td><td>

Manages attachment insert syncing through the transport layer.

</td></tr><tr><td>

Trigger provider PT transport

</td><td>

sn\_sb\_pro\_provider\_task

</td><td>

Manages provider task syncing through the transport layer.

</td></tr><tr><td>

Trigger provider remote task transport

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Manages remote task insert and delete syncing through the transport layer.

</td></tr><tr><td>

Trigger remote task transport update

</td><td>

sn\_sb\_pro\_remote\_task

</td><td>

Manages remote task update syncing through the transport layer.

</td></tr><tr><td>

Trigger SBScratchpad Transport

</td><td>

sn\_sb\_scratchpad

</td><td>

Manages scratchpad update syncing through the transport layer.

</td></tr><tr><td>

Trigger settings transport

</td><td>

sn\_sb\_pro\_service\_bridge\_

 settings

</td><td>

Manages Service Exchange setting syncing through the transport layer.

</td></tr><tr><td>

Update comments from Task to PT

</td><td>

task

</td><td>

Handles syncing of comments from parent task to provider task.

</td></tr><tr><td>

Update consumer registration

</td><td>

sn\_sb\_pro\_service\_bridge\_

 settings

</td><td>

Updates consumer registration on insert of settings record.

</td></tr><tr><td>

Update Persona RRPs on Change

</td><td>

sn\_sb\_pro\_persona

</td><td>

Updates remote record producer persona when modified.

</td></tr><tr><td>

Validate Authorized Users Field Values

</td><td>

sn\_sb\_pro\_service\_bridge\_

 settings

</td><td>

Validates authorized users field values when updated.

</td></tr><tr><td>

Validate max authorized user

</td><td>

sn\_sb\_pro\_service\_bridge\_

 settings

</td><td>

Ensures max authorized user number is within valid range.

</td></tr><tr><td>

Validate Provider task

</td><td>

sn\_sb\_pro\_provider\_task

</td><td>

Validates a provider task insert or update is allowed.

</td></tr></tbody>
</table>## Tables installed

The following tables are installed with the Service Exchange for Providers application.

<table id="table_hnb_j13_bme"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authorized Users \[sn\_sb\_pro\_authorized\_user\]

</td><td>

Contains the authorized user records.

</td></tr><tr><td>

Consumer Connection \[sn\_sb\_pro\_consumer\_connection\]

</td><td>

Consumer connection record for provider, extends the base connection table.

</td></tr><tr><td>

Entitlement \[sn\_sb\_pro\_entitlement\]

</td><td>

Provider entitlements associating records to entitled consumers, extends base entitlement table.

</td></tr><tr><td>

Inbound Field \[sn\_sb\_pro\_inbound\_field\]

</td><td>

Manages provider side inbound field mappings for remote task definitions.

</td></tr><tr><td>

Outbound Field \[sn\_sb\_pro\_outbound\_field\]

</td><td>

Manages provider side outbound field mappings for remote task definitions.

</td></tr><tr><td>

Personas \[sn\_sb\_pro\_persona\]

</td><td>

Manages personas for Service Exchange.

</td></tr><tr><td>

Provider \[sn\_sb\_pro\_provider\]

</td><td>

Provider association record to tie provider side records together.

</td></tr><tr><td>

Provider Task \[sn\_sb\_pro\_provider\_task\]

</td><td>

Provider tasks on provider side, created by consumers through remote record producers.

</td></tr><tr><td>

Registration \[sn\_sb\_pro\_registration\]

</td><td>

Service Exchange registration records.

</td></tr><tr><td>

Remote Choice Definition \[sn\_sb\_pro\_remote\_choice\_definition\]

</td><td>

Remote choice definitions for remote record producer.

</td></tr><tr><td>

Consumer Criteria

 \[sn\_sb\_pro\_remote\_record\_producer\_consumer\_criteria\]

</td><td>

Consumer criteria records attributed to remote record producers, controls which consumers are entitled to a given remote record producer.

</td></tr><tr><td>

Remote service \[sn\_sb\_pro\_remote\_service\]

</td><td>

Remote service record.

</td></tr><tr><td>

Remote Task \[sn\_sb\_pro\_remote\_task\]

</td><td>

Remote tasks for managing data transfer between parent tasks on synced instances.

</td></tr><tr><td>

Remote Task Definition \[sn\_sb\_pro\_remote\_task\_def\]

</td><td>

Remote task definition, controls creation and processing of remote tasks.

</td></tr><tr><td>

Consumer Criteria

 \[sn\_sb\_pro\_remote\_task\_def\_consumer\_criteria\]

</td><td>

Consumer criteria records attributed to remote task definitions, controls which consumers are entitled to a given remote task definition.

</td></tr><tr><td>

Remote Task Variable \[sn\_sb\_pro\_remote\_task\_variable\]

</td><td>

Glide variables associated with a remote task, allows displaying incoming synced data

</td></tr><tr><td>

Service Exchange Settings \[sn\_sb\_pro\_service\_bridge\_settings\]

</td><td>

Settings record for provider, manages various Service Exchange settings alignment between provider and consumer.

</td></tr><tr><td>

Transform \[sn\_sb\_pro\_transform\]

</td><td>

Provider side transform records.

</td></tr></tbody>
</table>## Flows installed

The following flows are installed with the Service Exchange for Providers application.

<table id="table_cyl_nyp_gzb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Proactive Provider task from Case

 \[create\_proactive\_provider\_task\_from\_case\]

</td><td>

Creates provider task from case in proactive use case.

</td></tr><tr><td>

Process Incoming Consumer Provider Task

 \[process\_incoming\_consumer\_provider\_task\]

</td><td>

Manages incoming provider tasks from consumer.

</td></tr><tr><td>

Process Service Exchange registration

 \[process\_service\_bridge\_registration\]

</td><td>

Manages Service Exchange registration.

</td></tr><tr><td>

Service Exchange Attachment Sync to Task

 \[attachment\_sync\_provider\_task\_to\_task\]

</td><td>

Syncs attachments from provider task to parent task.

</td></tr><tr><td>

Service Exchange Case to Provider task Update

 \[service\_bridge\_case\_to\_provider\_task\_update\]

</td><td>

Manages creating provider tasks on case update.

</td></tr><tr><td>

Service Exchange Change Request to Provider

 task Update

 \[service\_bridge\_change\_request\_to\_provider\_task\_update\]

</td><td>

Manages creating provider tasks on change update.

</td></tr><tr><td>

Service Exchange Incident to Provider task\_Update

 \[service\_bridge\_incident\_to\_provider\_task\_update\]

</td><td>

Manages creating provider tasks on incident update.

</td></tr><tr><td>

Service Exchange Provider Task to Case Update

 \[service\_bridge\_provider\_task\_to\_case\_update\]

</td><td>

Manages processing of provider tasks and creation of associated parent case task.

</td></tr><tr><td>

Service Exchange provider task to Change

 Request Update

 \[service\_bridge\_provider\_task\_to\_change\_request\_update\]

</td><td>

Manages processing of provider tasks and creation of associated parent change request task.

</td></tr><tr><td>

Service Exchange provider task to Incident Update

 \[service\_bridge\_provider\_task\_to\_incident\_update\]

</td><td>

Manages processing of provider tasks and creation of associated parent incident task.

</td></tr></tbody>
</table>## Subflows installed

The following subflows are installed with the Service Exchange for Providers application.

<table id="table_m3v_kzp_gzb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create Case from Provider task

 \[create\_case\_from\_provider\_task\]

</td><td>

Creates parent task case from a Provider Task.

</td></tr><tr><td>

Create Change from Provider task

 \[create\_change\_from\_provider\_task\]

</td><td>

Creates parent task change from Provider Task.

</td></tr><tr><td>

Create Incident from Provider task

 \[create\_incident\_from\_provider\_task\]

</td><td>

Creates parent task incident from Provider Task.

</td></tr><tr><td>

Create OAuth Client

 \[create\_oauth\_client\]

</td><td>

Creates the OAuth client on onboarding.

</td></tr><tr><td>

Process invalid Provider task

 \[process\_invalid\_provider\_task\]

</td><td>

Manages provider tasks that have invalid configurations.

</td></tr><tr><td>

Repair RPS Consumer Connection Error

 \[repair\_rps\_consumer\_connection\_error\]

</td><td>

Attempts to fix Remote Process Sync errors in the Consumer Connection.

</td></tr></tbody>
</table>## Flow actions installed

The following flow actions are installed with the Service Exchange for Providers application.

<table id="table_ybb_wzp_gzb"><thead><tr><th>

Flow action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Copy attachment

 \[copy\_attachment\]

</td><td>

Copies a given attachment to a given record.

</td></tr><tr><td>

Copy task variables

 \[copy\_task\_variables\]

</td><td>

Retrieves task variable data for use in flows.

</td></tr><tr><td>

Create parent from remote task

 \[create\_parent\_from\_remote\_task\]

</td><td>

Creates a parent task from a given remote task.

</td></tr><tr><td>

Create remote task for consumer

 \[create\_remote\_task\_for\_consumer\]

</td><td>

Creates a remote task for a given parent task and consumer.

</td></tr><tr><td>

File Service Exchange registration email event \[file\_service\_bridge\_registration\_email\_event\]

</td><td>

Files email with information during Service Exchange registration.

</td></tr><tr><td>

Is Transporter User

 \[is\_transporter\_user\]

</td><td>

Checks if current user is transport user.

</td></tr><tr><td>

Parse Provider Task vars\_json

 \[parse\_provider\_task\_vars\_json\]

</td><td>

Parses out the vars json field on the Provider Task.

</td></tr><tr><td>

Repair RPS Consumer Connection

 \[repair\_rps\_consumer\_connection\]

</td><td>

Attempts to fix Remote Process Sync errors on Consumer Connection.

</td></tr></tbody>
</table>**Parent Topic:**[Service Exchange reference](service-bridge-v2-reference.md)


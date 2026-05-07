---
title: Components installed with Service Exchange for Consumers
description: Several types of components are installed with activation of the Service Exchange for Consumers application including tables, user roles, and business rules.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Reference, Service Exchange]
---

# Components installed with Service Exchange for Consumers

Several types of components are installed with activation of the Service Exchange for Consumers application including tables, user roles, and business rules.

**Note:** The Application Files \[sys\_metadata\] table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Roles installed

The following roles are installed with the Service Exchange for Consumers application.

<table id="table_gtr_pw3_bmb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Service Exchange admin \[sn\_sb.admin\]

</td><td>

-   Typically assigned to an administrator for the Service Exchange applications on both the customer and the provider side.
-   Provides read access to all Service Exchange tables

</td><td>

-   sn\_sb.read
-   sn\_sb.requestor
-   sn\_sb.remote\_task\_creator
-   flow\_designer
-   catalog

</td></tr><tr><td>

Service Exchange read \[sn\_sb.read\]

</td><td>

Provides read-only access to provider tasks

</td><td>

N/A

</td></tr><tr><td>

Service Exchange requester \[sn\_sb.requestor\]

</td><td>

Provides access to remote record producers and provider tasks

</td><td>

N/A

</td></tr></tbody>
</table>## Business rules installed

The following business rules are installed with the Service Exchange for Consumers application.

<table id="table_lgm_zdq_gzb"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Abort Duplicate Remote Task Insert

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Aborts remote task insert if one already exists matching the same parent and remote task definition.

</td></tr><tr><td>

Abort if duplicate transform is found

</td><td>

\[sn\_sb\_con\_transform\]

</td><td>

Aborts transform insert if duplicate is found.

</td></tr><tr><td>

Abort if duplicate URL

</td><td>

\[sn\_sb\_con\_provider\_connection\]

</td><td>

Aborts connection record insert if record with same URL is found.

</td></tr><tr><td>

Abort Remote Task Create If Missing Conn

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Aborts remote task insert if connection field is empty.

</td></tr><tr><td>

Add provider connection data to session

</td><td>

\[sn\_sb\_con\_provider\_connection\]

</td><td>

Saves connection data for later use.

</td></tr><tr><td>

Change state to Work in Progress

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Updates State to Work in Progress for provider tasks.

</td></tr><tr><td>

Check provider published variable

</td><td>

\[item\_option\_new\]

</td><td>

Verifies if the provider side variable published is valid.

</td></tr><tr><td>

Check Remote Task Def Simple Triggers

</td><td>

\[task\]

</td><td>

Checks if changes to parent task have triggered changes in the Remote Task Definition simple trigger conditions.

</td></tr><tr><td>

Clear Remote Task Client Data

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Clears client data associated with remote tasks after the transaction is completed.

</td></tr><tr><td>

Create or Update Transport Connection

</td><td>

\[sn\_sb\_con\_provider\_connection\]

</td><td>

Manages transport connection insert and update.

</td></tr><tr><td>

Create parent on synced remote task

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Creates parent task for synced remote tasks.

</td></tr><tr><td>

Delete associated records

</td><td>

\[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Deletes related records when Remote Task Definition is deleted.

</td></tr><tr><td>

Disconnect RT when RTD Deleted

</td><td>

\[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Disconnects all associated remote tasks when Remote Task Definition is deleted.

</td></tr><tr><td>

Error RT when Parent Deleted

</td><td>

\[task\]

</td><td>

Errors out all associated remote tasks when parent task is deleted.

</td></tr><tr><td>

Generate OAuth registry

</td><td>

\[sn\_sb\_con\_provider\_connection\]

</td><td>

Creates OAuth registry for a connection.

</td></tr><tr><td>

Handle authorized user transport

</td><td>

\[sn\_sb\_con\_authorized\_user\]

</td><td>

Sends authorized user records through transport layer.

</td></tr><tr><td>

Inactive Remote Task Definition when archived

</td><td>

\[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Deactivates Remote Task Definition on consumer instance when archived by provider.

</td></tr><tr><td>

Populate Company on Consumer

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Sets company field on provider tasks on Insert.

</td></tr><tr><td>

Populate Provider task data

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Adds extra data on Insert of Provider Task.

</td></tr><tr><td>

Process Deleted Entitlements

</td><td>

\[sn\_sb\_con\_entitlement\]

</td><td>

Manages entitlement deletion by deleting associated elements.

</td></tr><tr><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Entitlement attachment changes

</td><td>

\[sys\_attachment\]

</td><td>

Manages changes to attachments for entitlements.

</td></tr><tr><td>

Process New and Updated Entitlements

</td><td>

\[sn\_sb\_con\_entitlement\]

</td><td>

Manages creation of new entitlements and updates to existing entitlements.

</td></tr><tr><td>

Propagate Service Exchange Version Changes

</td><td>

\[v\_plugin\]

</td><td>

Tracks and updates settings when Service Exchange version is updated.

</td></tr><tr><td>

Remote Choice: cache user selection

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Caches user selections to prevent repeat requests for the same data.

</td></tr><tr><td>

Retry Errored RT on RTD Activation

</td><td>

\[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Attempts to create parent task creation for remote tasks with errors when the associated remote task definition is activated.

</td></tr><tr><td>

Set company field on remote task insert

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Sets the company field for remote tasks during Insert.

</td></tr><tr><td>

Set Connection Id from RRP

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Sets the Connection Id from the Remote Record Producer associated with the Provider Task.

</td></tr><tr><td>

Set Customer Version on Settings Insert

</td><td>

\[sn\_sb\_con\_service\_bridge\_settings\]

</td><td>

Sets the Service Exchange for Consumer application version on Settings during the Insert operation.

</td></tr><tr><td>

Set default values

</td><td>

\[sn\_sb\_con\_authorized\_user\]

</td><td>

Sets default values on authorized users when created.

</td></tr><tr><td>

Set outbound vars json on insert

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Sets the outbound json field on remote tasks when inserted by current instance.

</td></tr><tr><td>

Set Provider task number

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Sets provider task number on insert from client data

</td></tr><tr><td>

Set Remote Task number

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Sets remote task number on insert from client data

</td></tr><tr><td>

Set Table Details On Virtual Transform

</td><td>

\[sn\_sb\_con\_transform\]

</td><td>

Sets table data on virtual transforms.

</td></tr><tr><td>

Sync Attachment from Parent Task

</td><td>

\[sys\_attachment\]

</td><td>

Syncs attachments from parent task to all remote tasks associated with parent task.

</td></tr><tr><td>

Sync Remote Task Attachment to Parent

</td><td>

\[sys\_attachment\]

</td><td>

Syncs attachments from remote task to parent task.

</td></tr><tr><td>

Trigger changed attachment transport

</td><td>

\[sys\_attachment\]

</td><td>

Triggers attachment sync through transport layer when updated.

</td></tr><tr><td>

Trigger consumer PT transport

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Triggers provider task sync through transport layer.

</td></tr><tr><td>

Trigger consumer remote task transport

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Triggers remote task sync through transport layer during Insert or Delete operations.

</td></tr><tr><td>

Trigger inserted attachment transport

</td><td>

\[sys\_attachment\]

</td><td>

Triggers attachment sync through transport layer during Insert operation.

</td></tr><tr><td>

Trigger remote task transport update

</td><td>

\[sn\_sb\_con\_remote\_task\]

</td><td>

Triggers remote task sync through transport layer when updated.

</td></tr><tr><td>

Trigger SBScratchpad Transport

</td><td>

\[sn\_sb\_scratchpad\]

</td><td>

Triggers scratchpad sync through transport layer.

</td></tr><tr><td>

Trigger settings transport

</td><td>

\[sn\_sb\_con\_service\_bridge\_settings\]

</td><td>

Triggers settings record sync through transport layer.

</td></tr><tr><td>

Update entitlement status on delete

</td><td>

\[sn\_sb\_con\_service\_bridge\_settings\]

</td><td>

Updates entitlement status when deleted.

</td></tr><tr><td>

Update entitlement status on delete

</td><td>

\[sn\_sb\_con\_persona\]

</td><td>

Updates persona record on entitlement when deleted.

</td></tr><tr><td>

Update entitlement status on delete

</td><td>

\[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Updates Remote Task Definition record on entitlement when deleted.

</td></tr><tr><td>

Update entitlement status on update

</td><td>

\[sn\_sb\_con\_persona\]

</td><td>

Manages persona record on entitlement when updated.

</td></tr><tr><td>

Update entitlement status on update

</td><td>

\[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Manages Remote Task Definition record on entitlement when updated.

</td></tr><tr><td>

Update entitlement status on update

</td><td>

\[sn\_sb\_con\_remote\_record\_producer\]

</td><td>

Manages Remote Record Producer record on entitlement when updated.

</td></tr><tr><td>

Validate activation and complete setup

</td><td>

\[sn\_sb\_con\_remote\_record\_producer\]

</td><td>

Validates Remote Record Producer before activation.

</td></tr><tr><td>

Validate request on customer

</td><td>

\[sn\_sb\_con\_provider\_task\]

</td><td>

Checks for valid connection on Provider Task.

</td></tr><tr><td>

Warn if Global Script Include is missing

</td><td>

\[sn\_sb\_con\_remote\_record\_producer\]

</td><td>

Displays warning if global script include is not present when processing Remote Record Producer.

</td></tr></tbody>
</table>## Tables installed

<table id="table_ttz_z2q_gzb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Authorized user \[sn\_sb\_con\_authorized\_user\]

</td><td>

Authorized users.

</td></tr><tr><td>

Connection \[sn\_sb\_con\_consumer\]

</td><td>

Consumer side connection record.

</td></tr><tr><td>

Entitlement \[sn\_sb\_con\_entitlement\]

</td><td>

Consumer side table extending entitlements.

</td></tr><tr><td>

Inbound Field \[sn\_sb\_con\_inbound\_field\]

</td><td>

Consumer side inbound fields for Remote Task Definitions.

</td></tr><tr><td>

Outbound Field \[sn\_sb\_con\_outbound\_field\]

</td><td>

Consumer side outbound fields for Remote Task Definitions.

</td></tr><tr><td>

Personas \[sn\_sb\_con\_persona\]

</td><td>

Consumer side persona records.

</td></tr><tr><td>

Provider Connection \[sn\_sb\_con\_provider\_connection\]

</td><td>

Provider Connection record linking consumer to provider instance, extending base connection table.

</td></tr><tr><td>

Provider Task \[sn\_sb\_con\_provider\_task\]

</td><td>

Consumer side provider task records, extends Provider Task base table.

</td></tr><tr><td>

Remote Choice Cache \[sn\_sb\_con\_remote\_choice\_cache\]

</td><td>

Consumer side cache for remote choice queries.

</td></tr><tr><td>

Remote Record Producer \[sn\_sb\_con\_remote\_record\_producer\]

</td><td>

Consumer side Remote Record Producer records.

</td></tr><tr><td>

Remote Task \[sn\_sb\_con\_remote\_task\]

</td><td>

Consumer side remote task records, extends remote task base table.

</td></tr><tr><td>

Remote Task Definition \[sn\_sb\_con\_remote\_task\_def\]

</td><td>

Consumer side Remote Task Definition records.

</td></tr><tr><td>

Remote Task Variable\[sn\_sb\_con\_remote\_task\_variable\]

</td><td>

Remote Task associated variable table extending glide vars.

</td></tr><tr><td>

Service Exchange Settings \[sn\_sb\_con\_service\_bridge\_settings\]

</td><td>

Consumer side Service Exchange setting records, extends settings base table.

</td></tr><tr><td>

Remote Choice \[sn\_sb\_con\_st\_remote\_choice\]

</td><td>

Consumer side remote choice records.

</td></tr><tr><td>

Transform \[sn\_sb\_con\_transform\]

</td><td>

Consumer side transform records, extends transform base table.

</td></tr></tbody>
</table>## Flows installed

The following flows are installed with the Service Exchange for Consumers application.

<table id="table_qwz_zkc_kmb"><thead><tr><th>

Flow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Process Remote Record Producer Entitlements with Remote Choice Variables\[process\_remote\_record\_producer\_entitlements\_with\_remote\_choice\_variables\]

</td><td>

Processes entitlements for remote record producers on consumer with remote choice variables included.

</td></tr></tbody>
</table>## Subflows installed

The following subflows are installed with the Service Exchange for Consumers application.

<table id="table_ud5_pht_fzb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Repair RPS Provider Connection Error \[repair\_rps\_provider\_connection\_error\]

</td><td>

Handles provider connection errors with Remote Process Sync when in error state.

</td></tr></tbody>
</table>## Flow actions installed

The following flow actions are installed with the Service Exchange for Consumers application.

|Action|Description|
|------|-----------|
|Create Parent From Remote Task \[create\_parent\_from\_remote\_task\]|Creates a parent record for a synced remote task.|
|Create Record Producer and Remote Choice Dependent Variables \[create\_record\_producer\_and\_entities\]|Creates a remote record producer and the associated remote choice dependent variables from a synced entitlement.|
|Create Remote Task \[create\_remote\_task\]|Creates a remote task for a given parent and remote task definition.|
|Repair RPS Provider Connection \[repair\_rps\_provider\_connection\]|Attempts to fix Remote Process Sync errors on Provider Connection.|


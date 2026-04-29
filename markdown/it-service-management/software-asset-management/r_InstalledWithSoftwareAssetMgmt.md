---
title: Installed with the legacy Software Asset Management plugin
description: A number of tables, properties, user roles, script includes, client scripts, UI policies, and business rules are installed with the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Legacy Software Asset Management plugin Overview module, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Installed with the legacy Software Asset Management plugin

A number of tables, properties, user roles, script includes, client scripts, UI policies, and business rules are installed with the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

**Note:** Demo data is available with the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Tables

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following tables.

<table id="table_sdt_dxt_hq"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Processor Definition \[cmdb\_processor\_definition\]

</td><td>

Describes a computer in terms of the attributes IBM uses for its PVU licensing model. If they are all identical in terms of the attributes used for PVU licensing, a row can be associated with one or more discovered computers.

</td></tr><tr><td>

Processor Mapping \[sam\_processor\_mapping\]

</td><td>

Encodes the information specified by the IBM [Table of Processor Value Units per core](https://www-01.ibm.com/software/lotus/passportadvantage/pvu_licensing_for_customers.html) and is used in matching a computer's processor definition to a PVU cost for that computer. Each row in this table is a mapping between a set of processors and the associated PVU cost \(per core\).

</td></tr><tr><td>

Software Counter \[sam\_sw\_counter\]

</td><td>

Configures license counting options for software models.

</td></tr><tr><td>

Software Counter Compliance Violations \[sam\_sw\_counter\_violation\]

</td><td>

Stores records of software counter compliance issues that are due to violations other than installs exceeding rights, such as:-   Maximum CPU/user count exceeded, based on model limits.
-   Maximum or minimum rights rules not followed, based on model limits.
-   Options installed on a server with a license that does not support options \(Oracle\).

</td></tr><tr><td>

Software Counter Detail \[sam\_sw\_counter\_detail\]

</td><td>

Reconciles a software installation or usage with its corresponding software license and entitlement. The software counting logic automatically generates and maintains these records.

</td></tr><tr><td>

Software Counter History \[sam\_sw\_counter\_history\]

</td><td>

Stores read-only copies of software counter records, which the system generates automatically each time a software counter finishes counting licenses.

</td></tr><tr><td>

Software Counter Result \[sam\_sw\_counter\_result\]

</td><td>

Records all software counter results. Organizes the results based on the Grouping field \(such as Company, Department, or Location\) on the Software Counter record.

</td></tr><tr><td>

Software Counter Summary \[sam\_sw\_counter\_summary\]

</td><td>

Aggregates all the software counter details for a given allocation state, a given group, and a given software counter. The software counting logic automatically generates and maintains these records.

</td></tr><tr><td>

Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Stores a unique and definitive list of all software found by a discovery tool.

</td></tr><tr><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Associates software discovery models and the hardware on which they are installed.

</td></tr><tr><td>

Software Usage \[cmdb\_sam\_sw\_usage\]

</td><td>

Associates software discovery models and the hardware that uses the models. ServiceNow Discovery does not populate the Software Usage \[cmdb\_sam\_sw\_usage\] table. Use a third-party tool to add information about software assets to the Software Usage table.

</td></tr></tbody>
</table>## Properties

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following system properties.

<table id="table_ckb_lyt_hq"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sam.install\_deletion\_deadline

</td><td>

Defines the number of days after which a software install is deleted if not discovered with the configuration item. Use a value that is greater than the number of days between consecutive discovery runs.-   Type: integer
-   Default value: 7
-   Location: System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>## User roles

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following user roles.

<table id="table_p5d_czt_hq"><thead><tr><th>

Role

</th><th>

Contains roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sam

</td><td>

inventory\_user

 contract\_manager

 category\_manager

 financial\_mgmt\_user

</td><td>

Can create, edit, change, and manage software licenses. Can edit the Software model field on a Discovery model. Can approve a model. Has full control of the [Legacy Software Asset Management plugin](../concept/c_SoftwareAssetManagement.md). Controls the legacy IBM PVU Process Pack, if activated.

</td></tr></tbody>
</table>## Script includes

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following script includes.

|Name|Description|
|----|-----------|
|DiscoveryModelMatcher|Matches a discovery model with a software product model.|
|ProcessorDefinitionsUtils|Contains utilities for managing the Processor Definition \[cmdb\_processor\_definition\] table.|
|ProcessorValueUnitsUtils|Contains logic that determines the IBM PVU pricing associated with a given processor. Also generates an event when a processor mapping is not found.|
|SAMMigration|Deprecated. Used by the fix job that migrates software license management data to the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.|
|SAMSuiteEngine|Contains functions for handling suite inference on software installations.|
|SAMUtil|Generates models and counters for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.|

## Client scripts

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following client scripts.

|Name|Table|Description|
|----|-----|-----------|
|Clean up Counter|Software Counter \[sam\_sw\_counter\]|Ensures integrity between the various counting options of a software counter.|
|Deactivate automatched checkbox|Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]|Deactivates the automatically matched check box when a user edits the software model.|
|Notify if counter in progress|Software Counter \[sam\_sw\_counter\]|Displays a message if the counter is currently running.|

## UI policies

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following UI policies.

|Name|Table|Description|
|----|-----|-----------|
|Enforce Installs per license|Software Counter \[sam\_sw\_counter\]|Makes the Installs per license field mandatory when the software counter License type is By number of users.|
|Handle custom counts|License Calculation \[sam\_sw\_license\_calculation\]|Displays the fields for entitlement type and valuation script when Count by is set to custom.|
|Hide condition fields|Software Counter \[sam\_sw\_counter\]|Hides the Software usage condition field if the license calculation query table is set to Software install and hides the Software install condition field if the license calculation query table is set to Software usage.|
|Hide query table|Software Counter \[sam\_sw\_counter\]|Hides the Query table field on the Software Counter form.|

## Business rules

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following business rules.

<table id="table_km4_yc5_hq"><thead><tr><th>

Name

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assign processor

</td><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Attempts to match a processor with a processor definition.

</td></tr><tr><td>

Build Primary Key

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Sets the primary key for the record to the serial number on the \[cmdb\_sam\_sw\_install\] table. If the serial number is empty, the rule creates one based on the publisher, display name, product ID, version, and revision.

</td></tr><tr><td>

Build Primary Key

</td><td>

Software Usage \[cmdb\_sam\_sw\_usage\]

</td><td>

Creates the primary key for the record from the publisher, name, product ID, and version number on the \[cmdb\_sam\_sw\_usage\] table.

</td></tr><tr><td>

Check for software suite

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Checks if the current software install is part of a software suite.

</td></tr><tr><td>

Check for suite omission

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Checks if the current software install should be omitted from any suites.

</td></tr><tr><td>

Clean up Cache

</td><td>

Software License \[alm\_license\]

</td><td>

Removes the cache for the counter of the software license record when a software license is deleted.

</td></tr><tr><td>

Clean up software normalization

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Deletes the discovery model if the discovery model is changed and it is not used by other software installs. This rule is not enabled by default.

</td></tr><tr><td>

Clear install and usage records

</td><td>

Software Counter Summary \[sam\_sw\_counter\_summary\]

</td><td>

Uncaches all related install and usage records when a software counter summary is deleted.

</td></tr><tr><td>

Clear normalized flag

</td><td>

Software Usage \[cmdb\_sam\_sw\_usage\]

</td><td>

Clears normalized flag on certain field changes.

</td></tr><tr><td>

Clear normalized flag

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Clears the is\_normalized check box when a field value is changed from a normalized value.

</td></tr><tr><td>

CPU/Core count change

</td><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Clears the Cached check box on related software installs when the [CPU count or CPU core count](../task/t_FindingSoftwareOnTheNetwork.md) changes.

</td></tr><tr><td>

Create a Software Normalization

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Links the record to the discovery model with that primary key on the \[cmdb\_sam\_sw\_install\] table if the primary key changes. The business rule creates a discovery model if none exist for that primary key.

</td></tr><tr><td>

Create a Software Normalization

</td><td>

Software Usage \[cmdb\_sam\_sw\_usage\]

</td><td>

Links the record to the discovery model with that primary key on the \[cmdb\_sam\_sw\_usage\] table if the primary key changes. The business rule creates a discovery model if none exist for that primary key.

</td></tr><tr><td>

Delete cached count results

</td><td>

Software License \[alm\_license\]

</td><td>

Marks the software counter results to be recounted when one or more fields on a license have changed. This script runs after a change to a field that a counter can be grouped on, such as location, department, company, cost\_center, entitlement\_condition, or assigned\_condition. If one or more of these fields changes, then the script sets the Recount field to true on any cached counter results matching the previous value. When the counter runs, the results with Recount set to true are treated as non-cached results and are recounted. For example, if Location on a license was Americas and changes to EMEA, cached results for Americas will have Recount set to true for the next count.

</td></tr><tr><td>

Delete Cached row entry

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

When an entitlement is deleted:-   Deletes all related software counter details.
-   Clears the Cached check box on the related software install.

</td></tr><tr><td>

Drop counter Cache

</td><td>

Software Counter \[sam\_sw\_counter\]

</td><td>

Clears the Cached check box for the software counter if the grouping, license type, contract, or installs per license change in a software counter. Added enforce field changes to the conditions

</td></tr><tr><td>

Flag counter to reprocess

</td><td>

Software Upgrade and Downgrades \[cmdb\_m2m\_downgrade\_model\]

</td><td>

Clears the Cached check box for all related software counters if the upgrade parent or downgrade child values are changed or deleted.

</td></tr><tr><td>

Flag counter to reprocess

</td><td>

Software Suite \[cmdb\_m2m\_suite\_model\]

</td><td>

Clears the Cached check box for all related software counters if the suite parent or suite child values are changed or deleted.

</td></tr><tr><td>

invalidate sw install cache

</td><td>

Computer \[cmdb\_ci\_computer\]

</td><td>

Uncaches all install and usage records referencing a computer when the computer's processor field is changed.

</td></tr><tr><td>

Limit license metric

</td><td>

License \[alm\_license\]

</td><td>

Limits software licenses to a single license metric value.

</td></tr><tr><td>

Limit license metric combinations

</td><td>

Hardware \[cmdb\_ci\_hardware\]

</td><td>

Rejects license metric combinations of the same type, such as CAL \(user\) and CAL \(devices\).

</td></tr><tr><td>

Link to Model

</td><td>

Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Finds and sets the model field to the model that best corresponds to the record when a software discovery model is created.

</td></tr><tr><td>

Mark install for suite omission

</td><td>

License Entitlement \[alm\_entitlement\]

</td><td>

Searches for any matching installs and marks them for suite omission.

</td></tr><tr><td>

One and only one default mapping

</td><td>

Processor Mapping \[sam\_processor\_mapping\]

</td><td>

Ensures only one default mapping by resetting the last resort flag for modified records and setting it to false for new records.

</td></tr><tr><td>

Process cache reset

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Resets the install of any counter information when it becomes uncached.

</td></tr><tr><td>

Process suite component deletion

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Updates all other members of an install's suite if the install is deleted.

</td></tr><tr><td>

rebind processor definitions

</td><td>

Processor Mapping \[sam\_processor\_mapping\]

</td><td>

Refreshes processor definitions when a processor mapping changes.

</td></tr><tr><td>

Rebuild Cache

</td><td>

Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Clears the Cached field on the software counter if the associated software model is modified on the software discovery model record.

</td></tr><tr><td>

Rebuild inferred suite and cached

</td><td>

Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Clears the cached flag and inferred suite field on records referencing this discovery model, when the matched model changes.

</td></tr><tr><td>

Remove cached flag

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Clears the corresponding cached software counter details if a software installation is deleted or if the configuration item on which it is installed changes.

</td></tr><tr><td>

Remove cached flag

</td><td>

Software Usage \[cmdb\_sam\_sw\_usage\]

</td><td>

Clears the corresponding cached software counter details if a software usage record is deleted or if the configuration item from which the software is accessed changes.

</td></tr><tr><td>

Remove caches from detail

</td><td>

Software Counter Detail \[sam\_sw\_counter\_detail\]

</td><td>

Clears the Cached check box on the related entitlement, installation, and usage records if they exist.

</td></tr><tr><td>

Reset counter info on suite change

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Uncaches and resets counter information on the install if its inferred suite changes.

</td></tr><tr><td>

Reset Installs per License

</td><td>

Software Counter \[sam\_sw\_counter\]

</td><td>

Clears the Installations per license fields if the counter license type is not per user.

</td></tr><tr><td>

Retrieve PVU Mapping

</td><td>

Processor Definition \[cmdb\_processor\_definition\]

</td><td>

Finds a matching processor mapping based on the information of the processor definition.

</td></tr><tr><td>

SAM: Core Process

</td><td>

Global \[global\]

</td><td>

Not used for any processing.

</td></tr><tr><td>

Set Display name

</td><td>

Software Counter Result \[sam\_sw\_counter\_result\]

</td><td>

Sets the display name of the counter result to the counter name with the grouping type.

</td></tr><tr><td>

Set normalized fields

</td><td>

Software Usage \[cmdb\_sam\_sw\_usage\]

</td><td>

Sets normalized fields on insert to be copies of discovered fields.

</td></tr><tr><td>

Set normalized fields

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Copies the given values as their normalized values when a software install is inserted.

</td></tr><tr><td>

Sync Software Package

</td><td>

Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\]

</td><td>

Creates a row in the package table to reflect the row in the discovery model table.

</td></tr><tr><td>

Update Cache

</td><td>

Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Updates all corresponding cached software counter details if usage metrics for this installation change.

</td></tr><tr><td>

Update Cache

</td><td>

Software Usage \[cmdb\_sam\_sw\_usage\]

</td><td>

Updates all corresponding cached software counter details if usage metrics for this software usage change.

</td></tr></tbody>
</table>## References

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds the following references.

|Name|Description|
|----|-----------|
|Processor Definition|If you activated the legacy IBM PVU Process Pack after activating the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin, a reference to the processor definition is added to the Hardware \[cmdb\_ci\_hardware\] table.|

**Parent Topic:**[Legacy Software Asset Management plugin Overview module](../concept/c_SWAssetMgmtOverviewMod.md)

**Related topics**  


[Use the legacy Software Asset Management plugin Overview module](../concept/c_UseSWAssetMgmtOverviewMod.md)

[Legacy Software Asset Management plugin roles](r_SoftwareAssetManagementRoles.md)


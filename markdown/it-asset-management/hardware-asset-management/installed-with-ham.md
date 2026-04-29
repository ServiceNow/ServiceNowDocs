---
title: Installed with Hardware Asset Management
description: Several types of components are installed with activation of the sn\_hamp plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Installed with Hardware Asset Management

Several types of components are installed with activation of the sn\_hamp plugin, including tables, user roles, and scheduled jobs.

## Roles installed

<table id="table_j1k_3f5_fyb"><thead><tr><th>

Role title

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

ham\_admin

</td><td>

Grants full access to the respective features of the Hardware Asset Management application including the ability to Opt-in for the Content Service. This role is used for Hardware Asset Management.

</td><td>

-   inventory\_admin
-   catalog\_manager
-   report\_user
-   sn\_hamp.ham\_user
-   asset
-   procurement\_admin

</td></tr><tr><td>

sn\_hamp.ham\_user

</td><td>

Manage hardware assets and reports. This role enables users to view, create, update, and delete hardware asset records, and to generate and view asset-related reports. This role is tailored for everyday asset management tasks.

</td><td>

asset

</td></tr></tbody>
</table>## Granular roles

<table id="table_rxh_hmp_yhc"><thead><tr><th>

HAM functionality

</th><th>

Granular admin role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HAM licensing

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Provides access to:-   Edit Exclusion flag \[ excluded\_from\_ham\] value over asset
-   **HAM Resource Categories** menu

</td></tr><tr><td>

Advanced Shipment Notification \(ASN\)

</td><td>

sn\_hamp.ham\_asn\_admin

</td><td>

Provides access to:-   **Import shipment notification** and **Import status** UI options
-   Read access to the **Import template** page

</td></tr><tr><td>

Zero touch request

</td><td>

asset\_integration\_admin

</td><td>

Provides access to:-   Create provider integration profile records in the Provider integration profile \[sn\_hamp\_provider\_int\_profile\] table
-   **Provider integration profiles** list in the Asset operations view of the Hardware Asset Workspace

</td></tr><tr><td>

HAM Guided Setup

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Provides access to:-   **HAM Guided Setup** module
-   **Getting started** page of Hardware Asset Management Guided Setup

</td></tr><tr><td>

HAM application properties

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Access to the following application properties:-   **sn\_hamp.enable\_asset\_action\_validation\_incident**
-   **sn\_hamp.enable\_asset\_action\_validation\_change\_request**
-   **sn\_hamp.enable\_asset\_tag\_serial\_number\_edits**

</td></tr><tr><td>

HAM system properties

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Access to the following system properties:-   **sn\_hamp.update\_assets\_norm\_model\_name**
-   **sn\_hamp.enable\_asset\_action\_validation\_change\_request**
-   **sn\_hamp.enable\_asset\_tag\_serial\_number\_edits**
-   **sn\_hamp.enable\_shipping\_carrier\_validation\_asn**
-   **glide.ui.sn\_hamp\_loaner\_asset\_order\_activity.fields**
-   **sn\_hamp.enable\_custom\_category\_licensing**
-   **sn\_hamp.model\_lifecycle\_phase\_order**
-   **sn\_hamp.sn\_ham\_active\_entitlements**
-   **glide.sg.voice\_search.enabled**
-   **glide.ui.sn\_hamp\_asset\_reclaim\_task\_activity.fields**
-   **glide.ui.sn\_hamp\_ztr\_task\_activity.fields**
-   **sn\_itam\_common.close\_attestation\_async**
-   **sn\_itam\_common.sn\_enable\_indoormap\_for\_assets**
-   **com.sn\_itam.enable\_flow\_designer.transfer\_order\_line**
-   **sn\_itam\_common.asset\_tco\_benchmark\_threshold\_percentage**
-   **sn\_itam\_common.put\_away\_task.drop\_off\_location.delimiter**
-   **com.sn\_itam.enable\_flow\_designer.transfer\_order**

</td></tr><tr><td>

Important Actions in the Inventory view of the Hardware Asset Workspace

</td><td>

Admin role isn't required. The asset, inventory\_admin, or ham\_admin role is sufficient.

</td><td>

You can view the following important action cards in the Inventory view without the admin role:-   **Inventory - Stale shipments**
-   **Inventory - Carrier integration failures**
-   **Inventory - Unmapped carrier profiles**

</td></tr><tr><td>

Asset operations list in the Hardware Asset Workspace

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Provides access to the following lists in the Assets operations view:-   **Asset warranty**
-   **Carrier integration profiles**

</td></tr><tr><td>

Loaner asset order

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Provides access to delete records in the Loaner Asset Order \[sn\_hamp\_loaner\_asset\_order\] table.

</td></tr><tr><td>

Shipment

</td><td>

asset\_integration\_admin

</td><td>

Provides write access to the Ignore stale check \[ignore\_stale\_check\] column in the Shipment \[sn\_itam\_common\_shipment\] table.

</td></tr><tr><td>

Carrier integration

</td><td>

asset\_integration\_admin

</td><td>

Provides access to the Carrier Integration Profile \[sn\_itam\_carrier\_int\_profile\] table to perform the following tasks:-   Create carrier integration profiles
-   View reports

</td></tr><tr><td>

Import assets

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Provides access to the **sn\_itam\_common.receive\_assets\_batch\_size** system property and application property.

</td></tr><tr><td>

Attestation

</td><td>

Admin role isn't required. The asset or inventory\_admin is sufficient.

</td><td>

Provides access to the following UI actions:-   **Cancel attestation**
-   **Cancel schedule**

</td></tr><tr><td>

Contract renewal

</td><td>

contract\_system\_admin

</td><td>

Provides Write access to the **sn\_itam\_common.sn\_contract\_enable\_renewal\_flow** system property.

</td></tr><tr><td>

ITAM AI agents

</td><td>

asset\_aia\_admin

</td><td>

Provides access to read, write, delete, and report on the ITAM AI Agents Log \[itam\_aia\_log\] table.

</td></tr><tr><td>

Common Hardware Asset Management and Enterprise Asset Management tables

</td><td>

sn\_hamp.ham\_system\_admin

</td><td>

Provides access to the following tables:-   RFID Connection Attributes \[sn\_itam\_common\_rfid\_conn\_attr\]
-   RFID Stage Asset \[sn\_itam\_common\_rfid\_stg\_asset\]
-   Repair order \[sn\_itam\_common\_repair\_order\]
-   Repair order line \[sn\_itam\_common\_repair\_orderline\]
-   Asset order \[sn\_itam\_common\_asset\_order\]
-   Asset order line \[sn\_itam\_common\_asset\_orderline\]
-   Loaner Asset Order \[sn\_itam\_common\_loaner\_asset\_order\]

</td></tr></tbody>
</table>## Scheduled jobs installed

<table id="table_l1k_3f5_fyb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HAM - Content Upload

</td><td>

Publishes the normalized hardware models.

</td></tr><tr><td>

HAM - Daily Job

</td><td>

Calculates number of hardware and consumable models for each model category, active life cycle phase for models, and sets client schedule pull-time.

</td></tr><tr><td>

HAM - Hardware Lifecycles

</td><td>

Generates hardware life cycles.

</td></tr><tr><td>

HAM - Hardware Normalization

</td><td>

Normalizes hardware and consumables models.

</td></tr><tr><td>

HAM - Loaner Asset Order Allocations

</td><td>

Allocates assets to Loaner Asset Orders.

</td></tr><tr><td>

HAM - Populate Licensing Data

</td><td>

Populates licensing details.

</td></tr><tr><td>

HAMP - Content File Manager

</td><td>

Job is triggered from the Manage Hardware Library.

</td></tr><tr><td>

Purge Asset Audits More Than Year Old or with More Than 10k Assets

</td><td>

Removes old asset audit records or asset audits with more that 10K assets.

</td></tr><tr><td>

\[PA HAM\] Daily collection job

</td><td>

Daily job that collects scores for different parameters.

</td></tr></tbody>
</table>## Tables installed

<table id="table_n1k_3f5_fyb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Bundle

 \[alm\_bundle\]

</td><td>

Details of bundle assets.

</td></tr><tr><td>

Asset Audits

 \[sn\_hamp\_asset\_audit\]

</td><td>

Details of the asset audits.

</td></tr><tr><td>

Hardware Asset Reclamation Line

 \[sn\_hamp\_asset\_reclaim\_line\]

</td><td>

Details of the Hardware Asset Reclamation Lines created for each reclaimed asset.

</td></tr><tr><td>

Hardware Asset Reclamation Task

 \[sn\_hamp\_asset\_reclaim\_task\]

</td><td>

Details of the tasks created for each Hardware Asset Reclamation Line.

</td></tr><tr><td>

Asset RMA Task

 \[sn\_hamp\_asset\_rma\_task\]

</td><td>

List of RMA asset task records.

</td></tr><tr><td>

Hardware Asset Configuration

 \[sn\_hamp\_configuration\]

</td><td>

Configuration records of Hardware Asset Management.

</td></tr><tr><td>

HAM Content Audit

 \[sn\_hamp\_content\_audit\]

</td><td>

Details of content values that changed.

</td></tr><tr><td>

Contract Renewal Request \[sn\_contract\_renewal\_request\]

</td><td>

Stores all the contract renewal requests through the contract renewal workflow.

</td></tr><tr><td>

Contract Renewal Request Line \[sn\_contract\_renewal\_request\_line\]

</td><td>

Stores all the contract renewal request lines through the contract renewal workflow.

</td></tr><tr><td>

Contract Renewal Task \[sn\_contract\_renewal\_task\]

</td><td>

Stores all the contract renewal request tasks through the contract renewal workflow.

</td></tr><tr><td>

Custom Device Type

 \[sn\_hamp\_custom\_hw\_device\_type\]

</td><td>

List of custom hardware device type records.

</td></tr><tr><td>

Custom Hardware Manufacturer

 \[sn\_hamp\_custom\_hw\_manufacturer\]

</td><td>

List of custom hardware device manufacturer records.

</td></tr><tr><td>

Custom Hardware Product

 \[sn\_hamp\_custom\_hw\_product\]

</td><td>

List of custom hardware product records.

</td></tr><tr><td>

Custom Hardware Model Library

 \[sn\_hamp\_custom\_hw\_prod\_model\]

</td><td>

List of custom hardware model library records.

</td></tr><tr><td>

Hardware Disposal Order

 \[sn\_hamp\_hardware\_disposal\]

</td><td>

List of Hardware Disposal Order records.

</td></tr><tr><td>

Hardware Disposal Tasks

 \[sn\_hamp\_hw\_asset\_disposal\_task\]

</td><td>

Details of the tasks associated with the Hardware Disposal Order flow.

</td></tr><tr><td>

Device Type

 \[sn\_hamp\_hw\_device\_type\]

</td><td>

List of hardware device type records.**Important:** You mustn't modify the records of this table.

</td></tr><tr><td>

Hardware Manufacturer

 \[sn\_hamp\_hw\_manufacturer\]

</td><td>

List of hardware device manufacturer records.

</td></tr><tr><td>

Hardware Normalization Map

 \[sn\_hamp\_hw\_normalization\_map\]

</td><td>

Product details such as hardware product and hardware product model IDs.

</td></tr><tr><td>

Hardware Product

 \[sn\_hamp\_hw\_product\]

</td><td>

Product details such as name of the product and type of device.

</td></tr><tr><td>

Hardware Model Library

 \[sn\_hamp\_hw\_product\_model\]

</td><td>

Product details such as product and model number.

</td></tr><tr><td>

Hardware Asset Refresh Line

 \[sn\_hamp\_hw\_refresh\_line\]

</td><td>

Hardware Asset Refresh Line details such as stage, requested item, replacement model, and replacement asset.

</td></tr><tr><td>

Refresh Line Tasks

 \[sn\_hamp\_hw\_refresh\_line\_task\]

</td><td>

Details of Refresh Line tasks associated with the Hardware Asset Refresh Lines.

</td></tr><tr><td>

Import Staging

 \[sn\_hamp\_import\_template\]

</td><td>

Template for importing assets and model records.

</td></tr><tr><td>

Hardware Lifecycle Definition

 \[sn\_hamp\_lifecycle\_definition\]

</td><td>

Life cycle phase of a hardware or consumable model and the associated dates.

</td></tr><tr><td>

Loaner Asset Order

 \[sn\_hamp\_loaner\_asset\_order\]

</td><td>

List of Loaner Asset Order records.

</td></tr><tr><td>

Loaner Asset Task

 \[sn\_hamp\_loaner\_asset\_task\]

</td><td>

List of Loaner Asset Order task records.

</td></tr><tr><td>

Audits to Scanned Assets

 \[sn\_hamp\_m2m\_audit\_asset\]

</td><td>

List of audit records of scanned assets.

</td></tr><tr><td>

Planned Assets

 \[sn\_hamp\_m2m\_hw\_asset\_disposal\]

</td><td>

Details of the assets included in Hardware Asset Disposal Orders.

</td></tr><tr><td>

Replacement Models

 \[sn\_hamp\_m2m\_ztr\_replacement\_model\]

</td><td>

List of replacement records for Zero Touch Refresh models.

</td></tr><tr><td>

Manage Hardware Library

 \[sn\_hamp\_manage\_hw\_library\]

</td><td>

List of Hardware Library content import records.

</td></tr><tr><td>

Model Category Normalization Summary

 \[sn\_hamp\_model\_ctg\_norm\_summary\]

</td><td>

Summary of normalization of model category.

</td></tr><tr><td>

HAM Resource Category

 \[sn\_hamp\_resource\_category\]

</td><td>

Subscription unit ratio and other licensing-related details of each Resource category.

</td></tr><tr><td>

RMA Request

 \[sn\_hamp\_rma\_request\]

</td><td>

List of RMA request records.

</td></tr><tr><td>

RMA Request Line

 \[sn\_hamp\_rma\_request\_line\]

</td><td>

List of RMA request line records of RAM requests.

</td></tr><tr><td>

HAM Success Activity

 \[sn\_hamp\_success\_activity\]

</td><td>

List of HAM Success Activity records.

</td></tr><tr><td>

HAM Success Goal

 \[sn\_hamp\_success\_goal\]

</td><td>

List of HAM Success Goal records.

</td></tr><tr><td>

Zero Touch Refresh Model

 \[sn\_hamp\_ztr\_refresh\_model\]

</td><td>

Details of refresh model records for the Zero Touch Refresh flow.

</td></tr><tr><td>

Zero Touch Refresh Request

 \[sn\_hamp\_ztr\_request\]

</td><td>

List of Zero Touch Refresh request records.

</td></tr><tr><td>

Zero Touch Refresh Task

 \[sn\_hamp\_ztr\_task\]

</td><td>

Details of tasks associated with the Zero Touch Refresh flow.

</td></tr><tr><td>

RFID asset

 \[rfid\_asset\]

</td><td>

Stores the RFID information of assets.

</td></tr></tbody>
</table>**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)

